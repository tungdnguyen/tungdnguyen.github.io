---
layout: post
title: Spotify’s social recommender
date: 2019-10-20 11:12:00-0400
description: Spotify’s music recommendation based on users’ followers' network
tags: social-computing recommendation-system collaborative-filtering followers-network community-detection machine-learning nlp social-network-analysis
categories: 
related_posts: false
thumbnail: assets/img/spotify/logo.png
importance: 2
---
{% assign pdf_path = "assets/pdf/spotify.pdf" | relative_url %}
<div class="row" >
    <div class="col-sm-6" style="font-weight:300;"> 
    <strong> Authors:</strong> Tung Nguyen, Tuan Tran, Paolo Ratti
    </div> 
</div>
<div class="row" >
    <div class="col-sm-6" style="font-weight:300;"> 
    <strong> Advisor:</strong> Aron Culotta - <a href="http://tapilab.github.io/"> TAPILAB </a>
    </div> 
</div>
<div class="row" >
    <div class="col-sm-3" style="font-weight:300;"> <strong> Artifacts: </strong><a href="{{ pdf_path | relative_url }}"> Presentation </a>
    </div>
</div>
<hr>

<h3> Details </h3>

Spotify is one of the biggest music streaming service. The service provides social feature which allow an user to follow other users' music playlist. The community can also build a shared playlist together. Using Spotify users’ playlists and their corresponding Twitter’s
networks, we want to understand how friends (and followers) influence users’
music taste. Consequently, we aim to build a music recommender based on user's follower network.

<h4> Approach </h4>

- Collected Spotify user's playlist and friends network. We scraped Twitter Streaming API for public tweets contains #NowPLaying hashtag, which is a Spotify specific tag. We consider these users to be highly influential on their followers' music predilection.
- Created a follower network between collected users.
- Created users' taste profiles based on their playlists characteristics: acousticness, danceability, energy, speechiness,valence, acousticness.
- Incorporated Last.FM's song tags to analyze users's music listening habits (diversity, genre, etc.,)
- Built a collaborative-filtering recommender which predict songs an user most likely listen to next based on their friends' profiles.

<h4> Results </h4>

- Achieved **0.77 AUC** on 6-fold cross-validation in our next-song prediction model. A **40% increase** from baseline Spotify's current recommender (0.46 AUC).
- Collected ~5k Spotify users' playlist and following/followers.
- For 1000 users with taste profiles,  14% of the songs appeared in a follower/friend playlist will appeared on the seed users'playlist later on.
-  41% of the friends/followers for a seed users will share at least a common song with the seed user.
-  Understand user listening habits and playlist diversity using text tokenization, PCA and cosine similarity
-  See strong correlation between of Spotify's current recommender on user listening habits.


<div class="row mt-6-9">
        {% include figure.html path="assets/img/spotify/music_habit.png" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
    User listening habit over time: cosine similarity between newly created playlist with existing playlists
</div>

<div class="row mt-6-9">
        {% include figure.html path="assets/img/spotify/spotify_recommend.png" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
    Correlation between Spotify recommendations and user playlist (Our baseline)
</div>

<div class="row mt-6-9">
        {% include figure.html path="assets/img/spotify/auc.png" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
    Collaborative-filtering recommender AUC on 6-fold cross validation.<br>
    Our model yields <strong>0.76 AUC</strong>, a <strong>40% increase</strong> from baseline 0.46 AUC.
</div>