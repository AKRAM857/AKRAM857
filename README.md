<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Akram Khoulid — Infrastructure Security Engineer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400;600;700&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg:        #0a0e1a;
    --surface:   #111827;
    --surface2:  #1a2035;
    --border:    #1e2d4a;
    --cyan:      #00d4aa;
    --cyan-dim:  #00d4aa22;
    --purple:    #7c3aed;
    --purple-dim:#7c3aed22;
    --text:      #e2e8f0;
    --muted:     #64748b;
    --mono:      'JetBrains Mono', monospace;
    --sans:      'Inter', sans-serif;
  }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--sans);
    font-size: 16px;
    line-height: 1.7;
    overflow-x: hidden;
  }

  /* ── SCROLLBAR ── */
  ::-webkit-scrollbar { width: 4px; }
  ::-webkit-scrollbar-track { background: var(--bg); }
  ::-webkit-scrollbar-thumb { background: var(--cyan); border-radius: 2px; }

  /* ── NOISE OVERLAY ── */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.03'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 0;
    opacity: 0.4;
  }

  /* ── NAV ── */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1rem 3rem;
    background: rgba(10,14,26,0.85);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
  }

  .nav-logo {
    font-family: var(--mono);
    font-size: 0.85rem;
    color: var(--cyan);
    letter-spacing: 0.05em;
  }

  .nav-links {
    display: flex;
    gap: 2rem;
    list-style: none;
  }

  .nav-links a {
    font-family: var(--mono);
    font-size: 0.78rem;
    color: var(--muted);
    text-decoration: none;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    transition: color 0.2s;
  }

  .nav-links a:hover { color: var(--cyan); }

  /* ── HERO ── */
  #hero {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 8rem 3rem 4rem;
    position: relative;
    max-width: 1100px;
    margin: 0 auto;
  }

  .hero-eyebrow {
    font-family: var(--mono);
    font-size: 0.78rem;
    color: var(--cyan);
    letter-spacing: 0.15em;
    text-transform: uppercase;
    margin-bottom: 1.5rem;
    display: flex;
    align-items: center;
    gap: 0.75rem;
  }

  .hero-eyebrow::before {
    content: '';
    display: block;
    width: 2rem;
    height: 1px;
    background: var(--cyan);
  }

  h1 {
    font-family: var(--mono);
    font-size: clamp(2.5rem, 6vw, 4.5rem);
    font-weight: 700;
    line-height: 1.1;
    letter-spacing: -0.02em;
    margin-bottom: 0.5rem;
  }

  h1 span { color: var(--cyan); }

  .hero-role {
    font-family: var(--mono);
    font-size: clamp(1rem, 2.5vw, 1.4rem);
    color: var(--muted);
    margin-bottom: 2rem;
    min-height: 2rem;
  }

  .cursor {
    display: inline-block;
    width: 2px;
    height: 1.2em;
    background: var(--cyan);
    margin-left: 2px;
    vertical-align: middle;
    animation: blink 1s step-end infinite;
  }

  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }

  .hero-desc {
    font-size: 1.05rem;
    color: var(--muted);
    max-width: 560px;
    line-height: 1.8;
    margin-bottom: 2.5rem;
  }

  .hero-links {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
  }

  .btn {
    font-family: var(--mono);
    font-size: 0.82rem;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    padding: 0.75rem 1.75rem;
    border-radius: 4px;
    text-decoration: none;
    transition: all 0.2s;
    cursor: pointer;
    border: none;
  }

  .btn-primary {
    background: var(--cyan);
    color: var(--bg);
    font-weight: 700;
  }

  .btn-primary:hover {
    background: #00f5c4;
    box-shadow: 0 0 24px var(--cyan);
    transform: translateY(-1px);
  }

  .btn-ghost {
    background: transparent;
    color: var(--cyan);
    border: 1px solid var(--border);
  }

  .btn-ghost:hover {
    border-color: var(--cyan);
    background: var(--cyan-dim);
    transform: translateY(-1px);
  }

  /* ── GRID BG ── */
  .grid-bg {
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(0,212,170,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,212,170,0.03) 1px, transparent 1px);
    background-size: 60px 60px;
    pointer-events: none;
    z-index: -1;
  }

  /* ── GLOW ORBS ── */
  .orb {
    position: fixed;
    border-radius: 50%;
    filter: blur(100px);
    pointer-events: none;
    z-index: -1;
    animation: float 8s ease-in-out infinite;
  }

  .orb-1 {
    width: 500px; height: 500px;
    background: rgba(0,212,170,0.06);
    top: -100px; right: -100px;
  }

  .orb-2 {
    width: 400px; height: 400px;
    background: rgba(124,58,237,0.05);
    bottom: 20%; left: -100px;
    animation-delay: -4s;
  }

  @keyframes float {
    0%,100% { transform: translate(0,0); }
    50% { transform: translate(20px, -20px); }
  }

  /* ── SECTIONS ── */
  section {
    padding: 6rem 3rem;
    max-width: 1100px;
    margin: 0 auto;
  }

  .section-label {
    font-family: var(--mono);
    font-size: 0.72rem;
    color: var(--cyan);
    letter-spacing: 0.2em;
    text-transform: uppercase;
    margin-bottom: 0.75rem;
    display: flex;
    align-items: center;
    gap: 0.75rem;
  }

  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
    max-width: 80px;
  }

  h2 {
    font-family: var(--mono);
    font-size: clamp(1.6rem, 3vw, 2.2rem);
    font-weight: 700;
    margin-bottom: 0.75rem;
    letter-spacing: -0.02em;
  }

  .section-desc {
    color: var(--muted);
    font-size: 1rem;
    max-width: 560px;
    margin-bottom: 3rem;
  }

  /* ── STATS ── */
  .stats-row {
    display: flex;
    gap: 3rem;
    flex-wrap: wrap;
    margin-bottom: 4rem;
    padding: 2rem;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
  }

  .stat {
    display: flex;
    flex-direction: column;
  }

  .stat-num {
    font-family: var(--mono);
    font-size: 2rem;
    font-weight: 700;
    color: var(--cyan);
    line-height: 1;
  }

  .stat-label {
    font-size: 0.82rem;
    color: var(--muted);
    margin-top: 0.25rem;
    font-family: var(--mono);
  }

  /* ── PROJECTS ── */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 1.5rem;
  }

  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 2rem;
    position: relative;
    overflow: hidden;
    transition: all 0.3s;
    cursor: pointer;
  }

  .project-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--cyan), var(--purple));
    transform: scaleX(0);
    transition: transform 0.3s;
    transform-origin: left;
  }

  .project-card:hover {
    border-color: var(--cyan);
    transform: translateY(-4px);
    box-shadow: 0 16px 40px rgba(0,212,170,0.08);
  }

  .project-card:hover::before { transform: scaleX(1); }

  .project-card.flagship {
    grid-column: 1 / -1;
    border-color: rgba(0,212,170,0.3);
    background: linear-gradient(135deg, var(--surface) 0%, rgba(0,212,170,0.03) 100%);
  }

  .project-card.flagship::before { transform: scaleX(1); }

  .project-badge {
    font-family: var(--mono);
    font-size: 0.68rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    padding: 0.25rem 0.6rem;
    border-radius: 3px;
    display: inline-block;
    margin-bottom: 1rem;
  }

  .badge-flagship {
    background: var(--cyan-dim);
    color: var(--cyan);
    border: 1px solid rgba(0,212,170,0.3);
  }

  .badge-security {
    background: var(--purple-dim);
    color: #a78bfa;
    border: 1px solid rgba(124,58,237,0.3);
  }

  .badge-network {
    background: rgba(59,130,246,0.1);
    color: #60a5fa;
    border: 1px solid rgba(59,130,246,0.2);
  }

  .project-title {
    font-family: var(--mono);
    font-size: 1.1rem;
    font-weight: 600;
    margin-bottom: 0.75rem;
    color: var(--text);
  }

  .project-desc {
    font-size: 0.9rem;
    color: var(--muted);
    line-height: 1.7;
    margin-bottom: 1.5rem;
  }

  .project-stack {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-bottom: 1.5rem;
  }

  .stack-tag {
    font-family: var(--mono);
    font-size: 0.72rem;
    padding: 0.2rem 0.6rem;
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 3px;
    color: var(--muted);
  }

  .project-highlights {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 0.4rem;
  }

  .project-highlights li {
    font-size: 0.85rem;
    color: var(--muted);
    display: flex;
    gap: 0.5rem;
    align-items: flex-start;
  }

  .project-highlights li::before {
    content: '→';
    color: var(--cyan);
    flex-shrink: 0;
    font-family: var(--mono);
  }

  /* ── SKILLS ── */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1.5rem;
  }

  .skill-group {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 1.75rem;
    transition: border-color 0.2s;
  }

  .skill-group:hover { border-color: rgba(0,212,170,0.3); }

  .skill-group-title {
    font-family: var(--mono);
    font-size: 0.78rem;
    color: var(--cyan);
    letter-spacing: 0.12em;
    text-transform: uppercase;
    margin-bottom: 1rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }

  .skill-pills {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
  }

  .pill {
    font-family: var(--mono);
    font-size: 0.75rem;
    padding: 0.3rem 0.7rem;
    border-radius: 3px;
    background: var(--surface2);
    border: 1px solid var(--border);
    color: var(--text);
    transition: all 0.2s;
  }

  .pill:hover {
    border-color: var(--cyan);
    color: var(--cyan);
    background: var(--cyan-dim);
  }

  /* ── TERMINAL BLOCK ── */
  .terminal {
    background: #060a14;
    border: 1px solid var(--border);
    border-radius: 8px;
    overflow: hidden;
    margin-top: 3rem;
  }

  .terminal-bar {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    padding: 0.75rem 1rem;
    background: var(--surface);
    border-bottom: 1px solid var(--border);
  }

  .dot { width: 12px; height: 12px; border-radius: 50%; }
  .dot-red { background: #ff5f57; }
  .dot-yellow { background: #febc2e; }
  .dot-green { background: #28c840; }

  .terminal-title {
    font-family: var(--mono);
    font-size: 0.75rem;
    color: var(--muted);
    margin-left: auto;
    margin-right: auto;
  }

  .terminal-body {
    padding: 1.5rem;
    font-family: var(--mono);
    font-size: 0.82rem;
    line-height: 2;
  }

  .t-prompt { color: var(--cyan); }
  .t-cmd { color: var(--text); }
  .t-comment { color: var(--muted); }
  .t-output { color: #94a3b8; }
  .t-success { color: #4ade80; }
  .t-highlight { color: #fbbf24; }

  /* ── KNOWLEDGE BASE ── */
  .kb-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 1rem;
  }

  .kb-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 1.5rem;
    transition: all 0.2s;
  }

  .kb-card:hover {
    border-color: rgba(0,212,170,0.3);
    transform: translateY(-2px);
  }

  .kb-icon {
    font-size: 1.5rem;
    margin-bottom: 0.75rem;
  }

  .kb-title {
    font-family: var(--mono);
    font-size: 0.88rem;
    font-weight: 600;
    margin-bottom: 0.4rem;
  }

  .kb-meta {
    font-family: var(--mono);
    font-size: 0.72rem;
    color: var(--cyan);
    margin-bottom: 0.5rem;
  }

  .kb-desc {
    font-size: 0.82rem;
    color: var(--muted);
    line-height: 1.6;
  }

  /* ── CONTACT ── */
  #contact {
    border-top: 1px solid var(--border);
  }

  .contact-grid {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
  }

  .contact-link {
    font-family: var(--mono);
    font-size: 0.82rem;
    letter-spacing: 0.08em;
    text-decoration: none;
    color: var(--muted);
    padding: 0.75rem 1.25rem;
    border: 1px solid var(--border);
    border-radius: 4px;
    transition: all 0.2s;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }

  .contact-link:hover {
    color: var(--cyan);
    border-color: var(--cyan);
    background: var(--cyan-dim);
  }

  /* ── FOOTER ── */
  footer {
    text-align: center;
    padding: 2rem;
    font-family: var(--mono);
    font-size: 0.72rem;
    color: var(--muted);
    border-top: 1px solid var(--border);
  }

  /* ── FADE IN ON SCROLL ── */
  .fade-in {
    opacity: 0;
    transform: translateY(24px);
    transition: opacity 0.6s ease, transform 0.6s ease;
  }

  .fade-in.visible {
    opacity: 1;
    transform: translateY(0);
  }

  /* ── RESPONSIVE ── */
  @media (max-width: 768px) {
    nav { padding: 1rem 1.5rem; }
    .nav-links { display: none; }
    section { padding: 4rem 1.5rem; }
    #hero { padding: 7rem 1.5rem 3rem; }
    .stats-row { gap: 1.5rem; }
    .project-card.flagship { grid-column: auto; }
  }

  @media (prefers-reduced-motion: reduce) {
    .fade-in { opacity: 1; transform: none; }
    .orb { animation: none; }
    .cursor { animation: none; }
  }
</style>
</head>
<body>

<div class="grid-bg"></div>
<div class="orb orb-1"></div>
<div class="orb orb-2"></div>

<!-- NAV -->
<nav>
  <div class="nav-logo">~/akram-khoulid</div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#knowledge">Knowledge</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<div id="hero">
  <div class="hero-eyebrow">Networks & Telecom Engineering · ENSA Safi</div>
  <h1>Akram<br><span>Khoulid</span></h1>
  <div class="hero-role" id="typed-role"><span class="cursor"></span></div>
  <p class="hero-desc">
    I build infrastructure from scratch, harden it layer by layer, and document every decision. 
    My work lives at the intersection of Linux systems, network security, and Zero-Trust architecture.
  </p>
  <div class="hero-links">
    <a href="#projects" class="btn btn-primary">View Projects</a>
    <a href="https://www.linkedin.com/in/akram-khoulid-08aa4435a/" target="_blank" class="btn btn-ghost">LinkedIn</a>
    <a href="https://github.com/AKRAM857" target="_blank" class="btn btn-ghost">GitHub</a>
  </div>
</div>

<!-- ABOUT -->
<section id="about">
  <div class="section-label">About</div>
  <h2>Build. Break. Understand.</h2>
  <p class="section-desc">
    Third-year engineering student focused on the infrastructure security stack — from kernel-level packet 
    filtering to cryptographic access control. I don't follow tutorials. I build systems from first principles.
  </p>

  <div class="stats-row fade-in">
    <div class="stat">
      <span class="stat-num" data-target="70">0</span><span class="stat-num">+</span>
      <span class="stat-label">pages documented</span>
    </div>
    <div class="stat">
      <span class="stat-num" data-target="44">0</span><span class="stat-num">k+</span>
      <span class="stat-label">alerts detected (Wazuh)</span>
    </div>
    <div class="stat">
      <span class="stat-num" data-target="3">0</span>
      <span class="stat-label">infrastructure projects</span>
    </div>
    <div class="stat">
      <span class="stat-num" data-target="6">0</span>
      <span class="stat-label">knowledge bases maintained</span>
    </div>
  </div>

  <div class="terminal fade-in">
    <div class="terminal-bar">
      <div class="dot dot-red"></div>
      <div class="dot dot-yellow"></div>
      <div class="dot dot-green"></div>
      <span class="terminal-title">akram@bastion:~</span>
    </div>
    <div class="terminal-body">
      <div><span class="t-prompt">akram@bastion</span><span class="t-cmd"> ~ $ </span><span class="t-highlight">whoami</span></div>
      <div class="t-output">Networks & Telecom Engineer · DevSecOps Track · ENSA Safi</div>
      <br>
      <div><span class="t-prompt">akram@bastion</span><span class="t-cmd"> ~ $ </span><span class="t-highlight">cat philosophy.txt</span></div>
      <div class="t-output">"The best way to learn is to break things,</div>
      <div class="t-output"> understand why they broke, and document everything."</div>
      <br>
      <div><span class="t-prompt">akram@bastion</span><span class="t-cmd"> ~ $ </span><span class="t-highlight">nft list ruleset | grep policy</span></div>
      <div class="t-success">policy drop; <span class="t-comment"># secure by default</span></div>
      <br>
      <div><span class="t-prompt">akram@bastion</span><span class="t-cmd"> ~ $ </span><span class="t-highlight">id developer1</span></div>
      <div class="t-output">uid=1001(developer1) gid=1001(devs) groups=1001(devs)</div>
      <br>
      <div><span class="t-prompt">akram@bastion</span><span class="t-cmd"> ~ $ </span><span class="t-highlight">sudo -l -U developer1 | grep NOPASSWD</span></div>
      <div class="t-success">    (root) NOPASSWD: /usr/bin/systemctl restart apache2</div>
      <div class="t-comment">    # exactly one command. nothing more.</div>
      <br>
      <div><span class="t-prompt">akram@bastion</span><span class="t-cmd"> ~ $ </span><span class="t-highlight">_</span><span class="cursor"></span></div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="section-label">Projects</div>
  <h2>What I've Built</h2>
  <p class="section-desc">Real systems, real environments, real problems. Every project produces working infrastructure and complete documentation.</p>

  <div class="projects-grid">

    <!-- FLAGSHIP -->
    <div class="project-card flagship fade-in">
      <span class="project-badge badge-flagship">Flagship Project</span>
      <div class="project-title">Zero-Trust SSH Bastion Host Infrastructure</div>
      <p class="project-desc">
        A complete enterprise-grade secure access environment built from scratch in VirtualBox. 
        Dual-interface network segmentation, cryptographic identity verification, role-based access control, 
        stateful firewalling, and kernel-level audit telemetry — every layer designed, implemented, and validated.
      </p>
      <div class="project-stack">
        <span class="stack-tag">Ubuntu 25.10</span>
        <span class="stack-tag">Kali Linux</span>
        <span class="stack-tag">OpenSSH</span>
        <span class="stack-tag">nftables</span>
        <span class="stack-tag">fail2ban</span>
        <span class="stack-tag">auditd</span>
        <span class="stack-tag">Apache</span>
        <span class="stack-tag">VirtualBox</span>
      </div>
      <ul class="project-highlights">
        <li>Dual-interface architecture — enp0s3 public / enp0s8 private with NAT masquerade for backend server internet access</li>
        <li>SSH hardened to keys-only with ProxyJump blind tunneling — private key never leaves the client machine</li>
        <li>RBAC implementation — devs, ops, auditors with precisely scoped filesystem permissions and sudo policies</li>
        <li>nftables stateful ruleset — BastionRules table with connection tracking, default-drop policy on all chains</li>
        <li>70+ page technical report documenting every architectural decision and its security reasoning</li>
      </ul>
    </div>

    <!-- WAZUH -->
    <div class="project-card fade-in">
      <span class="project-badge badge-security">SIEM / XDR</span>
      <div class="project-title">Wazuh SIEM Lab — Threat Detection</div>
      <p class="project-desc">
        Complete Wazuh v4.14.4 XDR/SIEM deployment monitoring a Kali Linux attack machine over a custom OVS/VLAN network. 
        Simulated SSH brute force and detected 44,000+ alerts correlated against MITRE ATT&CK.
      </p>
      <div class="project-stack">
        <span class="stack-tag">Wazuh v4.14.4</span>
        <span class="stack-tag">Filebeat OSS</span>
        <span class="stack-tag">OpenSearch</span>
        <span class="stack-tag">Ubuntu</span>
        <span class="stack-tag">Kali</span>
      </div>
      <ul class="project-highlights">
        <li>Custom OVS/VLAN network — attack and defense machines isolated on separate segments</li>
        <li>44,000+ brute force alerts detected and visualized in real time</li>
        <li>MITRE ATT&CK framework correlation — mapped attack techniques to detection rules</li>
      </ul>
    </div>

    <!-- ROUTER -->
    <div class="project-card fade-in">
      <span class="project-badge badge-network">Networking</span>
      <div class="project-title">Linux Router — DHCP, DNS & SDN</div>
      <p class="project-desc">
        Ubuntu VM configured as a complete software-defined network router. BIND9 DNS, isc-dhcp-server, 
        Open vSwitch VLAN segmentation, NAT masquerading, and inter-VLAN routing for multiple client machines.
      </p>
      <div class="project-stack">
        <span class="stack-tag">Ubuntu</span>
        <span class="stack-tag">Open vSwitch</span>
        <span class="stack-tag">BIND9</span>
        <span class="stack-tag">isc-dhcp-server</span>
        <span class="stack-tag">iptables</span>
      </div>
      <ul class="project-highlights">
        <li>Full SDN stack on a single VM — DHCP · DNS · VLAN · NAT · inter-VLAN routing</li>
        <li>OVS VLAN trunking with tagged ports and internal bridge interfaces</li>
        <li>BIND9 authoritative DNS with forward and reverse lookup zones</li>
      </ul>
    </div>

  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="section-label">Skills</div>
  <h2>Core Competencies</h2>
  <p class="section-desc">Built through hands-on projects, not certifications. Every skill here has been tested on real systems.</p>

  <div class="skills-grid fade-in">
    <div class="skill-group">
      <div class="skill-group-title">⚙️ Linux Administration</div>
      <div class="skill-pills">
        <span class="pill">Ubuntu Server</span>
        <span class="pill">systemd</span>
        <span class="pill">user management</span>
        <span class="pill">RBAC</span>
        <span class="pill">file permissions</span>
        <span class="pill">SUID/SGID</span>
        <span class="pill">umask</span>
        <span class="pill">PAM</span>
        <span class="pill">auditd</span>
        <span class="pill">rsyslog</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-group-title">🔐 Security & Hardening</div>
      <div class="skill-pills">
        <span class="pill">Zero Trust</span>
        <span class="pill">SSH hardening</span>
        <span class="pill">ProxyJump</span>
        <span class="pill">nftables</span>
        <span class="pill">fail2ban</span>
        <span class="pill">least privilege</span>
        <span class="pill">sudo policy</span>
        <span class="pill">key-based auth</span>
        <span class="pill">intrusion detection</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-group-title">🌐 Networking</div>
      <div class="skill-pills">
        <span class="pill">TCP/IP</span>
        <span class="pill">NAT</span>
        <span class="pill">VLAN</span>
        <span class="pill">DHCP</span>
        <span class="pill">DNS / BIND9</span>
        <span class="pill">Open vSwitch</span>
        <span class="pill">network segmentation</span>
        <span class="pill">stateful inspection</span>
        <span class="pill">Netfilter</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-group-title">☁️ Cloud & DevOps</div>
      <div class="skill-pills">
        <span class="pill">AWS</span>
        <span class="pill">IAM</span>
        <span class="pill">Security Groups</span>
        <span class="pill">Docker</span>
        <span class="pill">CI/CD</span>
        <span class="pill">VirtualBox</span>
        <span class="pill">Git</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-group-title">🔍 Detection & Monitoring</div>
      <div class="skill-pills">
        <span class="pill">Wazuh XDR</span>
        <span class="pill">SIEM</span>
        <span class="pill">MITRE ATT&CK</span>
        <span class="pill">log analysis</span>
        <span class="pill">auditd</span>
        <span class="pill">journalctl</span>
        <span class="pill">tcpdump</span>
        <span class="pill">nmap</span>
      </div>
    </div>

    <div class="skill-group">
      <div class="skill-group-title">💻 Languages & Scripting</div>
      <div class="skill-pills">
        <span class="pill">Bash</span>
        <span class="pill">Python</span>
        <span class="pill">C</span>
        <span class="pill">nftables DSL</span>
        <span class="pill">YAML</span>
        <span class="pill">Markdown</span>
      </div>
    </div>
  </div>
</section>

<!-- KNOWLEDGE BASE -->
<section id="knowledge">
  <div class="section-label">Knowledge Base</div>
  <h2>Personal Technical Library</h2>
  <p class="section-desc">
    Every concept I learn gets documented after being understood and tested — not before. 
    These are living reference documents, built command by command.
  </p>

  <div class="kb-grid fade-in">
    <div class="kb-card">
      <div class="kb-icon">🖥️</div>
      <div class="kb-title">Linux Systems Administration</div>
      <div class="kb-meta">Active · 33+ pages</div>
      <div class="kb-desc">Filesystem · users · groups · permissions · services · systemd · process management</div>
    </div>
    <div class="kb-card">
      <div class="kb-icon">🔑</div>
      <div class="kb-title">SSH — Protocol & Theory</div>
      <div class="kb-meta">Active</div>
      <div class="kb-desc">Cryptography · Diffie-Hellman · key exchange · ProxyJump · agent forwarding · hardening directives</div>
    </div>
    <div class="kb-card">
      <div class="kb-icon">🔥</div>
      <div class="kb-title">Firewall & Network Security</div>
      <div class="kb-meta">Active — building now</div>
      <div class="kb-desc">Netfilter framework · nftables architecture · stateful inspection · connection tracking · fail2ban</div>
    </div>
    <div class="kb-card">
      <div class="kb-icon">🏰</div>
      <div class="kb-title">Bastion Host Project Report</div>
      <div class="kb-meta">Active · 70+ pages</div>
      <div class="kb-desc">Full implementation documentation — architecture diagrams · decision rationale · validation testing</div>
    </div>
    <div class="kb-card">
      <div class="kb-icon">🌐</div>
      <div class="kb-title">Network Fundamentals</div>
      <div class="kb-meta">Planned</div>
      <div class="kb-desc">OSI model · TCP/IP · subnetting · routing · NAT · DNS · VLANs · switching</div>
    </div>
    <div class="kb-card">
      <div class="kb-icon">🛡️</div>
      <div class="kb-title">Linux Security</div>
      <div class="kb-meta">Planned</div>
      <div class="kb-desc">Privilege escalation · SUID abuse · sudo misconfigs · capabilities · PAM · incident response</div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-label">Contact</div>
  <h2>Get in Touch</h2>
  <p class="section-desc">Open to internship opportunities, technical discussions, and collaboration on infrastructure projects.</p>

  <div class="contact-grid fade-in">
    <a href="https://www.linkedin.com/in/akram-khoulid-08aa4435a/" target="_blank" class="contact-link">
      <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
      LinkedIn
    </a>
    <a href="https://github.com/AKRAM857" target="_blank" class="contact-link">
      <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
      GitHub
    </a>
    <a href="mailto:akhoulid@gmail.com" class="contact-link">
      <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,12 2,6"/></svg>
      akhoulid@gmail.com
    </a>
  </div>
</section>

<footer>
  <span style="color:var(--cyan)">~/akram-khoulid</span> · Built with intention · Networks & Telecom Engineering · ENSA Safi
</footer>

<script>
// ── TYPING ANIMATION ──
const roles = [
  "Infrastructure Security Engineer",
  "Linux Systems Administrator",
  "Network Security Engineer",
  "DevSecOps Engineer",
  "Zero-Trust Architect",
];

let roleIndex = 0;
let charIndex = 0;
let deleting = false;
const el = document.getElementById('typed-role');

function type() {
  const current = roles[roleIndex];
  const cursor = '<span class="cursor"></span>';

  if (!deleting) {
    charIndex++;
    el.innerHTML = current.slice(0, charIndex) + cursor;
    if (charIndex === current.length) {
      deleting = true;
      setTimeout(type, 2000);
      return;
    }
  } else {
    charIndex--;
    el.innerHTML = current.slice(0, charIndex) + cursor;
    if (charIndex === 0) {
      deleting = false;
      roleIndex = (roleIndex + 1) % roles.length;
    }
  }
  setTimeout(type, deleting ? 40 : 80);
}

setTimeout(type, 800);

// ── COUNTER ANIMATION ──
function animateCount(el, target, duration = 1500) {
  let start = 0;
  const step = target / (duration / 16);
  const timer = setInterval(() => {
    start += step;
    if (start >= target) {
      el.textContent = target;
      clearInterval(timer);
    } else {
      el.textContent = Math.floor(start);
    }
  }, 16);
}

// ── SCROLL ANIMATIONS ──
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('visible');

      // trigger counters when stats section visible
      const nums = entry.target.querySelectorAll('[data-target]');
      nums.forEach(n => animateCount(n, parseInt(n.dataset.target)));

      observer.unobserve(entry.target);
    }
  });
}, { threshold: 0.15 });

document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));

// ── STAGGER PROJECT CARDS ──
document.querySelectorAll('.project-card.fade-in').forEach((card, i) => {
  card.style.transitionDelay = `${i * 0.1}s`;
});

document.querySelectorAll('.kb-card').forEach((card, i) => {
  card.style.transitionDelay = `${i * 0.07}s`;
});
</script>
</body>
</html>
