---

title: "Publications"
layout: gridlay
sitemap: true
permalink: /publications/
---

## Publications

<input type="text" class="pub-search" id="pubSearch" placeholder="Filter by title, author, or year...">

<div class="section-card" id="pubList">

<h3>Refereed Journal Articles</h3>

{% bibliography --query @article %}

<h3>Dissertation</h3>

{% bibliography --query @phdthesis %}

</div>
