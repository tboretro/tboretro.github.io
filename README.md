# My Collection

This is just a space to keep track of my collection of retro computer stuff

## Home Computers

{% assign sorted_home_computers = site.home_computers | sort: "released" %}
{% for item in sorted_home_computers %}
  <a href="{{ item.url | relative_url }}">{{ item.title }} (released in {{ item.released }})</a>
  {% if item.documented != 'done' %} <em> — documentation in progress</em> {% endif %}
  <br>
{% endfor %}

## IBM Compatible

{% assign sorted_ibm_compatibles = site.ibm_compatibles | sort: "released" | sort: "class" %}
{% for item in sorted_ibm_compatibles %}
  <a href="{{ item.url | relative_url }}">{{ item.title }} ({{ item.class }}-class, released in {{ item.released }})</a>
  {% if item.documented != 'done' %} <em> — documentation in progress</em> {% endif %}
  <br>
{% endfor %}

## IBM Portables

## Game Consoles

TODO

## Interals / To-Dos

* Add all devices

* Maybe add hifi setup

* Status of 
** progress: pile, started, done
** documentation: stub, started, done

* Add photo gallery (see ChatGPT chat for ideas how to)
