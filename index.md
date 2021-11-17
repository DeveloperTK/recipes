---
layout: default
home: true
---

Some of my basic student recipes (in German :D)

<ul>
{% assign recipes = site.static_files | where: "recipe", true %}
{% for recipe in recipes %}
  <li>
    <a href="{{ recipe.path | replace: ".md", ".html" | uri_escape }}">{{ recipe.basename | smartify }}</a>
  </li>
{% endfor %}
</ul>

Layout shamelessly stolen from [here](https://github.com/itspriddle/recipes.priddle.xyz)
