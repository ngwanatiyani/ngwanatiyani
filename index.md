---
layout: default
title: D6 Food Bulk Digital Portfolio
description: Agile project evidence and reflections by Tiyani Ngwana
permalink: /
---

{% capture portfolio %}
{% include_relative README.md %}
{% endcapture %}
{{ portfolio | markdownify }}
