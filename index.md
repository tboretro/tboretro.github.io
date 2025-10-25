# My Collection

This is just a space to keep track of my collection of retro computer stuff

## Home Computers

{% assign started_items = site.home_computers | where: "progress", "started" %}
{% assign done_items = site.home_computers | where: "progress", "done" %}
{% assign filtered = started_items | concat: done_items %}
{% assign sorted_home_computers = filtered | sort: "released" %}
<ul>
{% for item in sorted_home_computers %}
  <li>
  <a href="{{ item.url | relative_url }}">{{ item.title }} (released in {{ item.released }})</a>
  {% if item.documented != 'done' %} <em> — documentation in progress</em> {% endif %}
  </li>
{% endfor %}
</ul>

## IBM Compatible

{% assign sorted_ibm_compatibles = site.ibm_compatibles | sort: "released" | sort: "class" %}
{% for item in sorted_ibm_compatibles %}
  <a href="{{ item.url | relative_url }}">{{ item.title }} ({{ item.class }}-class, released in {{ item.released }})</a>
  {% if item.documented != 'done' %} <em> — documentation in progress</em> {% endif %}
  <br>
{% endfor %}

## IBM Portables

{% assign started_items = site.ibm_portables | where: "progress", "started" %}
{% assign done_items = site.ibm_portables | where: "progress", "done" %}
{% assign filtered = started_items | concat: done_items %}
{% assign sorted_ibm_portables = filtered | sort: "released" | sort: "class" %}
<ul>
{% for item in sorted_ibm_portables %}
  {% assign display_text = item.title %}
  {% if item.class %}
    {% assign display_text = display_text | append: " (" | append: item.class | append: "-class, released in " | append: item.released | append: ")" %}
  {% else %}
    {% assign display_text = display_text | append: " (released in " | append: item.released | append: ")" %}
  {% endif %}
  <li>
  {% if item.documented == "stub" %}
    {{ display_text }} <em>— documentation pending</em>
  {% else %}
    <a href="{{ item.url | relative_url }}">{{ display_text }}</a>
    {% if item.documented != "done" %} <em>— documentation in progress</em>{% endif %}
  {% endif %}
  </li>
{% endfor %}
</ul>

## Game Consoles

TODO

## Interals / To-Dos

* Add all devices

* Maybe add hifi setup

* Status of 
** progress: pile, started, done
** documented: stub, started, done

* Add photo gallery (see ChatGPT chat for ideas how to)
