---
layout: page
permalink: "/formulario-viagens-e-excursoes.html"
title: "Formulário"
description: 'Preencha!'
endpoint: '4fa54e79-da38-4579-8ca2-8999eb8084c8'
---

<div class="row">
      <div class="col-md-6 col-sm-12 wow fadeInDown">

      <h3><b>Formulário de Viagens e Excursões</b></h3>

      <form id="my-form" action="https://formspree.io/f/xgepyapr" method="POST">

        <div class="form-group col-md-12 col-xs-12">
          <input class="form-control" type="text" name="name" placeholder="Nome completo">
        </div>

        <div class="form-group col-md-6 col-xs-12">
          <input class="form-control" type="email" name="_replyto" placeholder="Email">
        </div>

        <div class="form-group col-md-6 col-xs-12">
          <input type="text" class="form-control" name="telefone" placeholder="Telefone">
        </div>

        <div class="form-group col-md-8 col-xs-12">
          <input type="text" class="form-control" name="destino" placeholder="Destino">
        </div>

        <div class="form-group col-md-4 col-xs-12">
          <input type="number" class="form-control" name="passageiros" placeholder="Nº Passageiros">
        </div>

        <div class="form-group col-md-12 col-xs-12">
        <textarea class="form-control" rows="5" type="text" name="mensagem" placeholder="Digite uma mensagem"></textarea>
        </div>

        <div class="col-md-12 text-center">
          <button type="submit" value="Send" class="btn btn-primary btt-orcamento">Solicitar Contato</button><br>
          <p id="my-form-status"></p>
        </div>

      </form>


      <script>
        window.addEventListener("DOMContentLoaded", function() {

          // get the form elements defined in your form HTML above

          var form = document.getElementById("my-form");
          var button = document.getElementById("my-form-button");
          var status = document.getElementById("my-form-status");

          // Success and Error functions for after the form is submitted

          function success() {
            form.reset();
            button.style = "display: none ";
            status.innerHTML = "Thanks!";
          }

          function error() {
            status.innerHTML = "Oops! There was a problem.";
          }

          // handle the form submission event

          form.addEventListener("submit", function(ev) {
            ev.preventDefault();
            var data = new FormData(form);
            ajax(form.method, form.action, data, success, error);
          });
        });

        // helper function for sending an AJAX request

        function ajax(method, url, data, success, error) {
          var xhr = new XMLHttpRequest();
          xhr.open(method, url);
          xhr.setRequestHeader("Accept", "application/json");
          xhr.onreadystatechange = function() {
            if (xhr.readyState !== XMLHttpRequest.DONE) return;
            if (xhr.status === 200) {
              success(xhr.response, xhr.responseType);
            } else {
              error(xhr.status, xhr.response, xhr.responseType);
            }
          };
          xhr.send(data);
        }
      </script>

  </div>
</div>
