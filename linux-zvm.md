---
layout: page
title: Linux on IBM Z with z/VM
description: >
  Running and administering a Linux server virtualized under z/VM on IBM Z.
permalink: /projects/mainframe-computing/linux-zvm/
sitemap: false
---

{% include mainframe-style.html %}

<div class="mf">
<a class="mf-back" href="{{ '/projects/mainframe-computing/' | relative_url }}">Back to Mainframe Computing</a>

<div class="mf-screen mf-mini" aria-hidden="true">
<p class="mf-cmd">$ <span>uname -m</span></p>
<p class="mf-white">s390x</p>
<p class="mf-cmd">$ <i class="mf-cursor"></i></p>
</div>

<ul class="mf-tags">
  <li>IBM Z</li><li>z/VM</li><li>Linux</li><li>SSH</li><li>Linux administration</li>
</ul>

<p class="mf-lede">Mainframes don't only run z/OS. In this project I worked with a Linux server running as a z/VM guest on IBM Z, connecting traditional mainframe concepts to Linux administration.</p>

<h2>What I did</h2>
<!-- TODO (Angel): Make these specific. Which distro? What did you configure? What security steps did you take (users, SSH keys, firewall, updates)? -->
<ul class="mf-did">
  <li>Connected to a Linux server running under z/VM over SSH</li>
  <li>Worked through the installation and security setup for the server</li>
  <li>Configured and managed the system from the command line</li>
  <li>Learned how z/VM carves one physical machine into virtual servers</li>
</ul>

<h2>Screenshots</h2>
<div class="mf-shots">
  <figure class="mf-shot"><img src="https://placehold.co/800x500/000000/38E038?text=SSH+Session" alt="SSH session into Linux on IBM Z"><figcaption>Connected to the Linux guest over SSH.</figcaption></figure>
  <figure class="mf-shot"><img src="https://placehold.co/800x500/000000/38E038?text=Configuration" alt="Linux configuration commands"><figcaption>Configuring the server from the command line.</figcaption></figure>
</div>

<h2>What I learned</h2>
<p>IBM Z can run many operating environments side by side through virtualization, Linux included. This project tied my mainframe coursework to the Linux and systems skills I use in the rest of my IT work.</p>

<h2>Skills developed</h2>
<ul class="mf-tags">
  <li>Linux</li><li>z/VM</li><li>Virtualization</li><li>Command-line administration</li><li>Systems administration</li>
</ul>

<nav class="mf-nav">
  <a href="{{ '/projects/mainframe-computing/rexx/' | relative_url }}">Previous: REXX programming on z/OS</a>
  <a href="{{ '/projects/mainframe-computing/' | relative_url }}">Back to all mainframe projects</a>
</nav>
</div>
