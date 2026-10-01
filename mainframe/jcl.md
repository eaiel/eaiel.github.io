---
layout: page
title: JCL and Batch Job Processing
description: >
  Building and submitting batch jobs with JCL, then using JCL to run the SORT utility on a customer file.
permalink: /projects/mainframe-computing/jcl/
sitemap: false
---

{% include mainframe-style.html %}
{% assign img = '/assets/img/projects/mainframe/jcl/' | relative_url %}

<div class="mf">
<a class="mf-back" href="{{ '/projects/mainframe-computing/' | relative_url }}">Back to Mainframe Computing</a>

<div class="mf-screen mf-mini" aria-hidden="true">
<p class="mf-white">//SORT     EXEC PGM=SORT</p>
<p>//SORTIN   DD DSN=ECU009.LANG.SOURCE(MASTCUST),DISP=SHR</p>
<p>//SYSIN    DD *</p>
<p class="mf-y">  SORT FIELDS=(1,2,CH,A,3,2,CH,A) <i class="mf-cursor"></i></p>
</div>

<ul class="mf-tags">
  <li>JCL</li><li>z/OS</li><li>TSO/ISPF</li><li>SDSF</li><li>SORT</li>
</ul>

<p class="mf-lede">This project introduced me to Job Control Language and the batch-processing model at the heart of z/OS. I built a job one statement at a time and submitted it, then wrote a job that runs the system SORT utility to put a customer file in order.</p>

<h2>Building a job</h2>
<ol class="mf-flow" aria-label="Building a job">
  <li>Edit JCLTEST</li><li>SUB</li><li>Add JOB statement</li><li class="ok">Resubmit</li>
</ol>

<ol class="mf-life">
  <li>
    <div><h3>Start with one line</h3><p>Copied JCLTEST from CWSEAY.LANG.CNTL into my LANG.CNTL. It held a single statement, <code>//STEP1 EXEC PGM=IEFBR14</code>, with no JOB statement.</p></div>
    <figure class="mf-shot"><img src="{{ img }}01-job-without-jobname.png" alt="JCLTEST with only an EXEC statement" loading="lazy"><figcaption>My job without a job name.</figcaption></figure>
  </li>
  <li>
    <div><h3>Submit it</h3><p>Submitted with <code>SUB</code>. With no JOB statement, z/OS prompted me for a character and built a default job name from my ID.</p></div>
    <figure class="mf-shot"><img src="{{ img }}02-job-submitted.png" alt="Job submitted message" loading="lazy"><figcaption>The job was submitted under a system-generated name.</figcaption></figure>
  </li>
  <li>
    <div><h3>Add a JOB statement</h3><p>Inserted a new first line, moved the EXEC statement down with the M and A line commands, and named the job <code>ECU009A</code>. Then I saved, resubmitted, and tracked my jobs in SDSF using <code>PREFIX *</code> and <code>OWNER ECU009</code>.</p></div>
    <figure class="mf-shot"><img src="{{ img }}03-job-statement-added.png" alt="JCLTEST with JOB statement added" loading="lazy"><figcaption>The JOB statement, added above the EXEC.</figcaption></figure>
  </li>
</ol>

<h2>Putting JCL to work: SORT</h2>
<p>I wrote a job, SORTLAB, that runs the system SORT program on a customer file (MASTCUST). The SYSIN statement sorts on two keys: branch number (bytes 1–2), then sales rep number (bytes 3–4), both ascending. SORTOUT writes the result to a new cataloged dataset.</p>
<ol class="mf-flow">
  <li>MASTCUST</li><li>SORTIN</li><li>SORT FIELDS=(1,2,CH,A,3,2,CH,A)</li><li class="ok">SORTOUT</li>
</ol>
<div class="mf-shots">
  <figure class="mf-shot"><img src="{{ img }}sort-01-data-before-sort.png" alt="MASTCUST data before sorting" loading="lazy"><figcaption>MASTCUST before the sort.</figcaption></figure>
  <figure class="mf-shot"><img src="{{ img }}sort-02-sortlab-jcl.png" alt="SORTLAB JCL" loading="lazy"><figcaption>The SORTLAB job.</figcaption></figure>
  <figure class="mf-shot"><img src="{{ img }}sort-03-data-after-sort.png" alt="Sorted output by branch then sales rep" loading="lazy"><figcaption>SORTOUT, ordered by branch and then sales rep.</figcaption></figure>
</div>

<h2>What I learned</h2>
<p>JCL showed me how mainframes run work in batch: you define a job once with JOB, EXEC, and DD statements, hand it to the system, and it runs without anyone babysitting it. The syntax is precise, down to where a comma or a blank goes. The SORT lab showed how those same few statements drive real data processing, turning an unordered customer file into a sorted dataset.</p>

<h2>Skills developed</h2>
<ul class="mf-tags">
  <li>JCL</li><li>Batch processing</li><li>Job submission</li><li>SDSF</li><li>SORT utility</li><li>DD statements</li>
</ul>

<nav class="mf-nav">
  <a href="{{ '/projects/mainframe-computing/datasets/' | relative_url }}">Previous: z/OS dataset management</a>
  <a href="{{ '/projects/mainframe-computing/rexx/' | relative_url }}">Next: REXX programming on z/OS</a>
</nav>
</div>
