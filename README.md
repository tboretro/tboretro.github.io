# My Collection

This is just a space to keep track of my collection of retro computrer stuff

## Home Computers

{% assign sorted_home_computers = site.home_computers | sort: "released" %}
{% for item in sorted_home_computers %}
  <a href="{{ item.url | relative_url }}">{{ item.title }} (released in {{ item.released }})</a><br>
{% endfor %}


## Interals / To-Dos

* Add all Computers

* Add phto gallery (see )
