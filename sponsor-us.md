---
layout: page
title: Sponsor Us
---

Support Andover Central High School Robotics by empowering the next generation of engineers and innovators. Every donation directly fuels the JagWire Robotics (Team 9626) mission! We are proud to represent the Andover Kansas community in the high-stakes world of FIRST Robotics. Your support helps us move toward our goals by providing raw materials, motors, and sensors to keep our robot running, essential 'brain food' to keep our students energized during marathon build sessions, and the travel funds needed to reach our FIRST Robotics Competitions. Help us keep the gears turning - every little bit helps us gear up for greatness!

{% include button.html
    href="https://hcb.hackclub.com/donations/start/9626-jagwires"
    text="Donate to Team 9626"
    open_new_tab=true
%}

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
