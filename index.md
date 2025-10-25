# My Collection

This is just a space to keep track of my collection of retro computer stuff

## Home Computers

{% assign started_items = site.home_computers | where: "progress", "started" %}
{% assign done_items = site.home_computers | where: "progress", "done" %}
{% assign filtered = started_items | concat: done_items %}
{% assign sorted_home_computers = filtered | sort: "released" %}

{% include collection_list.html items=sorted_home_computers %}

## IBM Compatible

{% assign started_items = site.ibm_compatibles | where: "progress", "started" %}
{% assign done_items = site.ibm_compatibles | where: "progress", "done" %}
{% assign filtered = started_items | concat: done_items %}
{% assign sorted_ibm_compatibles = filtered | sort: "released" | sort: "class" %}

{% include collection_list.html items=sorted_ibm_compatibles %}

## IBM Portables

{% assign started_items = site.ibm_portables | where: "progress", "started" %}
{% assign done_items = site.ibm_portables | where: "progress", "done" %}
{% assign filtered = started_items | concat: done_items %}
{% assign sorted_ibm_portables = filtered | sort: "released" | sort: "class" %}

{% include collection_list.html items=sorted_ibm_portables %}

## Game Consoles

TODO

## Interals / To-Dos

* Add all devices

* Maybe add hifi setup

* Status of 
** progress: pile, started, done
** documented: stub, started, done

* Add photo gallery (see ChatGPT chat for ideas how to)
