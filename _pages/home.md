---
title: "CVLab - Home"
layout: homelay
excerpt: "Computer Vision Lab at Hanyang University."
sitemap: false
permalink: /
---

We are the **Computer Vision Lab (CVLab)** at Hanyang University. Our research focuses on computer vision, video understanding, image restoration, 3D vision, generative AI, and multimodal learning. We aim to develop trustworthy, efficient, and scalable visual intelligence systems that can understand, restore, reconstruct, and generate visual content.

<div markdown="0" id="carousel" class="carousel slide" data-ride="carousel" data-interval="3000" data-pause="hover" >
    <ol class="carousel-indicators">
        <li data-target="#carousel" data-slide-to="0" class="active"></li>
        <li data-target="#carousel" data-slide-to="1"></li>
        <li data-target="#carousel" data-slide-to="2"></li>
    </ol>

    <div class="carousel-inner" markdown="0">
        <div class="item active">
            <img src="{{ site.url }}{{ site.baseurl }}/images/home-slider/20260624.png" alt="CVLab Slide 1" />
        </div>
        <div class="item">
            <img src="{{ site.url }}{{ site.baseurl }}/images/home-slider/20260624_2.png" alt="CVLab Slide 2" />
        </div>
        <div class="item">
            <img src="{{ site.url }}{{ site.baseurl }}/images/home-slider/20260624_3.png" alt="CVLab Slide 3" />
        </div>
    </div>

    <a class="left carousel-control" href="#carousel" role="button" data-slide="prev">
        <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
    </a>

    <a class="right carousel-control" href="#carousel" role="button" data-slide="next">
        <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
    </a>
</div>

## Latest News (from 2024.3)

<ul class="latest-news-list">
{% for article in site.data.news %}
  <li>
    <span class="latest-news-date">{{ article.date }}</span>
    <span class="latest-news-body">– {{ article.headline }}</span>
  </li>
{% endfor %}
</ul>