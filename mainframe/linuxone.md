---
layout: page
title: Linux on IBM LinuxONE
description: >
  Creating an Ubuntu server on IBM's LinuxONE Community Cloud, connecting over SSH, and installing MySQL.
permalink: /projects/mainframe-computing/linuxone/
sitemap: false
---

{% include mainframe-style.html %}
{% assign img = '/assets/img/projects/mainframe/linux/' | relative_url %}

<div class="mf">
<a class="mf-back" href="{{ '/projects/mainframe-computing/' | relative_url }}">Back to Mainframe Computing</a>

<div class="mf-screen mf-mini" aria-hidden="true">
<p class="mf-cmd">linux1@ecu-3:~$ <span>sudo apt install mysql-server</span></p>
<p class="mf-cmd">linux1@ecu-3:~$ <span>sudo mysql</span></p>
<p class="mf-cmd">mysql&gt; <span>SHOW DATABASES;</span> <i class="mf-cursor"></i></p>
</div>

<ul class="mf-tags">
  <li>IBM LinuxONE</li><li>Ubuntu</li><li>SSH</li><li>MySQL</li><li>Command line</li>
</ul>

<p class="mf-lede">IBM's mainframe hardware runs Linux too. In this lab I created my own Ubuntu server on IBM's LinuxONE Community Cloud, connected to it with an SSH key pair, and installed and ran MySQL from the command line.</p>

<h2>What I did</h2>
<ol class="mf-flow">
  <li>Create instance</li><li>SSH key pair</li><li>Connect</li><li>Install MySQL</li><li class="ok">SHOW DATABASES</li>
</ol>
<ul class="mf-did">
  <li>Created an Ubuntu server instance on the LinuxONE Community Cloud</li>
  <li>Generated an SSH key pair and used it to connect to the server</li>
  <li>Installed MySQL with <code>sudo apt install mysql-server</code></li>
  <li>Opened MySQL with <code>sudo mysql</code> and listed the databases to confirm the install</li>
</ul>

<h2>Screenshots</h2>
<div class="mf-shots">
  <figure class="mf-shot"><img src="{{ img }}linuxone-environment.png" alt="LinuxONE Community Cloud dashboard showing one active instance" loading="lazy"><figcaption>My active Ubuntu instance on the LinuxONE Community Cloud. Account email and IP address redacted.</figcaption></figure>
  <figure class="mf-shot"><img src="{{ img }}creating-ssh-key.png" alt="Creating an SSH key pair" loading="lazy"><figcaption>Creating the SSH key pair used to log in.</figcaption></figure>
  <figure class="mf-shot"><img src="{{ img }}linux-command-line.png" alt="Logged into the LinuxONE server over SSH" loading="lazy"><figcaption>Logged into the server over SSH.</figcaption></figure>
  <figure class="mf-shot"><img src="{{ img }}mysql-databases.png" alt="MySQL SHOW DATABASES output" loading="lazy"><figcaption>MySQL running, with its databases listed.</figcaption></figure>
</div>

<h2>What I learned</h2>
<p>This lab connected the mainframe world to tools I already use. The same hardware family that runs z/OS also hosts ordinary Linux servers, and once I was in, it was standard Ubuntu: key-based SSH, apt, and MySQL from the command line.</p>

<h2>Skills developed</h2>
<ul class="mf-tags">
  <li>Linux server setup</li><li>SSH key authentication</li><li>Package management</li><li>MySQL</li><li>IBM LinuxONE</li>
</ul>

<nav class="mf-nav">
  <a href="{{ '/projects/mainframe-computing/rexx/' | relative_url }}">Previous: REXX programming on z/OS</a>
  <a href="{{ '/projects/mainframe-computing/' | relative_url }}">Back to all mainframe projects</a>
</nav>
</div>
