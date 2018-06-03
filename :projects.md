---
layout: archive
title: Projects
permalink: /projects/ 
share: false
---
<div class="tiles">
{% for post in site.categories.project %}
  {% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->