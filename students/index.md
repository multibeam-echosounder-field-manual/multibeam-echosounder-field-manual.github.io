---
layout: home
permalink: students
title: "Current Students"
excerpt: ""
image:
  feature: banner6.jpg
---
<div class="tiles">
  <h2 class="post-title">PhD Candidates</h2>
{% for post in site.categories.phd-students %}
	{% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->


<div class="tiles">
  <h2 class="post-title">Masters and Honours students</h2>
{% for post in site.categories.masters-students %}
	{% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->