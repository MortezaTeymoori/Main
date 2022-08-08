---
layout: page
permalink: /publications/
title: Publications
description: My latest peer-reviewed publications and conferences
paperyears: [2022, 2017 , 2016]
Proceedingyears: [2022, 2019, 2016 ,2014, 2012]
nav: true
---

<div class="publications">
<h1> Peer-Reviewed </h1>
{% for y in page.paperyears %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @article[year={{y}}]* %}
{% endfor %}

</div>


<div class="publications">
<h1> Conferences </h1>
{% for x in page.Proceedingyears %}
  <h2 class="year">{{x}}</h2>
  {% bibliography -f papers -q @inproceedings[year={{x}}]* %}
{% endfor %}

</div>