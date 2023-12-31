---
layout: post
title: Competitive Gaming Matches Prediction
date: 2018-10-20 11:12:00-0400
description: utilize big data technologies to predict outcomes of League of Legends matches
tags: machine-learning, spark, cosmos-db, azure, cloud
categories: 
related_posts: false
thumbnail:
importance: -5
---

<p align="center"><iframe width="560" height="315" src="https://www.youtube.com/embed/KlYK1G1af1s" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe> </p> <br>


{% assign pdf_path = "assets/pdf/league_predict.pdf" | relative_url %}
<h3> Details </h3>
<div class="row" >
    <div class="col-sm-6" style="font-weight:300;"> 
    <strong> Authors:</strong> Tung Nguyen, James Guerrera-Sapone
    </div> 
</div>
<div class="row" >
    <div class="col-sm-3" style="font-weight:300;"> 
    <strong> Artifacts: <a target="_blank" rel="noopener noreferrer" href="https://github.com/tungdnguyen/league_of_legends_predict"> Code </a> | 
    <a target="_blank" rel="noopener noreferrer" href="{{ pdf_path | relative_url }}"> Paper </a> </strong>
    </div>
</div>
<br>

League of Legends (LoL) is one of the most popular online video games in the world. A game match contains 2 teams of 5 players, and each player controls a character with a unique set of abilities. This means that there are many factors which can influence which team wins. There are influences both from the characters being used as well as the individual skill of the players. We have created a data pipeline using Microsoft Azure to process data from the LoL developer API and developed a machine learning model to predict the winning team based both on the player and character compositions of each team.

**Notable work**
- Created a data pipeline to collect data from League of Legends Developer API to store on Azure Cosmos DB.
- Performed data processing and built a Logistic Regression model to predict outcome of each game match on Apache Spark (Azure HDInsight and Spark ML).
- Implemented the prediction model on an interactive web application.

<div class="row mt-3">
        {% include figure.html path="assets/img/league/pipeline.png" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
    Pipeline Overview
</div>

<div class="row mt-3">
        {% include figure.html path="assets/img/league/data_collection.png" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
    How League of Legends data is collected
</div>

<h4> Paper </h4>
<!-- ///assets/pdf/cv.pdf -->
{% assign pdf_path = "assets/pdf/league_predict.pdf" | relative_url %}
<object data="{{pdf_path | relative_url}}" width="850" height="900" type="application/pdf"></object>

{% assign next_project = "projects/2018/image-video-transform/" | relative_url %}
<div class="row" style="margin-top: 20px;" >
    <div class="col-sm-9" style="font-weight:300;"> 
    <a class="buttons" href="{{next_project}}"> next project 👉 </a>
    </div>
</div>
{% assign blog = "blog/" | relative_url %}
<div class="row" style="margin-top: 3px;">
    <div class="col-sm-9" style="font-weight:300;"> 
    <a class="buttons" href="{{blog}}"> 👈 back to list </a>
    </div>
</div>