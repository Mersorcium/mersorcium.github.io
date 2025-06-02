---
layout: category
title: Events
---

{% for event in site.data.seminar %}
---
**{{ event.type }}**

## {{ event.title }}

{% if event.speaker %}
*Speaker*: {{ event.speaker }}
{% endif %}

{% if event.affiliation %}
*Affiliation*: {{ event.affiliation }}
{% endif %}

{% if event.utc %}
*Time*: {{ event.utc }}
{% endif %}

{% if event.youtube %}
*Seminar Recording*: [Go To Mersorcium YouTube Channel]({{ event.youtube }})
<iframe width="560" height="315" src="{{ event.youtube | replace: 'watch?v=', 'embed/' }}" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
{% endif %}

{% if event.poster %}
![Alt text]({{ '/posters/' | append: event.poster | relative_url }} "{{ event.poster }}")
{% endif %}
{% endfor %}
