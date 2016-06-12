---
layout: projects
title: 项目
permalink: /Projects/
---
{% for category in site.categories %}
{% if category.first == 'Project' %}
<h4>汉化库里存在{{ category | last | size }}个项目</h4>
{% endif %}
{% endfor %}