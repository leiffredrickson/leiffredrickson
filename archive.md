---
layout: page
title: Posts
permalink: /archive/
---
<div>

  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        {% assign date_format = site.minima.date_format | default: "%b %-d, %Y" %}
        <span class="post-meta">{{ post.date | date: date_format }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
          <!-- <p style="font-size:16px">{{ post.excerpt }}</p> -->
        </h2>
      </li>
    {% endfor %}
  </ul>
</div>


<!-- <div>
  <h2 class="page-heading">Post Archives</h2>
<section class="archive-post-list">

   {% for post in site.posts %}
       {% assign currentDate = post.date | date: "%Y" %}
       {% if currentDate != myDate %}
           {% unless forloop.first %}</ul>{% endunless %}
           <h1>{{ currentDate }}</h1>
           <ul>
           {% assign myDate = currentDate %}
       {% endif %}
       <li><a href="{{ post.url }}"><span>{{ post.date | date: "%B %-d, %Y" }}</span> - {{ post.title }}</a></li>
       {% if forloop.last %}</ul>{% endif %}
   {% endfor %}

</section>
<br>

</div>-->
