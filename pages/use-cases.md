---
layout: default
title: Use Cases
permalink: /use-cases/
---

# Industry Use Cases

Explore real-world implementations of semantic interoperability across various industries.

## Featured Use Cases

{% for use_case in site.data.use_cases %}
### {{ use_case.title }}

**Organization:** {{ use_case.organization }}

**Industry:** {{ use_case.industry }}

{{ use_case.description }}

[Learn more]({{ use_case.link }})

---

{% endfor %}

## Share Your Use Case

If your organization has implemented semantic interoperability solutions, we'd love to feature your story. [Submit a use case](https://forms.office.com/e/N8n24DvrsV).
