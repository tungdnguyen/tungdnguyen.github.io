---
layout: default
permalink: /cv/
title: cv
nav: true
nav_order: 2
redirect_to:
---

<!-- ///assets/pdf/cv.pdf -->
{% assign pdf_path = "assets/pdf/cv.pdf" | relative_url %}
<object data="{{pdf_path | relative_url}}" width="850" height="900" type="application/pdf"></object>