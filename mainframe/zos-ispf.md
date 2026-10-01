---
layout: page
title: z/OS and TSO/ISPF Fundamentals
description: >
  Logging into z/OS through a 3270 emulator and navigating TSO, ISPF, the catalog, and system libraries.
permalink: /projects/mainframe-computing/zos-ispf/
sitemap: false
---

{% include mainframe-style.html %}
{% assign img = '/assets/img/projects/mainframe/zos-ispf/' | relative_url %}

<div class="mf">
<a class="mf-back" href="{{ '/projects/mainframe-computing/' | relative_url }}">Back to Mainframe Computing</a>

<div class="mf-screen mf-mini" aria-hidden="true">
<p class="mf-cmd">LISTC</p>
<p class="mf-white">IN CATALOG:V31E.ECU.USER.CATALOG</p>
<p>ECU009.BRODCAST</p>
<p class="mf-white">READY <i class="mf-cursor"></i></p>
</div>

<ul class="mf-tags">
  <li>IBM Z</li><li>z/OS</li><li>TSO</li><li>ISPF</li><li>SDSF</li><li>3270 terminal</li>
</ul>

<p class="mf-lede">My first two labs were about getting into a z/OS system and learning to move around without a mouse. I logged in through a 3270 terminal emulator, worked from the TSO READY prompt and ISPF menus, and learned where datasets, catalogs, and system libraries live.</p>

<h2>What I did</h2>
<ul class="mf-did">
  <li>Logged into TSO through the Mocha 3270 emulator and ended sessions properly with EXIT and LOGOFF</li>
  <li>Browsed another user's JCL library (CWSEAY.JCL) from the View Entry panel without changing anything</li>
  <li>Opened the system log in SDSF to see what was running on the system</li>
  <li>Switched my TSO profile between PREFIX and NOPREFIX to see how z/OS resolves dataset names</li>
  <li>Ran <code>LISTC</code> to list my catalog entries, using PA1 to interrupt long output</li>
  <li>Used the Data Set List Utility (3.4) to explore SYS1 datasets and the members of SYS1.PROCLIB</li>
  <li>Toggled the function-key legend with PFSHOW ON and OFF</li>
</ul>

<h2>Screenshots</h2>
<div class="mf-shots">
  <figure class="mf-shot"><img src="{{ img }}lab2-tso-ready-prompt.png" alt="TSO READY prompt" loading="lazy"><figcaption>The TSO READY prompt, the starting point for every session.</figcaption></figure>
  <figure class="mf-shot"><img src="{{ img }}lab1-view-entry-panel.png" alt="ISPF View Entry panel" loading="lazy"><figcaption>The ISPF View Entry panel, used to open datasets read-only.</figcaption></figure>
  <figure class="mf-shot"><img src="{{ img }}lab2-listc-catalog.png" alt="LISTC output showing ECU009 catalog entries" loading="lazy"><figcaption>LISTC showing the datasets cataloged under my ID.</figcaption></figure>
  <figure class="mf-shot"><img src="{{ img }}lab2-sys1-proclib-members.png" alt="Member list of SYS1.PROCLIB" loading="lazy"><figcaption>Members of SYS1.PROCLIB, where system procedures live.</figcaption></figure>
</div>

<h2>What I learned</h2>
<p>Almost everything on z/OS happens through structured panels, commands, and function keys. Once I understood how TSO resolves dataset names and how the catalog points to them, the system stopped feeling like a wall of green text and started feeling organized.</p>

<h2>Skills developed</h2>
<ul class="mf-tags">
  <li>TSO/ISPF navigation</li><li>Catalog lookups</li><li>Dataset naming</li><li>SDSF system log</li><li>3270 terminal use</li>
</ul>

<nav class="mf-nav">
  <span></span>
  <a href="{{ '/projects/mainframe-computing/datasets/' | relative_url }}">Next: z/OS dataset management</a>
</nav>
</div>
