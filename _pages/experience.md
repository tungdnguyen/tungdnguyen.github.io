---
layout: schedule
permalink: /experience/
title: experiences
description:
nav: 
nav_order: 
---
<h4> Professional </h4>
<br>
{% for item in site.data.experiences %}
{% if item.tag == "work" %}
{% assign work = item %}
<div class="row" >
    <div class="col-sm-3" style="text-align:right;"> <strong style="font-weight:500; font-size:18px; letter-spacing:1px; text-align:left;"> {{work.year}} </strong> </div>
    <div class="col-sm-9"> 
    <strong style="font-weight:500; font-size:18px; letter-spacing:1px;"> {{work.company}} </strong> <br>
    <em style="font-size:16px; letter-spacing:1px;"> {{work.title}} </em> <br>
    {% if work.advisors %}
    <em style="font-size:16px; letter-spacing:1px;"> Advisors: {{work.advisors}} </em> <br>
    {% endif %}
    <ul class="items" style="padding-left: 0;list-style-position:inside; font-size:16px;">
    {% for achievement in work.achievements %}
        <li> {{achievement}} </li>
    {% endfor %}
    </ul>
    </div>
</div>
{% endif %}
{% endfor %}

<h4> Teaching </h4> <br>
{% for item in site.data.experiences %}
{% if item.tag == "teaching" %}
{% assign work = item %}
<div class="row" >
    <div class="col-sm-3" style="text-align:right;"> <strong style="font-weight:500; font-size:18px; letter-spacing:1px; text-align:left;"> {{work.year}} </strong> </div>
    <div class="col-sm-9"> 
    <strong style="font-weight:500; font-size:18px; letter-spacing:1px;"> {{work.company}} </strong> <br>
    <em style="font-size:16px; letter-spacing:1px;"> {{work.title}} </em> <br>
    <ul class="items" style="padding-left: 0;list-style-position:inside;font-size:16px;">
    {% for achievement in work.achievements %}
        <li> {{achievement}} </li>
    {% endfor %}
    </ul>
    </div>
</div>
{% endif %}
{% endfor %}

<h4> Others </h4>
<br>
{% for item in site.data.experiences %}
{% if item.tag == "other" %}
{% assign work = item %}
<div class="row" >
    <div class="col-sm-3" style="text-align:right;"> <strong style="font-weight:500; font-size:18px; letter-spacing:1px; text-align:left;"> {{work.year}} </strong> </div>
    <div class="col-sm-9"> 
    <strong style="font-weight:500; font-size:18px; letter-spacing:1px;"> {{work.company}} </strong> <br>
    <em style="font-size:16px; letter-spacing:1px;"> {{work.title}} </em> <br>
    <ul class="items" style="padding-left: 0;list-style-position:inside;font-size:16px;">
    {% for achievement in work.achievements %}
        <li> {{achievement}} </li>
    {% endfor %}
    </ul>
    </div>
</div>
{% endif %}
{% endfor %}
