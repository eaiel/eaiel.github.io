---
layout: page
title: z/OS and TSO/ISPF Fundamentals
description: >
  Accessing and navigating a z/OS environment through a 3270 terminal using TSO and ISPF.
permalink: /projects/mainframe-computing/zos-ispf/
sitemap: false
---

{% include mainframe-style.html %}

<div class="mf">
<a class="mf-back" href="{{ '/projects/mainframe-computing/' | relative_url }}">Back to Mainframe Computing</a>

<div class="mf-screen mf-mini" aria-hidden="true">
<p class="mf-white">READY</p>
<p class="mf-cmd">ISPF <i class="mf-cursor"></i></p>
</div>

<ul class="mf-tags">
  <li>IBM Z</li><li>z/OS</li><li>TSO</li><li>ISPF</li><li>3270 terminal</li>
</ul>

<p class="mf-lede">My introduction to mainframe computing started with getting into a z/OS system through a 3270 terminal. I used TSO and ISPF to work with the operating system, move through system panels, find datasets, and examine members in system libraries.</p>

<h2>What I did</h2>
<ul class="mf-did">
  <li>Logged into z/OS through a 3270 terminal emulator</li>
  <li>Worked from the TSO READY prompt and the ISPF Primary Option Menu</li>
  <li>Used ISPF utilities to locate and examine datasets</li>
  <li>Ran <code>LISTC</code> (LISTCAT) to pull catalog and dataset information</li>
  <li>Explored SYS1 system libraries, including SYS1.PROCLIB</li>
  <li>Opened and browsed dataset members</li>
</ul>

<h2>Screenshots</h2>
<!-- Replace each src with your image, e.g. {{ '/assets/img/projects/mainframe/zos-ready.png' | relative_url }} -->
<div class="mf-shots">
  <figure class="mf-shot"><img src="https://placehold.co/800x500/000000/38E038?text=TSO+READY" alt="TSO READY prompt"><figcaption>The TSO READY prompt, the starting point for every session.</figcaption></figure>
  <figure class="mf-shot"><img src="https://placehold.co/800x500/000000/38E038?text=ISPF+Primary+Menu" alt="ISPF Primary Option Menu"><figcaption>The ISPF Primary Option Menu.</figcaption></figure>
  <figure class="mf-shot"><img src="https://placehold.co/800x500/000000/38E038?text=Member+List" alt="Dataset member listing"><figcaption>A dataset member list in ISPF.</figcaption></figure>
  <figure class="mf-shot"><img src="https://placehold.co/800x500/000000/38E038?text=SYS1.PROCLIB" alt="SYS1.PROCLIB members"><figcaption>Browsing SYS1.PROCLIB, where system procedures live.</figcaption></figure>
</div>

<h2>What I learned</h2>
<p>Unlike a graphical OS, most mainframe work happens through structured panels, commands, and keyboard navigation. This lab showed me how TSO and ISPF give you the tools to work with z/OS resources quickly once you know where things are.</p>

<h2>Skills developed</h2>
<ul class="mf-tags">
  <li>TSO/ISPF navigation</li><li>Dataset discovery</li><li>3270 terminal use</li><li>System libraries</li>
</ul>

<nav class="mf-nav">
  <span></span>
  <a href="{{ '/projects/mainframe-computing/datasets/' | relative_url }}">Next: z/OS dataset management</a>
</nav>
</div>
