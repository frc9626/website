---
layout: page
title: Contact
---

<style>
    .social-links-vertical {
        display: flex;
        flex-direction: column; /* Stacks items vertically */
        align-items: flex-start; /* Aligns items to the left */
        gap: 15px;
        padding: 20px;
    }

    .social-link-item {
        display: flex;
        align-items: center; /* Aligns icon and text vertically centered */
        gap: 10px;
        text-decoration: none;
    }

    .social-link-item img.contact-icon {
        width: 32px; /* Adjusted size for better layout with text */
        height: 32px;
        object-fit: contain;
    }

    .social-username {
        font-size: 1.1em;
        color: #333;
    }
</style>

<div class="wrapper">
  <div class="footer-col-wrapper">
    <div class="social-links-vertical">
      {% for social in site.data.social-media %}
        {% assign platform = social[1] %}
          <a href="{{ platform.url }}" class="social-link-item" target="_blank" rel="noopener noreferrer">
            <img class="contact-icon" 
                 src="{{ 'assets/images/social-icons/' | append: platform.icon | relative_url }}" 
                 alt="{{ social[0] }}">
            <span class="social-username">{{ platform.username }}</span>
          </a>
      {% endfor %}
    </div>
  </div>
</div>