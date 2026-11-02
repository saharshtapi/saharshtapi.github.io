---
layout: page
body_class: pf-page
title: About
permalink: /about/
---

<section class="pf-section">
  <p class="pf-prompt">~/portfolio <span class="pf-sym">$</span> <span class="pf-cmd">cat about.md</span></p>
  <h1 class="pf-name" style="font-size: 2.2rem;">Saharsh Agrawal</h1>
  <p class="pf-role"><span class="pf-dot"></span> Security Researcher <span class="pf-sep">&middot;</span> Threat Intelligence <span class="pf-sep">&middot;</span> Pentester</p>

  <p class="pf-tagline">
    Hi there! I'm a security researcher who spends most of my time finding bugs in web applications,
    taking apart malware campaigns, and writing up exactly how the attack worked. I care about the
    part after the exploit: the detection, the write-up, the tooling that makes the next hunt faster.
  </p>
  <p class="pf-contact-lead">
    Everything published on this site is my own work &mdash; CVE analysis, CTF walkthroughs,
    threat research and the tools I build along the way. When I'm not in front of a terminal
    you'll find me out on the racetrack.
  </p>
</section>

<section class="pf-section">
  <h2 class="pf-h2"><span class="pf-h2-prompt">$</span> cat ./focus.md</h2>
  <div class="pf-grid pf-grid-2">
    <article class="pf-card">
      <h3 class="pf-card-title"><i class="fas fa-bug"></i> Vulnerability Research</h3>
      <p>Finding and reporting real vulnerabilities in production web applications &mdash; from open
      redirects and access-control flaws to injection issues &mdash; and writing them up with a
      reproducible proof of concept.</p>
    </article>
    <article class="pf-card">
      <h3 class="pf-card-title"><i class="fas fa-crosshairs"></i> Penetration Testing</h3>
      <p>Full-scope offensive engagements against infrastructure and applications, from initial
      reconnaissance through to privilege escalation and lateral movement.</p>
    </article>
    <article class="pf-card">
      <h3 class="pf-card-title"><i class="fas fa-radiation"></i> Threat Intelligence</h3>
      <p>Tracking how commodity malware is delivered and updated &mdash; PaperCut exploitation,
      IcedID, Qakbot, OneNote campaigns and Aurora Stealer &mdash; and turning that research into
      detections teams can actually deploy.</p>
    </article>
    <article class="pf-card">
      <h3 class="pf-card-title"><i class="fas fa-terminal"></i> Automation &amp; Tooling</h3>
      <p>Building the small tools that remove the repetitive parts of a hunt: subdomain enumeration
      wrappers, data pipelines and analysis scripts that make the work repeatable.</p>
    </article>
  </div>
</section>

<section class="pf-section">
  <h2 class="pf-h2"><span class="pf-h2-prompt">$</span> git log --oneline --reverse</h2>
  <ul class="pf-timeline">
    <li>
      <span class="pf-timeline-year">2020</span>
      <div class="pf-timeline-body">
        <h3>Started publishing CTF walkthroughs</h3>
        <p>Wrote up TryHackMe rooms from first blood to root &mdash; Lazy Admin, Pickle Rick, Agent
        Sudo, Ignite, Tomghost, Anthem, Vulnversity, Kenobi and more &mdash; documenting every
        command and every dead end along the way.</p>
      </div>
    </li>
    <li>
      <span class="pf-timeline-year">2021</span>
      <div class="pf-timeline-body">
        <h3>Built Sub3num and shipped more writeups</h3>
        <p>Created <a href="https://github.com/saharshtapi/sub3num" target="_blank" rel="noopener">Sub3num</a>,
        a subdomain-enumeration wrapper that chains Sublist3r, Assetfinder, Subfinder, Findomain,
        Amass, httprobe and subjack into one pass. Continued with the Overpass, ColddBox and
        Advent of Cyber 3 writeups.</p>
      </div>
    </li>
    <li>
      <span class="pf-timeline-year">2022</span>
      <div class="pf-timeline-body">
        <h3>Shipped NEPSE FloorSheet Analysis</h3>
        <p>Built a Python, Pandas and NumPy pipeline that pulls and analyses NEPSE floor sheet data,
        turning a raw daily dump into something you can actually read and trade off.</p>
      </div>
    </li>
    <li>
      <span class="pf-timeline-year">2023</span>
      <div class="pf-timeline-body">
        <h3>Published threat research with Loginsoft</h3>
        <p>Co-authored four articles on active intrusion chains &mdash; exploitation of CVE-2023-27350
        in PaperCut by Cl0p, LockBit and TrueBot; the evolving IcedID malware family; the OneNote
        delivery campaign; and the Aurora Stealer campaign.</p>
        <p><a href="{{ '/blogs/' | relative_url }}">Read the articles &rarr;</a></p>
      </div>
    </li>
    <li class="pf-timeline-highlight">
      <span class="pf-timeline-year">2025</span>
      <div class="pf-timeline-body">
        <h3>CVE-2025-47789 published</h3>
        <p>Reported and disclosed an open redirect vulnerability (CWE-601) in the Horilla HRMS
        platform, with a full proof of concept and remediation guidance.</p>
        <p><a href="{{ '/CVES/' | relative_url }}">Read the analysis &rarr;</a></p>
      </div>
    </li>
  </ul>
</section>

<section class="pf-section">
  <h2 class="pf-h2"><span class="pf-h2-prompt">$</span> cat ./skills.txt</h2>
  <div class="pf-grid pf-grid-3">
    <article class="pf-card">
      <h3 class="pf-card-title">Offensive</h3>
      <ul class="pf-skill-list">
        <li>Web application security</li>
        <li>Exploit development &amp; PoC writing</li>
        <li>Privilege escalation &amp; lateral movement</li>
        <li>API and authentication testing</li>
        <li>Network service enumeration</li>
      </ul>
    </article>
    <article class="pf-card">
      <h3 class="pf-card-title">Defensive &amp; research</h3>
      <ul class="pf-skill-list">
        <li>Malware analysis &amp; reverse engineering</li>
        <li>Threat hunting &amp; OSINT</li>
        <li>Detection engineering (Osquery, Sigma)</li>
        <li>Incident response</li>
        <li>CVE research &amp; disclosure</li>
      </ul>
    </article>
    <article class="pf-card">
      <h3 class="pf-card-title">Tooling</h3>
      <ul class="pf-skill-list">
        <li>Burp Suite, Nuclei, Nmap, Nessus</li>
        <li>Ghidra, IDA, Volatility</li>
        <li>Wireshark, Sysmon, Zeek</li>
        <li>Python, Bash, PowerShell</li>
        <li>Pandas, NumPy, Jupyter</li>
      </ul>
    </article>
  </div>
</section>

<section class="pf-section pf-contact">
  <h2 class="pf-h2"><span class="pf-h2-prompt">$</span> contact --info</h2>
  <p class="pf-contact-lead">
    Open to security research roles, freelance assessments, and collaboration on tooling or
    interesting problems. The fastest way to reach me is email.
  </p>
  <ul class="pf-contact-list">
    <li><i class="fas fa-envelope"></i><a href="mailto:saharshtapi@gmail.com">saharshtapi@gmail.com</a></li>
    <li><i class="fab fa-github"></i><a href="https://github.com/saharshtapi" target="_blank" rel="noopener">github.com/saharshtapi</a></li>
    <li><i class="fab fa-linkedin-in"></i><a href="https://www.linkedin.com/in/saharsh-agrawal-146b991b4/" target="_blank" rel="noopener">linkedin.com/in/saharsh-agrawal</a></li>
    <li><i class="fab fa-twitter-square"></i><a href="https://twitter.com/saharshtapi" target="_blank" rel="noopener">@saharshtapi</a></li>
    <li><i class="fas fa-mug-hot"></i><a href="https://www.buymeacoffee.com/saharshtapi" target="_blank" rel="noopener">buymeacoffee.com/saharshtapi</a></li>
  </ul>
</section>
