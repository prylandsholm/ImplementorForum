---
layout: default
title: Focus Groups
permalink: /focus-groups/
---

# Working Groups

The Implementor Forum is organized into working groups focused on specific aspects of semantic interoperability.

{% for group in site.data.working_groups %}
## {{ group.name }}

**Status:** {{ group.status }}

**Leader:** {{ group.leader }}

**Members:** {{ group.members }}

{{ group.description }}

**Contact:** [{{ group.contact }}](mailto:{{ group.contact }})

---

{% endfor %}

## Join a Working Group

Interested in joining one of our working groups? [Contact us](https://forms.office.com/e/N8n24DvrsV) to learn more.
