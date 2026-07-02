---
title: "CVLab - Members"
layout: gridlay
excerpt: "Computer Vision Lab: Members"
sitemap: false
permalink: /team/
---

# Members

<button class="member-toggle" data-target="#professor-section">Professor</button>

<div id="professor-section" class="member-section">

{% assign selected_categories = "principal-investigator" | split:',' %}
{% include team_list.html %}

</div>

<button class="member-toggle" data-target="#students-section">Students</button>

<div id="students-section" class="member-section" style="display:none;">

### Graduate Students

{% assign selected_categories = "student" | split:',' %}
{% include team_list.html %}

<br/>

### Undergraduate Interns

{% assign selected_categories = "intern" | split:',' %}
{% include team_list.html %}

</div>

<button class="member-toggle" data-target="#alumni-section">Alumni</button>

<div id="alumni-section" class="member-section" style="display:none;">

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

});

$('.member-toggle').on('click', function(){

  var target = $(this).data('target');

  $('.member-section').not(target).slideUp();

  $(target).slideToggle();

});

</script>