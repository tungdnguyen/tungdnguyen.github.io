---
layout: post
title: Music Genre Conversion
date: 2019-10-20 11:12:00-0400
description: using Fast Fourier Transform and neural net for music genre translation
tags: adversarial-network signal-processing music-generation machine-learning deep-learning
categories: 
related_posts: false
thumbnail:
importance: -2
---
<div class="row" >
    <div class="col-sm-6" style="font-weight:300;"> 
    <strong> Authors:</strong> Tung Nguyen
    </div> 
</div>
<div class="row" >
    <div class="col-sm-6" style="font-weight:300;"> 
    <strong> Advisor:</strong> Edward M. Reingold
    </div> 
</div>
<hr>

<h3> Details </h3>

Fast Fourier Transform has been the backbone of signal processing. Under professor Edward M. Reingold, I conducted an independent research study on Fast Fourier Transform and its application on audio processing. 

The goal of the project is to create a music genre-conversion model. Given an audio file, the model would algorithmatically modify the song to a different genre. The problem statement would then be: 

```
Create a Folk version of Nirvana's Smells Like Teen Spirit using Deep Neural Network
```

<h4> Approach </h4>
- Created an adversarial network including one conversion model and an adversarial music genre classifier.
- Using Short Time Fourier Transform, vectorized audio files in [GTZAN Dataset](https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification).
- Using vectorize audio as input, created a music genre classification model.
- Trained a music generation model for each genre using GTZAN as our training data. These models are called `genre blueprints`.

<h4> Results </h4>
Folk -> Rock conversion on Rock blueprints achieved **60% accuracy** on genre classifier.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include audio.html path="assets/audio/sample_folk_song.mp3" controls=true %}
    </div>
</div>
<div class="caption">
    Original Folk song
</div>
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include audio.html path="assets/audio/folk_x_average_rock_footprint.mp3" controls=true %}
    </div>
</div>
<div class="caption">
    An example of Folk -> Rock
</div>
{% assign next_project = "projects/2015/harmonizing/" | relative_url %}
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