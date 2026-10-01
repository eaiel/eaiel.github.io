---
layout: page
title: z/OS Dataset Management
description: >
  Copying libraries, creating members, and allocating and verifying datasets in z/OS.
permalink: /projects/mainframe-computing/datasets/
sitemap: false
---

{% include mainframe-style.html %}

<div class="mf">
<a class="mf-back" href="{{ '/projects/mainframe-computing/' | relative_url }}">Back to Mainframe Computing</a>

<div class="mf-screen mf-mini" aria-hidden="true">
<p class="mf-t">Allocate New Data Set</p>
<p class="mf-cmd">Record format . . <span>FB</span>    Record length . . <span>80</span>    Directory blocks . . <span>10</span></p>
</div>

<ul class="mf-tags">
  <li>z/OS</li><li>ISPF</li><li>Dataset utilities</li><li>Partitioned datasets</li>
</ul>

<p class="mf-lede">This project was the jump from looking at mainframe resources to actually managing them. I copied and moved existing libraries, created new members, allocated my own datasets, and verified everything landed where it should.</p>

<h2>What I did</h2>
<ul class="mf-did">
  <li>Copied source, load, and control libraries into my own user libraries</li>
  <li>Worked with partitioned datasets (PDS) and their members</li>
  <li>Created and saved new members</li>
  <li>Allocated a new dataset through ISPF</li>
  <li>Set space and dataset attributes: tracks, directory blocks, record format, and LRECL</li>
  <li>Verified datasets and members with ISPF utilities</li>
</ul>

<p class="mf-flow-label">Lab 3: copying and creating</p>
<ol class="mf-flow">
  <li>Source dataset</li><li>Copy / move</li><li>User library</li><li class="ok">New members</li>
</ol>
<div class="mf-shots">
  <figure class="mf-shot"><img src="https://placehold.co/800x500/000000/38E038?text=Copy+%2F+Move" alt="ISPF copy/move utility"><figcaption>Copying a library into my user space.</figcaption></figure>
  <figure class="mf-shot"><img src="https://placehold.co/800x500/000000/38E038?text=New+Member" alt="Newly created member"><figcaption>A new member saved in my library.</figcaption></figure>
</div>

<p class="mf-flow-label">Lab 4: allocating and verifying</p>
<ol class="mf-flow">
  <li>Allocate dataset</li><li>LAB4</li><li>NEWMEM</li><li class="ok">Verified</li>
</ol>
<div class="mf-shots">
  <figure class="mf-shot"><img src="https://placehold.co/800x500/000000/38E038?text=Allocation+Panel" alt="ISPF dataset allocation panel"><figcaption>Setting space and record attributes for the new dataset.</figcaption></figure>
  <figure class="mf-shot"><img src="https://placehold.co/800x500/000000/38E038?text=Verification" alt="Dataset verification in ISPF"><figcaption>Confirming LAB4 and NEWMEM exist with the right attributes.</figcaption></figure>
</div>

<h2>What I learned</h2>
<p>Mainframe datasets aren't just files. They have defined organizations and attributes that you have to decide on before you create them, and getting those wrong causes problems later. I also got in the habit of verifying every resource after creating it instead of assuming it worked.</p>

<h2>Skills developed</h2>
<ul class="mf-tags">
  <li>Dataset allocation</li><li>Partitioned datasets</li><li>ISPF utilities</li><li>Storage concepts</li><li>Resource organization</li>
</ul>

<nav class="mf-nav">
  <a href="{{ '/projects/mainframe-computing/zos-ispf/' | relative_url }}">Previous: z/OS and TSO/ISPF fundamentals</a>
  <a href="{{ '/projects/mainframe-computing/jcl/' | relative_url }}">Next: JCL and batch job processing</a>
</nav>
</div>
