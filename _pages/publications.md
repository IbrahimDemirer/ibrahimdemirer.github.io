---

title: "Publications"
layout: gridlay
sitemap: false
permalink: /publications/
---

## Publications

<input type="text" class="pub-search" id="pubSearch" placeholder="Filter by title, author, or year...">

<div class="section-card" id="pubList">

<h3>Under Review and Submitted Manuscripts</h3>

{% bibliography --query @unpublished[keywords ^= manuscript] %}

<h3>Working Papers and Work in Progress</h3>

{% bibliography --query @unpublished[keywords ^= prepublication] %}

<h3>Refereed Journal Articles</h3>

{% bibliography --query @article %}

<h3>Dissertation</h3>

{% bibliography --query @phdthesis %}

<h3>Book Chapters and Reports</h3>

{% bibliography --query @incollection %}

{% bibliography --query @techreport %}

</div>
