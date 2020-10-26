---
layout: page
permalink: "/dicas-de-viagens.html"
title: "Dicas de Viagens"
description: 'Os melhores roteiros e mais procurados destinos para sua escolha.'
---
<div class="row">

  {% for post in site.posts %}
  <div class="card col-md-3 col-sm-12 col-xs-12 wow fadeInDown">
    <img class="card-img-top img-responsive" src="{{ post.image }}" alt="Imagem de capa do card">
    <div class="card-body">
      <h4 class="card-title">
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
      </h4>
      <p class="card-text">{{ post.description }}</p>
      <div class="col-md-12 col-sm-12 col-xs-12">
      <a href="javascript:alert('Em Breve')" style="color:#FFFFFF; width:100%;" class="btn btn-primary">
      <i class="fas fa-plus"></i> Abrir destino</a>
    </div>
    </div>
  </div>
  {% endfor %}




</div> <!-- final de artigos container -->
