---
layout: page
title: JCL and Batch Job Processing
description: >
  Preparing, submitting, monitoring, and verifying batch jobs on z/OS with JCL and SDSF.
permalink: /projects/mainframe-computing/jcl/
sitemap: false
---

{% include mainframe-style.html %}

<div class="mf">
<a class="mf-back" href="{{ '/projects/mainframe-computing/' | relative_url }}">Back to Mainframe Computing</a>

<div class="mf-screen mf-mini" aria-hidden="true">
<p class="mf-cmd">Command ===&gt; <span>SUB</span></p>
<p class="mf-white">JOB JOB01234 SUBMITTED</p>
<p><span class="mf-t">STEPNAME</span>  <span class="mf-t">PROCSTEP</span>  <span class="mf-t">RC</span></p>
<p>STEP1               <span class="mf-y">COND CODE 0000</span> <i class="mf-cursor"></i></p>
</div>

<ul class="mf-tags">
  <li>JCL</li><li>z/OS</li><li>TSO/ISPF</li><li>SDSF</li>
</ul>

<p class="mf-lede">This project introduced me to Job Control Language and the batch-processing model at the heart of z/OS. I took existing JCL, adapted it to my environment, submitted it, tracked it through SDSF, and confirmed it completed cleanly.</p>

<h2>The lifecycle of a batch job</h2>
<ol class="mf-flow" aria-label="Batch job lifecycle">
  <li>JCL source</li><li>Modify</li><li>SUB</li><li>z/OS</li><li>SDSF</li><li class="ok">COND CODE 0000</li><li>Job output</li>
</ol>

<ol class="mf-life">
  <li>
    <div><h3>Prepare</h3><p>Copied JCL members into my working control library and reviewed the job structure.</p></div>
    <figure class="mf-shot"><img src="https://placehold.co/800x500/000000/38E038?text=JCL+Source" alt="JCL source in the ISPF editor"><figcaption>The JCL source in the ISPF editor.</figcaption></figure>
  </li>
  <li>
    <div><h3>Modify</h3><p>Updated the JCL to point at my assigned datasets and match my environment.</p></div>
    <figure class="mf-shot"><img src="https://placehold.co/800x500/000000/38E038?text=Edited+JCL" alt="Modified JCL"><figcaption>The JCL after my edits.</figcaption></figure>
  </li>
  <li>
    <div><h3>Submit</h3><p>Submitted the job from TSO/ISPF with the <code>SUB</code> command.</p></div>
    <figure class="mf-shot"><img src="https://placehold.co/800x500/000000/38E038?text=SUB" alt="Job submitted message"><figcaption>z/OS confirming the job was submitted.</figcaption></figure>
  </li>
  <li>
    <div><h3>Monitor</h3><p>Found the job in SDSF and walked through its execution and output.</p></div>
    <figure class="mf-shot"><img src="https://placehold.co/800x500/000000/38E038?text=SDSF" alt="Job in SDSF"><figcaption>Tracking the job in SDSF.</figcaption></figure>
  </li>
  <li>
    <div><h3>Verify</h3><p>Checked the job output and confirmed a clean run with COND CODE 0000.</p></div>
    <figure class="mf-shot"><img src="https://placehold.co/800x500/000000/38E038?text=COND+CODE+0000" alt="COND CODE 0000 in job output"><figcaption>COND CODE 0000: the job ran without errors.</figcaption></figure>
  </li>
</ol>

<h2>What I learned</h2>
<p>JCL showed me how mainframes run work in batch: you define a job once, hand it to the system, and it runs without anyone babysitting it. SDSF is how you find out what actually happened, whether that's a clean 0000 or a failure you need to dig into.</p>

<h2>Skills developed</h2>
<ul class="mf-tags">
  <li>JCL</li><li>Batch processing</li><li>Job submission</li><li>SDSF</li><li>Completion-code analysis</li><li>Troubleshooting</li>
</ul>

<nav class="mf-nav">
  <a href="{{ '/projects/mainframe-computing/datasets/' | relative_url }}">Previous: z/OS dataset management</a>
  <a href="{{ '/projects/mainframe-computing/rexx/' | relative_url }}">Next: REXX programming on z/OS</a>
</nav>
</div>
