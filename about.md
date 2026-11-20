---
layout: about
image: /assets/img/blog/hydejack-9.jpg
description: >
  Portfolio of Eaiel 'Angel' Camilotes. Cybersecurity Student and Business Administration & IT Intern. 
hide_description: true
---

<script type="module" src="https://ajax.googleapis.com/ajax/libs/model-viewer/3.4.0/model-viewer.min.js"></script>

<div style="margin: 1.5rem 0; display: flex; justify-content: center;">
  <model-viewer 
  src="/assets/img/retro-computer/retro-computer-fixed.glb" 
  alt="A 3D model of a retro computer"
  auto-rotate 
  camera-controls
  disable-zoom
  bounds="tight"
  camera-orbit="0deg 75deg 60%"
  environment-image="/assets/img/pinkblue.hdr"
  exposure="1.2"
  shadow-intensity="1"
  style="width: 100%; max-width: 500px; height: 350px; background-color: transparent; margin: 0 auto;">
  </model-viewer>
</div>
<p style="font-size: 0.8rem; color: #888; margin-top: 0.3rem; text-align: center;">
  This work is based on <a href="https://sketchfab.com/3d-models/retro-computer-9439cb5e09cc44caa63dfbfb299df45f">"Retro computer"</a> 
  by <a href="https://sketchfab.com/dogflesh">dogflesh</a>, licensed under 
  <a href="http://creativecommons.org/licenses/by/4.0/">CC-BY-4.0</a>
</p>

# About

<!--author-->

## Eaiel Camilotes

I am a student currently pursuing a Bachelors in Science for Cybersecurity and Information Technology. I also work full-time as a Business Administration Intern for a Food & Hospitality company. I have skills with auditing, data collection, formatting and creating documentation for ~12 brands. Personally, I have started building projects and taking certifications to take my first step into the IT and Security workforce. 
{:.lead}

1. this list will be replaced by the toc
{:toc .large-only}

> Recipes, rollout guides, SOPs, and systems — built to make things run smoother. Coming soon with Security centric projects. 
{:.lead}

## Portfolio

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;600&display=swap" rel="stylesheet">
<style>
  .rt { --mono: "IBM Plex Mono", ui-monospace, Menlo, Consolas, monospace;
        --blk: #000; --grn: #38E038; --turq: #40E0D0; --yel: #F5E642; --wht: #F2F2F2; --blu: #7890F0;
        font-family: var(--mono); background: var(--blk); color: var(--grn); border-radius: 8px;
        padding: 1rem 1.1rem 1.2rem; margin: 1.25rem 0 2rem; box-shadow: inset 0 0 0 1px #1d3a1d, 0 0 24px rgba(56,224,56,.08); }
  .rt p { margin: 0; }
  .rt-bar { display: flex; justify-content: space-between; gap: 1rem; color: var(--blu); font-size: .85rem; white-space: nowrap; overflow: hidden; }
  .rt-cmd { color: var(--turq); font-size: .9rem; margin: .9rem 0 1rem !important; }
  .rt-cmd span { color: var(--wht); }
  .rt-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(230px, 1fr)); gap: 1rem; }
  .rt-card { display: flex; flex-direction: column; border: 1px solid #2a5a2a; border-radius: 4px; overflow: hidden;
             color: var(--grn) !important; text-decoration: none !important; border-bottom-width: 1px !important;
             transition: border-color .15s ease, box-shadow .15s ease; }
  .rt-card:hover, .rt-card:focus-visible { border-color: var(--grn); box-shadow: 0 0 14px rgba(56,224,56,.35); outline: none; }
  .rt-shot { position: relative; aspect-ratio: 16 / 9; overflow: hidden; border-bottom: 1px solid #2a5a2a; }
  .rt-shot img { width: 100%; height: 100%; object-fit: cover; object-position: top left; margin: 0; display: block;
                 filter: grayscale(1) contrast(1.15) brightness(.85); transition: filter .2s ease; }
  .rt-shot::before { content: ""; position: absolute; inset: 0; z-index: 1; background: rgba(56,224,56,.28); mix-blend-mode: multiply; transition: opacity .2s ease; }
  .rt-shot::after { content: ""; position: absolute; inset: 0; z-index: 2; pointer-events: none;
                    background: repeating-linear-gradient(to bottom, rgba(0,0,0,.28) 0 1px, transparent 1px 3px); }
  .rt-card:hover .rt-shot img, .rt-card:focus-visible .rt-shot img { filter: none; }
  .rt-card:hover .rt-shot::before, .rt-card:focus-visible .rt-shot::before { opacity: 0; }
  .rt-body { padding: .8rem .9rem .9rem; display: flex; flex-direction: column; gap: .45rem; flex: 1; }
  .rt-id { color: var(--blu); font-size: .78rem; }
  .rt-title { color: var(--wht); font-weight: 600; font-size: 1.05rem; letter-spacing: .03em; text-transform: uppercase; }
  .rt-desc { font-size: .85rem; line-height: 1.5; }
  .rt-tags { color: var(--yel); font-size: .78rem; }
  .rt-go { margin-top: auto !important; padding-top: .3rem; color: var(--turq); font-size: .85rem; }
  .rt-cursor { display: inline-block; width: .55em; height: 1em; vertical-align: -.12em; background: var(--grn); opacity: 0; }
  .rt-card:hover .rt-cursor, .rt-card:focus-visible .rt-cursor { opacity: 1; animation: rt-blink 1.1s steps(1) infinite; }
  @keyframes rt-blink { 50% { opacity: 0; } }
  .rt-pf { color: var(--turq); font-size: .85rem; margin-top: 1rem !important; display: flex; flex-wrap: wrap; gap: .25rem 1.25rem; }
  .rt-pf a { color: var(--wht) !important; text-decoration: none !important; border-bottom: 1px dotted var(--wht) !important; }
  @media (prefers-reduced-motion: reduce) { .rt-card, .rt-shot img, .rt-shot::before { transition: none; } .rt-card:hover .rt-cursor { animation: none; } }
</style>

<div class="rt">
<p class="rt-bar"><span>Menu  Utilities  Options  Help</span><span>ECU009.PORTFOLIO</span></p>
<p class="rt-cmd">Command ===&gt; <span>LIST PROJECTS</span></p>
<div class="rt-grid">
  <a class="rt-card" href="{{ '/projects/mainframe-computing/' | relative_url }}">
    <div class="rt-shot"><img src="{{ '/assets/img/projects/mainframe/zos-ispf/lab1-view-entry-panel.png' | relative_url }}" alt="ISPF View Entry panel on z/OS" loading="lazy"></div>
    <div class="rt-body">
      <p class="rt-id">PRJ001  //  IBM Z</p>
      <p class="rt-title">Mainframe Computing</p>
      <p class="rt-desc">Navigating z/OS, managing datasets, running JCL batch jobs, writing REXX, and Linux on LinuxONE.</p>
      <p class="rt-tags">z/OS  TSO/ISPF  JCL  REXX  LinuxONE</p>
      <p class="rt-go">&gt; OPEN <span class="rt-cursor"></span></p>
    </div>
  </a>
  <a class="rt-card" href="{{ '/projects/wireless-networking/' | relative_url }}">
    <div class="rt-shot"><img src="{{ '/assets/img/projects/wireless/lab4-topology.png' | relative_url }}" alt="Cisco Packet Tracer network topology" loading="lazy"></div>
    <div class="rt-body">
      <p class="rt-id">PRJ002  //  NETWORKING</p>
      <p class="rt-title">Wireless Networking</p>
      <p class="rt-desc">Building and securing wired and wireless networks in Cisco Packet Tracer, plus wireless site survey planning.</p>
      <p class="rt-tags">Packet Tracer  802.11  WPA2</p>
      <p class="rt-go">&gt; OPEN <span class="rt-cursor"></span></p>
    </div>
  </a>
</div>
<p class="rt-pf"><span>F3=<a href="{{ '/projects/' | relative_url }}">All Projects</a></span><span>F4=<a href="{{ '/resume/' | relative_url }}">Resume</a></span><span>F5=<a href="{{ '/certifications/' | relative_url }}">Certs</a></span></p>
</div>


[jekyll]: https://jekyllrb.com