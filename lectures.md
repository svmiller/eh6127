---
layout: page
title: Lectures
permalink: /lectures/
---

<!-- <ul id="archive">


{% for gallery in site.data.lectures %}
  {% if lectures.id == page.galleryid %}
    <h1>{{ lectures.description }}</h1>
    {% for image in sortedimages %}
      <li class="archiveposturl">
        <span><a href="{{ site.url }}/graphs/{{ image.file }}">{{image.title }}</a></span><br>
<span class = "postlower">{{ image.caption }}<br />
<strong>Tags:</strong> {{ image.tags }}</span>
      </li>
    {% endfor %}
  {% endif %}
{% endfor %}

</ul> -->

This page contains link to the lectures I give throughout the semester. Clicking the title of the week's lecture will go to a PDF, embedded in the user's browser, by default. The bottom left icons link to the Github directory for the lecture (<i class="fab fa-github"></i>), the R Markdown document for the lecture (<i class="fab fa-r-project"></i>), and a PDF, embedded on Github, for the lecture (<i class="fas fa-file-pdf"></i>).

<ul id="archive">
{% for lectures in site.data.lectures %}
      <li class="archiveposturl">
        <span><a href="{{ site.url }}/{{ lectures.dirname }}/eh6127-lecture-{{ lectures.filename }}.pdf">{{ lectures.title }}</a></span><br>
<span class = "postlower">
<strong>tl;dr:</strong> {{ lectures.tldr }}</span>
<strong style="font-size:100%; font-family: 'Titillium Web', sans-serif;  padding-right: .5em">
<br />
	<a href="https://github.com/{{ site.githubdir}}/tree/master/{{ lectures.dirname }}"><i class="fab fa-github"></i></a>&nbsp;&nbsp;
<a href="https://github.com/{{ site.githubdir}}/tree/master/{{ lectures.dirname }}/eh6127-lecture-{{ lectures.filename}}.Rmd"><i class="fab fa-r-project"></i></a>&nbsp;&nbsp;
<a href="https://github.com/{{ site.githubdir}}/blob/master/{{ lectures.dirname }}/eh6127-lecture-{{ lectures.filename}}.pdf"><i class="fas fa-file-pdf"></i></a>
</strong> 
      </li>
{% endfor %}
</ul>
