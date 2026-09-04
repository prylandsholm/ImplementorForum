---
layout: default
title: Events
permalink: /events/
---

# Events

{% if site.data.events %}
## Upcoming Events

{% for event in site.data.events %}
### {{ event.title }}

**Date:** {{ event.date | date: "%B %d, %Y" }}

**Location:** {{ event.location }}

{{ event.description }}

{% if event.registration_link %}
[Register now]({{ event.registration_link }})
{% endif %}

---

{% endfor %}
{% else %}
## No Events Scheduled

Check back soon for upcoming events. [Subscribe for updates](https://forms.office.com/e/N8n24DvrsV).
{% endif %}
