---
layout: page
title: Participants
---

<!--[![Group photo]({{ site.baseurl }}/photos/groupphoto-gapdays2017-spring_thumb.jpg "Group photo")]({{ site.baseurl }}/photos/groupphoto-gapdays2017-spring.jpg)-->

<ol>
{% for p in site.data.participants %}
  <li>
    {% if p.url != null %} <a href="{{p.url}}">{% endif %}
    <strong>{{ p.name }}</strong>
    {% if p.url != null %} </a>{% endif %}
    {% if p.affiliation != null %} ({{ p.affiliation }}){% endif %}
    {% if p.links != null %}
        {% for item in p.links %}
            <a href="{{ item[1] }}">({{ item[0] }})</a>
        {% endfor %}
    {% endif %}
    <br/>
      {% if p.talk != null %} Talk: {{ p.talk }}{% endif %}
  </li>
{% endfor %}
</ol>

{% if site.data.feedback.size > 0 %}

<ul>
{% for p in site.data.feedback %}
  <li>
    <strong>{{ p.name }}</strong>
    {% if p.package != null %} (author of {{ p.package }}){% endif %}
    <br/>
    {% if p.feedback != null %} {{ p.feedback }}{% endif %}
  </li>
{% endfor %}
</ul>

{% endif %}
