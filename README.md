# My Collection

This is just a space to keep track of my collection of retro computer stuff

## Home Computers

{% assign started_items = site.home_computers | where: "progress", "started" %}
{% assign done_items = site.home_computers | where: "progress", "done" %}
{% assign filtered = started_items | concat: done_items %}
{% assign sorted_home_computers = filtered | sort: "released" %}
<ul>
{% for item in sorted_home_computers -%}
  <li>
  <a href="{{ item.url | relative_url }}">{{ item.title }} (released in {{ item.released }})</a>
  {% if item.documented != 'done' %} <em> — documentation in progress</em> {% endif %}
  </li>
{%- endfor %}
</ul>

## IBM Compatible

{% assign sorted_ibm_compatibles = site.ibm_compatibles | sort: "released" | sort: "class" %}
{% for item in sorted_ibm_compatibles %}
  <a href="{{ item.url | relative_url }}">{{ item.title }} ({{ item.class }}-class, released in {{ item.released }})</a>
  {% if item.documented != 'done' %} <em> — documentation in progress</em> {% endif %}
  <br>
{% endfor %}

## IBM Portables

{% assign sorted_ibm_portables = site.ibm_portables | sort: "released" | sort: "class" %}
{% for item in sorted_ibm_cosorted_ibm_portablesmpatibles %}
  <a href="{{ item.url | relative_url }}">{{ item.title }} ({{ item.class }}-class, released in {{ item.released }})</a>
  {% if item.documented != 'done' %} <em> — documentation in progress</em> {% endif %}
  <br>
{% endfor %}

## Game Consoles

TODO

## Interals / To-Dos

* Add all devices

* Maybe add hifi setup

* Status of 
** progress: pile, started, done
** documented: stub, started, done

* Add photo gallery (see ChatGPT chat for ideas how to)
