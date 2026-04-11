---
layout: page
title: Sponsor Us
---

Support Andover Central High School Robotics. Empower the next generation of engineers and innovators. Your sponsorship directly funds our robot builds, competition travel, and STEM outreach programs. Ready to Partner with us? Become a sponsor today!

{% include card.html
    image="assets/images/2026-city-of-fountains-regional/55191192597_c7bcdf48cf_o.jpg"
    alt="Team 9626 Photo"
%}

{% for tier in site.data.sponsors.levels %}
## {{ tier.name | capitalize }} Sponsor - {{ tier.amount }}

  {% for benefit in tier.schedule %}
  - {{ benefit }}
  {% endfor %}

{% endfor %}
