---
title: "CVLab - Members"
layout: gridlay
excerpt: "Computer Vision Lab: Members"
sitemap: false
permalink: /team/
---

## Faculty

{% assign selected_categories = "principal-investigator" | split:',' %}
{% include team_list.html %}

<br/>

## Graduate Students

{% assign selected_categories = "student" | split:',' %}
{% include team_list.html %}

<br/>

## Undergraduate Interns

{% assign selected_categories = "intern" | split:',' %}
{% include team_list.html %}

<br/>

## Alumni

<div id="alumni_list">

{% for person in site.data.alumni_members %}

<div class="member-row">

<h4>{{ person.name }}</h4>

{% if person.degree %}
<p><i>{{ person.degree }}</i></p>
{% endif %}

{% if person.current %}
<p><strong>Current Position:</strong> {{ person.current }}</p>
{% endif %}

{% if person.internship %}
<p class="member-section-title">Internship</p>

<ul class="member-detail-list">

{% for item in person.internship %}

<li>{{ item }}</li>

{% endfor %}

</ul>

{% endif %}

{% if person.publications %}

<p class="member-section-title">Publications</p>

<ul class="member-detail-list">

{% for item in person.publications %}

<li>{{ item }}</li>

{% endfor %}

</ul>

{% endif %}

</div>

{% endfor %}

</div>

<script>

$('body').on('click', '.member-list-item[data-href]', function(){

if (window.location.hash) {

window.location.hash = $(this).data('href');

} else {

window.location.href = $(this).data('href');

}

})

</script>