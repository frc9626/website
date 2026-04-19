---
layout: page
title: Sponsors
---

<link rel="stylesheet" href="{{ '/assets/css/main.css' | relative_url }}">

<style>
  .post-title { display: none; }
</style>

# Thank You to Our Sponsors

We are incredibly grateful for the generous support of our sponsors. Your contributions provide the essential resources and opportunities that drive our success and empower our team to reach new heights.

Thank you for investing in our mission and being a vital part of our community!

<div class="sponsors-container">
  {% for tier in site.data.sponsors.levels %}
    {% if tier.members.size > 0 %}
      <section class="sponsor-tier tier-{{ tier.name }}">
        <h2>{{ tier.name | capitalize }} Sponsors</h2>
        
        <div class="sponsor-grid">
          {% for member in tier.members %}
            <div class="sponsor-card">
              {% if member.url %}
                <a href="{{ member.url }}" target="_blank" rel="noopener">
              {% endif %}

                {% comment %} Determine which logo to use {% endcomment %}
                {% assign logo_file = member.logo | default: site.data.sponsors.config.default_logo %}
                
                <img src="{{ site.data.sponsors.config.image_base_path | append: logo_file | relative_url }}" alt="{{ member.name }}" class="sponsor-logo">
                
                <div class="sponsor-info">
                  <span class="sponsor-name">{{ member.name }}</span>
                  {% if member.icon %}
                    <img src="/assets/images/icons/{{ member.icon }}" class="contact-icon" alt="Contact">
                  {% endif %}
                </div>

              {% if member.url %}
                </a>
              {% endif %}
            </div>
          {% endfor %}
        </div>
      </section>
    {% endif %}
  {% endfor %}
</div>
