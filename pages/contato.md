---
layout: page
permalink: "/contato.html"
title: "Como chegar até nós?"
description: 'Entre em contato conosco para melhor atende-los.'
---
<section id="contact-info">

    <div class="gmap-area">
        <div class="container">
            <div class="row">

                <div class="col-sm-6 map-content">
                    <ul class="row">
                        <li class="col-sm-6">
                            <address>
                                <h5>Vabene Transtur</h5>
                                <p>CNPJ: {{site.cnpj}}<br>
                                 {{site.rua}} - {{site.bairro}} <br>
                                Cidade: {{site.cidade}}/{{site.estado}} <br>
                                CEP:{{site.cep}}<br>
                                {{site.email}}</p>
                            </address>
                        </li>                            
                    </ul>
                </div>

                <div class="col-sm-6 text-center">
                    <div class="gmap">
                        <iframe frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3670.048072888577!2d-46.98045138503089!3d-23.095335984916215!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94cf2e01a976cdc7%3A0xfd63a76d21890a23!2sR.+S%C3%A3o+Paulo%2C+21+-+Parque+Brasil%2C+Louveira+-+SP%2C+13290-000!5e0!3m2!1spt-BR!2sbr!4v1449339630702"></iframe>
                    </div>
                </div>


            </div>
        </div>
    </div>
</section>  <!--/gmap_area -->
<br>
<section id="contact-page">
    <div class="container">
        <div class="center">        
            <h2>Envie sua mensagem</h2>
            <p class="lead">Entre em contato conosco pelo formulário abaixo</p>
        </div>
        <div class="row contact-wrap">
            <div class="status alert alert-success" style="display: none"></div>


             <form id="my-form" action="https://formspree.io/f/xeqvkolj" method="POST">
                    <div class="row">
                        <div class="col-md-5 col-sm-offset-1">
                            <div class="form-group">
                                <label>Nome Completo *</label>
                                <input type="text" class="form-control" id="name" name="nome" required data-validation-required-message="Nome Completo">
                                <p class="help-block text-danger"></p>
                            </div>
                            <div class="form-group">
                                <label>Email *</label>
                                <input type="email" name="email" class="form-control" id="email" required data-validation-required-message="Email">
                                <p class="help-block text-danger"></p>
                            </div>
                            <div class="form-group">
                                 <label>Telefone / Celular *</label>
                                <input name="telefone" type="tel" class="form-control" id="phone" required data-validation-required-message="Telefone/Celular">
                                <p class="help-block text-danger"></p>
                            </div>


                          <label for="Assunto">Assunto:</label>
                            <select class="form-control" name="Assunto">
                              <option value="Contato">Contato</option>
                              <option value="Solicitar orçamento">Solicitar orçamento</option>
                          </select>

                        </div>
                        <div class="col-md-5">
                            <div class="form-group">
                                <label>Mensagem *</label>
                                <textarea class="form-control" id="message"  type="text" name="mensagem" required data-validation-required-message="Escreva sua mensagem" rows="8"></textarea>
                                <p class="help-block text-danger"></p>
                            </div>
                        </div>
                        <div class="clearfix"></div>
                        <div class="col-lg-12 text-center">
                            <p id="my-form-status"></p>
                            <button type="submit" class="btn btn-primary btn-lg" id="my-form-button">Enviar Mensagem</button>
                        </div>
                    </div>
                </form>

                <!-- Place this script at the end of the body tag -->

                <script>
                    var form = document.getElementById("my-form");

                    async function handleSubmit(event) {
                      event.preventDefault();
                      var status = document.getElementById("my-form-status");
                      var data = new FormData(event.target);
                      fetch(event.target.action, {
                        method: form.method,
                        body: data,
                        headers: {
                            'Accept': 'application/json'
                        }
                      }).then(response => {
                        status.innerHTML = "Sua mensagem foi enviada com sucesso!!";
                        form.reset()
                      }).catch(error => {
                        status.innerHTML = "Oops! Algum problema no envio da sua mensagem!"
                      });
                    }
                    form.addEventListener("submit", handleSubmit)
                </script>


<br />

        </div><!--/.row-->
    </div><!--/.container-->
</section><!--/#contact-page-->
