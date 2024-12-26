---
layout: default
title: Peñarol
author: PEÑAROLPRESS 1891
---

<div class="container-fluid bg-color4b4a42 title-wrapper inline w-100 mt-5 mb-2">
    <h1 class="float-start inline custom ms-2">noticias</h1>
    <span class="float-end inline me-2">{% include brand.html %}</span>
</div>

<div class="container-fluid">
    <div class="row">
    {% for post in site.categories.Penarol limit: 9 %}       
        <div class="col-md-4 mt-3 mb-3">
            <div class="card align-items-center justify-content-center">
                <img src="{{ post.image2 }}" width="100%">
                <div class="card-body">
                    <span class="archivo700">
                        {{ post.title }}
                    </span>
                    <p class="text-muted post-date archivo700">{{ post.date_es }}</p>
                    <a href="{{ site.url | relative_url }}/{{ post.url }}">
                        <img src="{{ site.url }}/images/veronline.png" width="120px">
                    </a>
                </div>
            </div>
        </div>
    {% endfor %}    
    </div>
</div>

