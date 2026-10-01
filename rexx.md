---
layout: page
title: REXX Programming on z/OS
description: >
  Writing, running, and debugging a REXX program inside the z/OS environment.
permalink: /projects/mainframe-computing/rexx/
sitemap: false
---

{% include mainframe-style.html %}

<div class="mf">
<a class="mf-back" href="{{ '/projects/mainframe-computing/' | relative_url }}">Back to Mainframe Computing</a>

<div class="mf-screen mf-mini" aria-hidden="true">
<p class="mf-white">READY</p>
<p class="mf-cmd">EX 'USERID.REXX.EXEC(LAB)' <i class="mf-cursor"></i></p>
</div>

<ul class="mf-tags">
  <li>REXX</li><li>TSO</li><li>ISPF</li><li>z/OS</li>
</ul>

<p class="mf-lede">This is the programming side of my mainframe work. I wrote a REXX program as an ISPF member, ran it on z/OS, and debugged it until it behaved.</p>

<h2>What I did</h2>
<ul class="mf-did">
  <li>Created a REXX program as a member in my library</li>
  <li>Used IF/THEN/ELSE logic to branch on input</li>
  <li>Wrote output to the terminal with <code>SAY</code></li>
  <li>Ran the program from TSO</li>
  <li>Tracked down and fixed syntax and execution errors</li>
</ul>

<h2>Source and output</h2>
<ol class="mf-flow"><li>REXX source</li><li>Execution</li><li class="ok">Program output</li></ol>
<!-- TODO (Angel): Replace both blocks with your actual program and its real output. Escape < as &lt; and > as &gt;. -->
<div class="mf-code">
  <figure>
    <figcaption>REXX source</figcaption>
<pre><code>/* REXX */
SAY 'Enter a number:'
PULL num
IF num &gt; 10 THEN
  SAY num 'is greater than 10'
ELSE
  SAY num 'is 10 or less'
EXIT</code></pre>
  </figure>
  <figure>
    <figcaption>Output</figcaption>
<pre><code>Enter a number:
14
14 is greater than 10
READY</code></pre>
  </figure>
</div>

<h2>What I learned</h2>
<p>REXX showed me how scripting fits into a mainframe: it runs right alongside TSO and ISPF and can automate work you'd otherwise do by hand. Debugging it inside TSO also taught me how source members and execution connect on z/OS.</p>

<h2>Skills developed</h2>
<ul class="mf-tags">
  <li>REXX</li><li>Scripting</li><li>Conditional logic</li><li>Debugging</li><li>Mainframe programming</li>
</ul>

<nav class="mf-nav">
  <a href="{{ '/projects/mainframe-computing/jcl/' | relative_url }}">Previous: JCL and batch job processing</a>
  <a href="{{ '/projects/mainframe-computing/linux-zvm/' | relative_url }}">Next: Linux on IBM Z with z/VM</a>
</nav>
</div>
