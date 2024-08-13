---
layout: archive
title: "Notes"
permalink: /publications/
author_profile: true
---

📝 When I study for a topic, I like to write notes for different modules. Most of school slides are long and messy, thus writing notes makes it a lot clearer and easy to understand. I have uploaded some of my notes below for my own revision and if anyone needs it. 

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
