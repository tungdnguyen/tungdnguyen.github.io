---
layout: schedule
permalink: /experience/
title: experiences
description:
nav: true
nav_order: 3
---
{% assign current_module = 0 %}
{% assign skip_classes = 0 %}
{% assign prev_date = 0 %}

{% for item in site.data.experiences %}
{% if item.year %}
{% assign work = item %}
{% endif %}

<div class="row" >
    <div class="col-sm-3"> <strong style="font-weight:500; font-size:18px; letter-spacing:1px;"> {{work.year}} </strong> </div>
    <div class="col-sm-9"> 
    <strong style="font-weight:500; font-size:18px; letter-spacing:1px;"> {{work.company}} </strong> <br>
    <em>{{work.title}}</em> <br>
    <ul class="items" style="padding-left: 0;list-style-position:inside;">
    {% for achievement in work.achievements %}
        <li> {{achievement}} </li>
    {% endfor %}
    </ul>
    </div>
</div>

{% endfor %}
