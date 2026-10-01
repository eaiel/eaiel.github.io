---
layout: page
title: Wireless Networking
description: >
  Building and securing wired and wireless networks in Cisco Packet Tracer, and planning a wireless site survey.
permalink: /projects/wireless-networking/
sitemap: false
---

{% include wireless-style.html %}
{% assign img = '/assets/img/projects/wireless/' | relative_url %}

<div class="wl">
<div class="wl-hero">
<p class="wl-title">Wireless Networking</p>
<p class="wl-sub">Cisco Packet Tracer / IEEE 802.11 / WPA2</p>
<p class="wl-desc">Building, connecting, and securing wired and wireless networks, then proving they work.</p>
<svg class="wl-diagram" viewBox="0 0 640 90" role="img" aria-label="Diagram: a laptop connects wirelessly to a wireless router, which is wired to a switch and a server.">
  <line x1="70" y1="40" x2="210" y2="40" stroke="#9FB8CC" stroke-width="3" stroke-dasharray="3 6"/>
  <line x1="250" y1="40" x2="390" y2="40" stroke="#F4F8FB" stroke-width="3"/>
  <line x1="430" y1="40" x2="570" y2="40" stroke="#F4F8FB" stroke-width="3"/>
  <g fill="#3CB54A">
    <polygon points="80,33 80,47 92,40"/><polygon points="200,33 200,47 188,40"/>
    <polygon points="260,33 260,47 272,40"/><polygon points="380,33 380,47 368,40"/>
    <polygon points="440,33 440,47 452,40"/><polygon points="560,33 560,47 548,40"/>
  </g>
  <g fill="#1B4766" stroke="#F4F8FB" stroke-width="2">
    <rect x="34" y="24" width="36" height="32" rx="4"/><circle cx="230" cy="40" r="20"/>
    <rect x="392" y="28" width="36" height="24" rx="3"/><rect x="574" y="18" width="30" height="44" rx="3"/>
  </g>
  <text x="52" y="80" text-anchor="middle">Laptop</text><text x="230" y="80" text-anchor="middle">Wireless router</text>
  <text x="410" y="80" text-anchor="middle">Switch</text><text x="589" y="80" text-anchor="middle">Server</text>
</svg>
<p class="wl-ping">Reply from 192.168.50.1: bytes=32 time=48ms TTL=255
Packets: Sent = 4, Received = 4, Lost = 0 <span class="ok">(0% loss)</span></p>
</div>

<ul class="wl-tags">
  <li>Cisco Packet Tracer</li><li>IEEE 802.11</li><li>WPA2-Personal</li><li>SSID</li><li>DHCP</li>
  <li>VLANs</li><li>Serial links</li><li>ping</li><li>Wi-Fi site surveys</li>
</ul>

<p class="wl-lede">I built four networks in Cisco Packet Tracer, each adding something new: a basic wireless router setup, a secured Linksys router, a wireless LAN joined to a VLAN-segmented enterprise network, and a home network connected through a cable modem to a routed WAN. I also designed a wireless site survey form for a client engagement.</p>

<h2 id="networks">Networks I built</h2>
<ol class="wl-builds">
  <li>
    <h3>Connect a wireless router</h3>
    <p>Set up a wireless router serving a wired PC, a wireless laptop, a switch, and a server.</p>
    <ul>
      <li>Configured the router's internet-facing IP address, subnet mask, and default gateway</li>
      <li>Set up its DHCP server pool, changed the admin password, and set the SSID</li>
      <li>Switched the PC to get its address through DHCP</li>
      <li>Verified the laptop could reach the server with ping</li>
    </ul>
    <div class="wl-figs">
      <figure class="wl-shot"><img src="{{ img }}lab2-topology.png" alt="Topology: PC0 and Switch0 wired to wireless router WRS1, Server0 on the switch, CompanyLaptop connected wirelessly" loading="lazy"><figcaption>The finished topology. The dashed line is the laptop's wireless link.</figcaption></figure>
      <figure class="wl-shot"><img src="{{ img }}lab2-ping.png" alt="Ping to 192.168.50.1 with 4 replies and 0% loss" loading="lazy"><figcaption>The laptop reaching the server: 4 sent, 4 received, 0% loss.</figcaption></figure>
    </div>
  </li>
  <li>
    <h3>Configure a Linksys router</h3>
    <p>Configured a Linksys router for a wired host and a wireless laptop, and secured the wireless side.</p>
    <ul>
      <li>Set the router's internet IP, DHCP pool, DNS server, and admin password</li>
      <li>Chose the wireless network mode and set the SSID</li>
      <li>Secured the wireless network with WPA2-Personal and a passphrase</li>
      <li>Tested connectivity with ping</li>
    </ul>
    <div class="wl-figs">
      <figure class="wl-shot"><img src="{{ img }}lab3-topology.png" alt="Topology: Host-A wired and Laptop wireless to a Linksys router" loading="lazy"><figcaption>Host-A wired and the laptop wireless.</figcaption></figure>
      <figure class="wl-shot"><img src="{{ img }}lab3-ping.png" alt="Ping to 172.31.1.1 with 4 replies and 0% loss" loading="lazy"><figcaption>Ping test: 4 for 4 replies, 0% loss.</figcaption></figure>
    </div>
  </li>
  <li>
    <h3>Secure wireless connectivity in an enterprise LAN</h3>
    <p>Added a WRT300N wireless router to an enterprise LAN that's segmented into VLANs 10, 20, and 88, with router subinterfaces handling traffic between them.</p>
    <ul>
      <li>Connected the wireless router to the switch on the VLAN 88 port</li>
      <li>Configured its internet connection, default gateway, and admin password</li>
      <li>Secured the wireless LAN with WPA2-Personal and set the SSID</li>
      <li>Joined PC3 to the wireless LAN in infrastructure mode</li>
    </ul>
    <div class="wl-figs">
      <figure class="wl-shot"><img src="{{ img }}lab4-topology.png" alt="Topology: enterprise LAN with router R1 subinterfaces for VLANs 10, 20, and 88, switch S1, PC1 and PC2, and wireless router WRS2 serving PC3 on a wireless LAN" loading="lazy"><figcaption>The enterprise LAN with VLANs on the left and the WPA2-secured wireless LAN on the right.</figcaption></figure>
    </div>
  </li>
  <li>
    <h3>Connect a wired and wireless LAN</h3>
    <p>Physically connected a home network to a routed network, choosing the right cable and port for every link.</p>
    <ul>
      <li>Connected a configuration terminal to Router0's console port</li>
      <li>Linked Router0 and Router1 over a serial connection, and Router1 to a switch</li>
      <li>Connected a cable modem to the cloud over coax and to the home wireless router</li>
      <li>Wired the family PC to the wireless router, with the home PC and printer on wireless</li>
    </ul>
    <div class="wl-figs">
      <figure class="wl-shot"><img src="{{ img }}lab5-topology.png" alt="Topology: Router0 and Router1 linked by serial, a switch, a server, a cloud, a cable modem, and a home wireless router serving a home PC, family PC, and printer" loading="lazy"><figcaption>The finished network: routers and serial link on the left, the home network on the right.</figcaption></figure>
    </div>
  </li>
</ol>

<h2 id="concepts">Configuration choices I had to understand</h2>
<div class="wl-concepts">
  <div><h3>Disabled vs. mixed network mode</h3><p>Disable the radio when nothing on the network needs wireless, so the router isn't broadcasting a signal it doesn't need. Use mixed mode when clients run different 802.11 standards and still need to share one network.</p></div>
  <div><h3>Hidden SSIDs</h3><p>When an access point doesn't broadcast its SSID, a device can still connect, but only if it's configured with the exact network name and the right security credentials.</p></div>
  <div><h3>WPA2-Personal vs. Enterprise</h3><p>Personal authenticates every device with one pre-shared key. Enterprise authenticates each user through IEEE 802.1X and a RADIUS server.</p></div>
</div>

<h2 id="survey">Planning a wireless site survey</h2>
<p>For a hypothetical client engagement, I designed a site survey form covering what a technician needs to capture before recommending where access points should go.</p>
<div class="wl-table-wrap">
<table class="wl-table">
  <thead><tr><th>Item</th><th>Why it matters</th></tr></thead>
  <tbody>
    <tr><td>Client / organization</td><td>Who the survey is for</td></tr>
    <tr><td>Survey date and time</td><td>When measurements were taken</td></tr>
    <tr><td>Survey technician</td><td>Who performed the survey</td></tr>
    <tr><td>Building location</td><td>The exact address or area being surveyed</td></tr>
    <tr><td>Building floor plan</td><td>Physical features like walls that affect signal</td></tr>
    <tr><td>Construction details</td><td>What the space is built from</td></tr>
    <tr><td>Access points</td><td>Details on any existing access points</td></tr>
    <tr><td>Frequency bands</td><td>Which bands the networks are using</td></tr>
    <tr><td>Channel width</td><td>Spotting congested channels and channel utilization</td></tr>
    <tr><td>Security mode</td><td>Required authentication and encryption</td></tr>
    <tr><td>SNR</td><td>Wireless signal quality</td></tr>
    <tr><td>Recommended AP locations</td><td>The best placements for the environment</td></tr>
    <tr><td>Security findings and recommendations</td><td>Results of the survey and next steps</td></tr>
    <tr><td>Final approval</td><td>Sign-off from the client</td></tr>
  </tbody>
</table>
</div>

<p>I also compared site survey tools and recommended one for each size of job:</p>
<div class="wl-tools">
  <div><h3>NetSpot</h3><p class="fit">Everyday surveys</p><p>Combines Wi-Fi discovery, heatmaps, and interference analysis to find weak signal areas and overlapping access points.</p></div>
  <div><h3>Acrylic Wi-Fi Heatmaps</h3><p class="fit">Deeper RF analysis</p><p>Maps RSSI, SNR, channel utilization, and signal overlap, and its advanced version adds monitor-mode captures and spectrum analysis.</p></div>
  <div><h3>Ekahau AI Pro</h3><p class="fit">Enterprise deployments</p><p>Built for large or complex sites that need predictive planning, capacity planning, and precise AP placement.</p></div>
</div>

<h2 id="learned">What I learned</h2>
<!-- TODO (Angel): Edit this into your own words. You didn't submit write-ups for these labs, so this is a starting point, not your voice yet. -->
<p>Every network came down to the same loop: configure it, connect it, then prove it works. Getting a router's addressing, DHCP, and security settings right matters as much as choosing the right cable for each link, and a successful ping is the quickest proof that all of it lines up.</p>

<h2 id="skills">Skills developed</h2>
<ul class="wl-tags">
  <li>Wireless router configuration</li><li>WPA2 security</li><li>DHCP</li><li>Network cabling</li>
  <li>Connectivity testing</li><li>Site survey planning</li>
</ul>
</div>
