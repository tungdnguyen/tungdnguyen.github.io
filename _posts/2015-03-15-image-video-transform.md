---
layout: post
title: Image and Real-time Video Style Transfer
date: 2015-10-20
description: Image and video style transferring using Deep Neural Network
tags: style-transfer computer-vision
categories:
related_posts: false
thumbnail: assets/img/transfer/transfer_logo.png
importance: 4
---
{% assign pdf_path = "assets/pdf/style_transfer.pdf" | relative_url %}
<h3> Details </h3>
<div class="row" >
    <div class="col-sm-6" style="font-weight:300;"> 
    <strong> Authors:</strong> Tung Nguyen, Tuan Tran
    </div> 
</div>
<div class="row" >
    <div class="col-sm-3" style="font-weight:300;"> 
    <strong>Artifacts: <a target="_blank" rel="noopener noreferrer" href="https://github.com/tungdnguyen/style-transfer"> Code </a> | 
    <a target="_blank" rel="noopener noreferrer" href="{{ pdf_path | relative_url }}"> Paper </a> </strong>
    </div>
</div>
<hr>

The term “style transfer” has been coined to describe such problem of training machines to “roughly” mimic human’s ability to interplay different image styles to create unique and complex visual experiences. To put it simply, style transfer is the problem of recomposing images in the style of other images; that is, given an original image, and a second image with specific style, we would like to create a new image with the style of the second image applied to the content of the original image. Even though it does not fully explain how humans create unique art pieces, style transfer is definitely the right logical step towards solving the more complex problem of understanding how humans create and perceive arts.

We’ll use the algorithm introduced by Gatys et al. as the basis of this project. With a pre-trained VGG model and a clever loss setup, Gatys et al. algorithm is able to achieve high-quality results and also provides insights into image representations learned by Convolutional Neural Networks and empirically demonstrate CNNs’ potential for high level image synthesis and manipulation [1]. We’ll also implement an extension of this method proposed by Johnson et al. in order to speed up styling process. This extension allows for fast real time style transfer.

<div class="row mt-3">
        {% include figure.html path="assets/img/transfer/Results.png" class="img-fluid rounded z-depth-1" %}
</div>
<div class="row mt-3">
        {% include figure.html path="assets/img/transfer/Results_2.png" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
    Results images
</div>


To obtain a style representation from the style input image, we construct a Gram matrix which can be built on top of the feature map in any layer of VGG16. The Gram matrix consists of the correlations between different filter responses, and thus captures the texture information of an image. 

The basic intuition behind Gram matrix is that by multiplying elements of each combination of feature maps together, we are essentially checking if the elements “overlap” at their location in the image. The summation then discards all the information’s spatial relevance.


<div class="row mt-3">
        {% include figure.html path="assets/img/transfer/training_1.png" class="img-fluid rounded z-depth-1" %}
</div>
<div class="row mt-3">
        {% include figure.html path="assets/img/transfer/training_2.png" class="img-fluid rounded z-depth-1" %}
</div>
<div class="caption">
    Training
</div>

<h4> Paper </h4>
<!-- ///assets/pdf/cv.pdf -->
{% assign pdf_path = "assets/pdf/style_transfer.pdf" | relative_url %}
<object data="{{pdf_path | relative_url}}" width="850" height="900" type="application/pdf"></object>