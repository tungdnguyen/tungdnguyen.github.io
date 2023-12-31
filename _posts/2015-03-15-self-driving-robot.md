---
layout: post
title: Self-driving NASA Mars Miner
date: 2018-10-20 11:12:00-0400
description: Automated control system for 2018 NASA Robotic Mining Competition 
tags: robotic computer-vision nasa mining kinect self-driving
categories:
related_posts: false
thumbnail:
importance: -4
---
<h3> Details </h3>
<div class="row" >
    <div class="col-sm-3" style="font-weight:300;"> 
    <strong> Authors:</strong> Tung Nguyen, Scarlett Hawk IIT
    </div> 
</div>
<div class="row" >
    <div class="col-sm-3" style="font-weight:300;"> 
    <strong>Artifacts: <a target="_blank" rel="noopener noreferrer" href="https://github.com/tungdnguyen/nasa-robot"> Code </a> </strong>
    </div>
</div>
<hr>

[LUNABOTICS](https://www.nasa.gov/press-release/nasa-announces-robotic-mining-competition-0) is an Artemis Student Challenge to educate college students on NASA Systems Engineering. Participating teams design and build a prototype robot for long-term human presence on Mars. During the simulation, robots must overcome regolith simulants, resources, weight, size, and remote/autonomous operations.

<div class="row mt-3">
        {% include figure.html path="assets/img/robot/team.jpeg" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
    IIT team at Kenedy Space Center.
</div>

I was part of Illinois Tech's automation team. We worked closely with fellow mechanical and electrical engineers to build a self-maneuvered system for the robot.

Our main achievements: 

  - Created a neural obstacle detection system using Kinect's depth sensors, LibFreenect, and OpenCV
  - Integrated LIDAR and Adafruit Capacitive touch sensors to develop a fully automated robot maneuvering system
  - Designed manual control system fall-back
  - Successfully ran self-driving test drives on real mining evironment.

<p align="center"><iframe width="560" height="315" src="https://www.youtube.com/embed/5FNd6rH5uJ4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></p>
<div class="caption">
    Proof of life for mining robot
</div>

**Personal Note**: My desire to participate in this competition stemmed from watching [Vietnam Robocon](https://www.youtube.com/watch?v=FI2VTcHbP4Q), a robot contest for college students across the country, during my childhood. Vietnam's tremendous effort in promoting STEM competitions/programs on national television during the 2000s incited my passion for STEMs. I hope Vietnamese govenment and education organizations can continue their supports for these programs in the future.

<p align="center"><iframe width="560" height="315" src="https://www.youtube.com/embed/m5mSOAzYh6s" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></p>
<div class="caption">
    Vietnam Robocon team claimed champion in Asia-Pacific Robot Contest in 2004. <br> The first of our 6 champion titles during the competion's 20 years history.
</div>

{% assign next_project = "projects/2018/league-predict/" | relative_url %}
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