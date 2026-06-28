---
title: Publications
permalink: /publications/
layout: default
---

# Publications

{% assign pubs_by_year = site.data.publist | group_by: "year" | sort: "name" | reverse %}

{% for year_group in pubs_by_year %}

## {{ year_group.name }}

{% for pub in year_group.items %}

<div class="pub-row">

{% if pub.image %}
<div class="pub-img">
  <img src="{{ site.baseurl }}/images/publications/{{ pub.image }}" alt="{{ pub.title }}">
</div>
{% endif %}

<div class="pub-content">

### {{ pub.title }}

<p class="pub-authors">
{% for author in pub.authors %}
{% if author.name == "Donghyeon Cho" %}
<strong>{{ author.name }}</strong>
{% else %}
{{ author.name }}
{% endif %}
{% unless forloop.last %}, {% endunless %}
{% endfor %}
</p>

<p class="pub-venue">
{% if pub.type == "Conference" %}
<span class="pub-type conference-type">Conference</span>
{% elsif pub.type == "Journal" %}
<span class="pub-type journal-type">Journal</span>
{% endif %}

<span class="venue-name">{{ pub.venue }}</span>

{% if pub.note %}
<span class="pub-note">{{ pub.note }}</span>
{% endif %}
</p>

{% if pub.paper or pub.project or pub.code %}
<div class="publication-links">
{% if pub.paper %}
<a href="{{ pub.paper }}" target="_blank">Paper</a>
{% endif %}
{% if pub.project %}
<a href="{{ pub.project }}" target="_blank">Project</a>
{% endif %}
{% if pub.code %}
<a href="{{ pub.code }}" target="_blank">Code</a>
{% endif %}
</div>
{% endif %}

</div>

</div>

---

{% endfor %}

{% endfor %}