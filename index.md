---
layout: default
title: D6 Food Bulk Digital Portfolio
permalink: /
---

{% capture portfolio %}
{% include_relative README.md %}
{% endcapture %}
{{ portfolio | markdownify }}
