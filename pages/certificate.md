---
layout: default
title: Certificates
permalink: /certificates/
weight: 3
---
<div class="card-columns m-3 mt-5">

{% for project in site.data.certificate %}
    <div class="wow animated fadeIn" data-wow-delay=".15s">
    <a href="{{ project.external_url }}" class="project card text-themed"  target="_blank">
        <img id="{{ project.name | slugify }}-img" class="card-img-top" src="{{ project.image }}" alt="{{ project_name }}" />
        <div class="card-body">
        <h5 id="{{ project.name | slugify }}-name" class="card-title">
            {{ project.name }}
        </h5>
        <p id="{{ project.name | slugify }}-desc" class="card-text">{{ project.provider }}<br>{{ project.date }}</p>
        <p id="{{ project.name | slugify }}-tools" class="card-text">
            ID Credential: {{ project.credential }}
        </p>
        </div>
    </a>
    </div>
{% endfor %}

</div>
