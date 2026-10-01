---
layout: page
title: z/OS Dataset Management
description: >
  Copying libraries, creating members, and allocating partitioned datasets on z/OS.
permalink: /projects/mainframe-computing/datasets/
sitemap: false
---

{% include mainframe-style.html %}
{% assign img = '/assets/img/projects/mainframe/datasets/' | relative_url %}

<div class="mf">
<a class="mf-back" href="{{ '/projects/mainframe-computing/' | relative_url }}">Back to Mainframe Computing</a>

<div class="mf-screen mf-mini" aria-hidden="true">
<p class="mf-t">Allocate New Data Set  —  ECU009.LAB4</p>
<p class="mf-cmd">Space units <span>TRKS</span>   Primary <span>10</span>   Secondary <span>5</span>   Directory blocks <span>10</span></p>
<p class="mf-cmd">Record format <span>FB</span>   Record length <span>80</span>   Data set type <span>LIBRARY</span> <i class="mf-cursor"></i></p>
</div>

<ul class="mf-tags">
  <li>z/OS</li><li>ISPF</li><li>Move/Copy utility</li><li>Partitioned datasets</li>
</ul>

<p class="mf-lede">This is where I went from looking at mainframe resources to managing my own. I copied the libraries I'd need for the rest of the course, created members, and allocated new datasets with attributes I chose myself.</p>

<h2>What I did</h2>
<ul class="mf-did">
  <li>Copied LANG.SOURCE, LANG.LOAD, and LANG.CNTL from CWSEAY into my own libraries with ISPF Move/Copy (3.3)</li>
  <li>Created three new members (NEWMEM1, NEWMEM2, NEWMEM3) in ECU009.LANG.SOURCE</li>
  <li>Allocated a new library, ECU009.LAB4, with the Data Set Utility (3.2)</li>
  <li>Set its attributes: tracks for space units, 10 primary and 5 secondary, 10 directory blocks, FB records at LRECL 80, block size 0 so z/OS picks the optimum</li>
  <li>Added a member with text, then found it again through the Data Set List Utility (3.4)</li>
  <li>Repeated the process on my own for a second dataset, LAB4-1</li>
</ul>

<p class="mf-flow-label">Lab 3: copying and creating</p>
<ol class="mf-flow">
  <li>CWSEAY libraries</li><li>Move/Copy</li><li>ECU009.LANG.*</li><li class="ok">New members</li>
</ol>
<div class="mf-shots">
  <figure class="mf-shot"><img src="{{ img }}lab3-copied-lang-load-cntl.png" alt="Data set list showing ECU009.LANG.CNTL, LANG.LOAD, and LANG.SOURCE" loading="lazy"><figcaption>My copied LANG.CNTL, LANG.LOAD, and LANG.SOURCE libraries.</figcaption></figure>
  <figure class="mf-shot"><img src="{{ img }}lab3-new-member.png" alt="Editing new member NEWMEM1" loading="lazy"><figcaption>NEWMEM1, a new member I created in LANG.SOURCE.</figcaption></figure>
</div>

<p class="mf-flow-label">Lab 4: allocating and verifying</p>
<ol class="mf-flow">
  <li>Allocate LAB4</li><li>Set attributes</li><li>Add NEWMEM</li><li class="ok">Find it in 3.4</li>
</ol>
<div class="mf-shots">
  <figure class="mf-shot"><img src="{{ img }}lab4-dataset-parameters.png" alt="Allocation panel with dataset parameters" loading="lazy"><figcaption>The allocation parameters I set for LAB4.</figcaption></figure>
  <figure class="mf-shot"><img src="{{ img }}lab4-navigate-to-member.png" alt="Member list of LAB4 showing NEWMEM" loading="lazy"><figcaption>Navigating back to NEWMEM inside LAB4.</figcaption></figure>
</div>

<h2>What I learned</h2>
<p>Mainframe datasets aren't just files. You decide their organization and attributes before they exist, and those choices affect everything that uses them later. Navigating took practice at first, but by the second dataset I could do it without the instructions.</p>

<h2>Skills developed</h2>
<ul class="mf-tags">
  <li>Dataset allocation</li><li>Partitioned datasets</li><li>Move/Copy utility</li><li>Space and record attributes</li>
</ul>

<nav class="mf-nav">
  <a href="{{ '/projects/mainframe-computing/zos-ispf/' | relative_url }}">Previous: z/OS and TSO/ISPF fundamentals</a>
  <a href="{{ '/projects/mainframe-computing/jcl/' | relative_url }}">Next: JCL and batch job processing</a>
</nav>
</div>
