---
layout: page
title: REXX Programming on z/OS
description: >
  Four REXX programs on z/OS: user input, conditionals, loops, and a sum/average calculator.
permalink: /projects/mainframe-computing/rexx/
sitemap: false
---

{% include mainframe-style.html %}
{% assign img = '/assets/img/projects/mainframe/rexx/' | relative_url %}

<div class="mf">
<a class="mf-back" href="{{ '/projects/mainframe-computing/' | relative_url }}">Back to Mainframe Computing</a>

<div class="mf-screen mf-mini" aria-hidden="true">
<p class="mf-r">You entered 2 numbers.</p>
<p class="mf-r">Their total is: 12</p>
<p class="mf-r">Their average is: 6</p>
<p class="mf-r">*** <i class="mf-cursor"></i></p>
</div>

<ul class="mf-tags">
  <li>REXX</li><li>TSO</li><li>ISPF</li><li>z/OS</li>
</ul>

<p class="mf-lede">This is the programming side of my mainframe work. Across four labs I wrote REXX programs in my own ECU009.REXX library, ran them from TSO with the <code>EX</code> command, and debugged them until the output was right.</p>

<h2>The progression</h2>
<ol class="mf-flow">
  <li>Input with PULL</li><li>IF/ELSE</li><li>Loops</li><li class="ok">Sum and average</li>
</ol>

<h2>Lab 4: Sum and average calculator</h2>
<p>The user enters numbers until they type 0000. The program then reports how many numbers were entered, their total, and their average. My first version counted the terminating 0000 as an entry, which threw off both the count and the average. I fixed it by checking for the terminating value before adding to the total or the counter.</p>
<div class="mf-pair">
  <figure class="mf-shot"><img src="{{ img }}lab4-sum-average-source.png" alt="REXX source for the sum and average program" loading="lazy"><figcaption>Source code.</figcaption></figure>
  <figure class="mf-shot"><img src="{{ img }}lab4-sum-average-run.png" alt="Program output showing 2 numbers, total 12, average 6" loading="lazy"><figcaption>Output: 2 entries, a total of 12, and an average of 6.</figcaption></figure>
</div>

<h2>Lab 3: Loops</h2>
<p>The program asks how many times to loop, captures the answer with PULL, and prints which pass it's on each time through. A counter starts at 0 and increases by one per pass until it reaches the user's number.</p>
<div class="mf-pair">
  <figure class="mf-shot"><img src="{{ img }}lab3-loop-source.png" alt="REXX loop program source" loading="lazy"><figcaption>Source code.</figcaption></figure>
  <figure class="mf-shot"><img src="{{ img }}lab3-loop-run.png" alt="Loop program output for 5 iterations" loading="lazy"><figcaption>A run with 5 iterations.</figcaption></figure>
</div>

<h2>Lab 2: IF/ELSE</h2>
<p>IFTEST assigns a value to <code>A</code> and checks whether it equals 100, printing a different message for each case. It also calls TSOCLR to clear the screen before printing.</p>
<div class="mf-pair">
  <figure class="mf-shot"><img src="{{ img }}lab2-if-source-a100.png" alt="IFTEST REXX source" loading="lazy"><figcaption>Source code with A = 100.</figcaption></figure>
  <figure class="mf-shot"><img src="{{ img }}lab2-if-run-a100.png" alt="IFTEST output" loading="lazy"><figcaption>Output.</figcaption></figure>
</div>

<p>Lab 1 came first: a program that asks for a name, hometown, and major with PULL and echoes them back with SAY.</p>

<h2>What I learned</h2>
<p>REXX itself is readable, but writing it inside ISPF means respecting the editor and the formatting rules too. The sum/average bug taught me the bigger lesson: test with real input and check the math, because a program can run cleanly and still be wrong.</p>

<h2>Skills developed</h2>
<ul class="mf-tags">
  <li>REXX</li><li>User input with PULL</li><li>Conditional logic</li><li>Loops and counters</li><li>Debugging</li><li>Testing</li>
</ul>

<nav class="mf-nav">
  <a href="{{ '/projects/mainframe-computing/jcl/' | relative_url }}">Previous: JCL and batch job processing</a>
  <a href="{{ '/projects/mainframe-computing/linuxone/' | relative_url }}">Next: Linux on IBM LinuxONE</a>
</nav>
</div>
