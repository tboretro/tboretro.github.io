# My Collection
This is just a space to keep track of my collection of retro computrer stuff

## Computers
[Atari ST](computers/atari_st.md)

## Computers 
{% for computer in site.computers %}
  <h2>{{ computer.title }}</h2>
  <p>{{ computer.content | markdownify }}</p>
{% endfor %}
