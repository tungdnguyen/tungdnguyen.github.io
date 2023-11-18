---
layout: post
title: harmonizing
date: 2015-10-20 11:12:00-0400
description: a crowdsourcing platform for creating community-based music (HackRice 2016’s winner)
tags: crowdsourcing crowdworking music signal-processing community-work social-computing
categories: 
related_posts: false
thumbnail:
importance: -3
---
<div class="row mt-3">
        {% include figure.html path="assets/img/harmonizing/harmonizing.gif" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
    UI design by <a href="https://www.behance.net/phtran">Phuong Tran</a>
</div>

<h3> Details </h3>
<div class="row" >
    <div class="col-sm-3" style="font-weight:300;"> 
    <strong> Authors:</strong> Tung Nguyen, Linh Hoang
    </div> 
</div>
<div class="row" >
    <div class="col-sm-6" style="font-weight:300;"> 
    <strong> Artifacts: <a target="_blank" rel="noopener noreferrer" href="https://github.com/tungdnguyen/harmonizing"> Code </a> | 
    <a target="_blank" rel="noopener noreferrer" href="https://devpost.com/software/harmonizing"> Hackrice </a> </strong>
    </div>
</div>
<hr>

A crowdsourcing platform which let users creating community-based songs. Users can choose to pariticipate in a designated part in a song: vocal, backup, instrumental. With provided guides, participants record their chosen part and upload it. Then, different harmony parts from different users will be selected randomly and merged into the final song.

<h3> Inspiration </h3>
As members of our high school's music club. Started as an Acapella club, without professional help, academic training or any advanced equipment, we always struggled to find the best way for our club members to harmonize together.

<h3> How we built it </h3>
We use node.js to create the server and Express as the framework. Then, we use Multer, a node.js middleware to allow users to upload their record. Lastly, we use HTML to play the tracks and merge them together.

<br>
<p align="center"><iframe width="560" height="315" src="https://www.youtube.com/embed/D-2Fi_42aQo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></p>
<div class="caption">
    Participate in community-based songs
</div>