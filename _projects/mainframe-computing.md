---
layout: page
title: Mainframe Computing
caption: IBM Z and z/OS — TSO/ISPF, datasets, JCL, REXX, and Linux on LinuxONE
description: >
  Hands-on work with IBM Z: navigating z/OS, managing datasets, running JCL batch
  jobs, writing REXX, and standing up Linux on IBM LinuxONE.
date: 2026-10-01
permalink: /projects/mainframe-computing/
sitemap: false
---

{% include mainframe-style.html %}

<div class="mf">
<div class="mf-screen" role="img" aria-label="Mainframe Computing: IBM Z and z/OS. Hands-on work navigating z/OS, managing datasets, running JCL batch jobs, writing REXX, and running Linux on IBM LinuxONE.">
<p class="mf-bar"><span>Menu  Utilities  Compilers  Options  Status  Help</span><span>ECU009</span></p>
<p class="mf-title">MAINFRAME COMPUTING</p>
<p class="mf-sub">IBM Z  /  z/OS</p>
<p class="mf-desc">Hands-on work with IBM Z: navigating z/OS, managing datasets, running JCL batch jobs, writing REXX, and standing up Linux on IBM LinuxONE.</p>
<p class="mf-cmd">Option ===&gt; <span>READY</span> <i class="mf-cursor"></i></p>
<p class="mf-pf"><span>F1=<b>Help</b></span><span>F3=<b>Exit</b></span><span>F7=<b>Up</b></span><span>F8=<b>Down</b></span><span>F12=<b>Cancel</b></span></p>
</div>

<h2 id="tools">What I've worked with</h2>
<ul class="mf-tags">
  <li>IBM Z</li><li>z/OS</li><li>TSO/ISPF</li><li>3270 terminal</li><li>JCL</li><li>SDSF</li>
  <li>SORT</li><li>REXX</li><li>IBM LinuxONE</li><li>Ubuntu</li><li>SSH</li><li>MySQL</li>
</ul>

<h2 id="journey">My mainframe journey</h2>
<p>Each step built on the one before it. Start at the top, or jump to the JCL project for the full batch-job story, error included.</p>
<ol class="mf-steps">
  <li>
    <div>
      <p class="labs">Labs 1–2</p>
      <h3>z/OS and TSO/ISPF fundamentals</h3>
      <p>Logging into z/OS through a 3270 emulator and learning TSO, ISPF, the catalog, and system libraries.</p>
    </div>
    <a class="go" href="{{ '/projects/mainframe-computing/zos-ispf/' | relative_url }}">View project</a>
  </li>
  <li>
    <div>
      <p class="labs">Labs 3–4</p>
      <h3>z/OS dataset management</h3>
      <p>Copying libraries, creating members, and allocating my own partitioned datasets.</p>
    </div>
    <a class="go" href="{{ '/projects/mainframe-computing/datasets/' | relative_url }}">View project</a>
  </li>
  <li class="featured">
    <div>
      <p class="labs">JCL Lab 1 + Sort Lab</p>
      <h3>JCL and batch job processing</h3>
      <p>Writing and submitting batch jobs, reading the SDSF job log to track down a JCL error, creating a dataset with JCL, and sorting a file with the SORT utility.</p>
    </div>
    <a class="go" href="{{ '/projects/mainframe-computing/jcl/' | relative_url }}">View project</a>
  </li>
  <li>
    <div>
      <p class="labs">REXX Labs 1–4</p>
      <h3>REXX programming on z/OS</h3>
      <p>Four programs, from user input to conditionals, loops, and a sum/average calculator.</p>
    </div>
    <a class="go" href="{{ '/projects/mainframe-computing/rexx/' | relative_url }}">View project</a>
  </li>
  <li>
    <div>
      <p class="labs">LinuxONE lab</p>
      <h3>Linux on IBM LinuxONE</h3>
      <p>Spinning up an Ubuntu server on IBM's LinuxONE Community Cloud, connecting over SSH, and installing MySQL.</p>
    </div>
    <a class="go" href="{{ '/projects/mainframe-computing/linuxone/' | relative_url }}">View project</a>
  </li>
</ol>

<h2 id="skills">Mainframe technologies</h2>
<div class="mf-groups">
  <div><h3>Operating systems</h3><ul><li>z/OS</li><li>Ubuntu Linux</li></ul></div>
  <div><h3>Mainframe tools</h3><ul><li>TSO</li><li>ISPF</li><li>SDSF</li><li>3270 terminal</li></ul></div>
  <div><h3>Programming and automation</h3><ul><li>JCL</li><li>REXX</li><li>SORT</li></ul></div>
  <div><h3>Systems</h3><ul><li>IBM Z</li><li>IBM LinuxONE</li><li>SSH</li><li>MySQL</li></ul></div>
  <div><h3>Core concepts</h3><ul><li>Batch processing</li><li>Dataset allocation</li><li>Catalogs and volumes</li><li>Reading job logs</li></ul></div>
</div>

<h2 id="taught">What mainframe computing taught me</h2>
<!--
  TODO (Angel): Replace this with 3–5 sentences in your own words. Prompts:
  - What did you assume about mainframes before Lab 1? What changed?
  - Your labs keep coming back to the same lesson: you hit an error, read what the
    system told you, and fixed it (JCL error, REXX average bug). Is that the real takeaway?
  - How does this change how you think about cybersecurity / IT systems?
-->
<blockquote class="mf-quote">
  Mainframes aren't simply large computers. They represent a different approach to reliability, scalability, and centralized data processing.
</blockquote>
</div>
