---
layout: page
title: JCL and Batch Job Processing
description: >
  Writing and submitting batch jobs, tracking down a JCL error in SDSF, creating a dataset with JCL, and sorting a file with SORT.
permalink: /projects/mainframe-computing/jcl/
sitemap: false
---

{% include mainframe-style.html %}
{% assign img = '/assets/img/projects/mainframe/jcl/' | relative_url %}

<div class="mf">
<a class="mf-back" href="{{ '/projects/mainframe-computing/' | relative_url }}">Back to Mainframe Computing</a>

<div class="mf-screen mf-mini" aria-hidden="true">
<p class="mf-cmd">Command ===&gt; <span>SUB</span></p>
<p class="mf-white">JOB ECU009A SUBMITTED</p>
<p class="mf-r">IEFC452I ECU009A - JOB NOT RUN - JCL ERROR</p>
<p class="mf-y">IEFC019I MISPLACED DD STATEMENT <i class="mf-cursor"></i></p>
</div>

<ul class="mf-tags">
  <li>JCL</li><li>z/OS</li><li>TSO/ISPF</li><li>SDSF</li><li>IEFBR14</li><li>SORT</li>
</ul>

<p class="mf-lede">This project introduced me to Job Control Language and the batch-processing model at the heart of z/OS. I built up a job one statement at a time, submitted it, read what the system sent back, and fixed what broke. Then I put JCL to work running the SORT utility.</p>

<h2>Building and running a job</h2>
<ol class="mf-flow" aria-label="Batch job lifecycle">
  <li>Edit JCLTEST</li><li>SUB</li><li>SDSF</li><li class="err">JCL error</li><li>Fix</li><li class="ok">ECU009.MYTEST</li>
</ol>

<ol class="mf-life">
  <li>
    <div><h3>Start with one line</h3><p>Copied JCLTEST from CWSEAY.LANG.CNTL into my LANG.CNTL. It held a single statement, <code>//STEP1 EXEC PGM=IEFBR14</code>, with no JOB statement.</p></div>
    <figure class="mf-shot"><img src="{{ img }}01-job-without-jobname.png" alt="JCLTEST with only an EXEC statement" loading="lazy"><figcaption>My job without a job name.</figcaption></figure>
  </li>
  <li>
    <div><h3>Submit it anyway</h3><p>Submitted with <code>SUB</code>. With no JOB statement, z/OS prompted me for a character and built a default job name from my ID.</p></div>
    <figure class="mf-shot"><img src="{{ img }}02-job-submitted.png" alt="Job submitted message" loading="lazy"><figcaption>The job was submitted under a system-generated name.</figcaption></figure>
  </li>
  <li>
    <div><h3>Add a JOB statement</h3><p>Inserted a new first line, moved the EXEC statement down with the M and A line commands, and named the job <code>ECU009A</code>.</p></div>
    <figure class="mf-shot"><img src="{{ img }}03-job-statement-added.png" alt="JCLTEST with JOB statement added" loading="lazy"><figcaption>The JOB statement, added above the EXEC.</figcaption></figure>
  </li>
  <li>
    <div><h3>Read the job log</h3><p>Filtered SDSF to my jobs with <code>PREFIX *</code> and <code>OWNER ECU009</code>, then opened the output. The job hadn't run: JES2 read a line between my JOB and EXEC statements as data, generated a SYSIN DD for it, and rejected the job with a misplaced DD error.</p></div>
    <figure class="mf-shot"><img src="{{ img }}04-sdsf-job-output.png" alt="SDSF job log showing JOB NOT RUN - JCL ERROR and IEFC019I MISPLACED DD STATEMENT" loading="lazy"><figcaption>SDSF pinpointing the error: IEFC019I, misplaced DD statement.</figcaption></figure>
  </li>
  <li>
    <div><h3>Create a dataset with JCL</h3><p>With the JOB and EXEC statements cleaned up, I added a DD statement that uses IEFBR14 to create and catalog a new sequential dataset, ECU009.MYTEST.</p></div>
    <figure class="mf-shot"><img src="{{ img }}05-dd-create-mytest.png" alt="JCLTEST with CREATE DD statement for ECU009.MYTEST" loading="lazy"><figcaption>The DD statement that creates ECU009.MYTEST.</figcaption></figure>
  </li>
  <li>
    <div><h3>Verify</h3><p>ECU009.MYTEST showed up when I listed the datasets on my volume, but not when I searched by name. A name search goes through the catalog and a volume listing reads the disk directly, so this points to the dataset being allocated but not cataloged.</p></div>
    <figure class="mf-shot"><img src="{{ img }}06-mytest-dataset-check.png" alt="Data set list on volume 31EU03 including ECU009.MYTEST" loading="lazy"><figcaption>ECU009.MYTEST on volume 31EU03.</figcaption></figure>
  </li>
</ol>

<h2>Putting JCL to work: SORT</h2>
<p>In a second lab I wrote a job, SORTLAB, that runs the system SORT program on a customer file (MASTCUST). The SYSIN statement sorts on two keys: branch number (bytes 1–2), then sales rep number (bytes 3–4), both ascending. SORTOUT writes the result to a new cataloged dataset.</p>
<ol class="mf-flow">
  <li>MASTCUST</li><li>SORTIN</li><li>SORT FIELDS=(1,2,CH,A,3,2,CH,A)</li><li class="ok">SORTOUT</li>
</ol>
<div class="mf-shots">
  <figure class="mf-shot"><img src="{{ img }}sort-01-data-before-sort.png" alt="MASTCUST data before sorting" loading="lazy"><figcaption>MASTCUST before the sort.</figcaption></figure>
  <figure class="mf-shot"><img src="{{ img }}sort-02-sortlab-jcl.png" alt="SORTLAB JCL" loading="lazy"><figcaption>The SORTLAB job.</figcaption></figure>
  <figure class="mf-shot"><img src="{{ img }}sort-03-data-after-sort.png" alt="Sorted output by branch then sales rep" loading="lazy"><figcaption>SORTOUT, ordered by branch and then sales rep.</figcaption></figure>
</div>

<h2>What I learned</h2>
<p>JCL is unforgiving about syntax, and I hit that more than once. The useful part was learning where to look: SDSF and the job log tell you exactly which statement failed and why, and a dataset search by volume versus by name tells you whether something was actually cataloged. Once the job structure made sense, the SORT lab showed how the same pieces (JOB, EXEC, DD) drive real data processing.</p>

<h2>Skills developed</h2>
<ul class="mf-tags">
  <li>JCL</li><li>Batch processing</li><li>Job submission</li><li>SDSF job logs</li><li>JCL troubleshooting</li><li>SORT utility</li><li>Catalogs and volumes</li>
</ul>

<nav class="mf-nav">
  <a href="{{ '/projects/mainframe-computing/datasets/' | relative_url }}">Previous: z/OS dataset management</a>
  <a href="{{ '/projects/mainframe-computing/rexx/' | relative_url }}">Next: REXX programming on z/OS</a>
</nav>
</div>
