# My Collection

This is just a space to keep track of my collection of retro computrer stuff

## Home Computers

{% assign sorted_home_computers = site.home_computers | sort: "released" %}
{% for item in sorted_home_computers %}
  <a href="{{ item.url | relative_url }}">{{ item.title }}</a><br>
{% endfor %}

Apple \]\[c

## Interals / To-Dos

* Add all Computers

* Shoot and add some photos

* Sort out [Jekyll](https://jekyllrb.com/) to use collections in mark-down, maybe have some kind of navigation sidebar
