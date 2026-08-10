<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Subathran J — SOC Analyst L1 | Blue Team Portfolio</title>
<meta name="description" content="Subathran J — aspiring SOC Analyst L1 specializing in threat detection, incident response, and SIEM operations. Home lab projects in Splunk, Wazuh, and MITRE ATT&CK.">
<meta name="keywords" content="SOC Analyst, Blue Team, Cybersecurity, Splunk, Wazuh, Incident Response, Threat Detection, MITRE ATT&CK">
<meta name="author" content="Subathran J">
<meta property="og:title" content="Subathran J — SOC Analyst L1 Portfolio">
<meta property="og:description" content="Threat detection, incident response and SIEM operations — home lab projects and skills.">
<meta property="og:type" content="website">
<link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Crect width='100' height='100' rx='20' fill='%230A192F'/%3E%3Cpath d='M30 50 L45 65 L72 35' stroke='%2300F5A0' stroke-width='9' fill='none' stroke-linecap='round' stroke-linejoin='round'/%3E%3C/svg%3E">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --void:#0A192F;
    --panel:#0D2340;
    --glass:rgba(17,41,71,0.55);
    --glass-border:rgba(136,255,214,0.14);
    --green:#00F5A0;
    --cyan:#22D9F2;
    --amber:#FFB454;
    --text-primary:#E6F1FF;
    --text-secondary:#8FA3C4;
    --text-muted:#5C6E8C;
    --line:rgba(136,255,214,0.10);
    --radius:14px;
    --maxw:1180px;
  }

  *{margin:0;padding:0;box-sizing:border-box;}
  html{scroll-behavior:smooth;}

  body{
    background:var(--void);
    color:var(--text-primary);
    font-family:'Inter',system-ui,sans-serif;
    line-height:1.6;
    overflow-x:hidden;
    position:relative;
  }

  body::before{
    content:'';
    position:fixed;
    inset:0;
    background:
      radial-gradient(ellipse 900px 600px at 15% -10%, rgba(0,245,160,0.08), transparent 60%),
      radial-gradient(ellipse 900px 700px at 90% 20%, rgba(34,217,242,0.07), transparent 60%),
      radial-gradient(ellipse 700px 700px at 50% 100%, rgba(0,245,160,0.05), transparent 60%);
    pointer-events:none;
    z-index:0;
  }

  body::after{
    content:'';
    position:fixed;
    inset:0;
    background-image:
      linear-gradient(rgba(136,255,214,0.025) 1px, transparent 1px),
      linear-gradient(90deg, rgba(136,255,214,0.025) 1px, transparent 1px);
    background-size:48px 48px;
    pointer-events:none;
    z-index:0;
  }

  .wrap{max-width:var(--maxw);margin:0 auto;padding:0 32px;position:relative;z-index:1;}

  h1,h2,h3,h4{font-family:'Space Grotesk',sans-serif;letter-spacing:-0.01em;}
  code, .mono{font-family:'JetBrains Mono',monospace;}
  a{color:inherit;text-decoration:none;}

  /* ============ SCROLL REVEAL ============ */
  .reveal{opacity:0;transform:translateY(24px);transition:opacity .7s cubic-bezier(.16,1,.3,1), transform .7s cubic-bezier(.16,1,.3,1);}
  .reveal.in{opacity:1;transform:translateY(0);}

  @media (prefers-reduced-motion: reduce){
    *{animation-duration:0.01ms !important; animation-iteration-count:1 !important; transition-duration:0.01ms !important; scroll-behavior:auto !important;}
  }

  /* ============ NAV ============ */
  nav{
    position:fixed;top:0;left:0;right:0;z-index:100;
    background:rgba(10,25,47,0.72);
    backdrop-filter:blur(16px) saturate(140%);
    -webkit-backdrop-filter:blur(16px) saturate(140%);
    border-bottom:1px solid var(--line);
  }
  .nav-inner{max-width:var(--maxw);margin:0 auto;padding:16px 32px;display:flex;align-items:center;justify-content:space-between;}
  .brand{display:flex;align-items:center;gap:10px;font-family:'Space Grotesk',sans-serif;font-weight:600;font-size:17px;}
  .brand-mark{
    width:34px;height:34px;border-radius:9px;
    background:linear-gradient(135deg, rgba(0,245,160,0.16), rgba(34,217,242,0.16));
    border:1px solid var(--glass-border);
    display:flex;align-items:center;justify-content:center;
    color:var(--green);font-size:14px;font-weight:700;
  }
  .status-dot{width:7px;height:7px;border-radius:50%;background:var(--green);box-shadow:0 0 8px var(--green);animation:pulse 2s ease-in-out infinite;}
  @keyframes pulse{0%,100%{opacity:1;}50%{opacity:0.35;}}

  .nav-links{display:flex;gap:2px;align-items:center;}
  .nav-links a{
    padding:8px 16px;font-size:14px;color:var(--text-secondary);
    border-radius:8px;transition:color .2s, background .2s;
    font-weight:500;
  }
  .nav-links a:hover{color:var(--text-primary);background:rgba(136,255,214,0.06);}
  .nav-cta{
    padding:9px 18px !important;border-radius:8px;
    background:rgba(0,245,160,0.10);
    border:1px solid rgba(0,245,160,0.35);
    color:var(--green) !important;font-weight:600;font-size:13px !important;
  }
  .nav-cta:hover{background:rgba(0,245,160,0.18) !important;}
  .nav-toggle{display:none;background:none;border:none;color:var(--text-primary);font-size:22px;cursor:pointer;}

  @media (max-width:900px){
    .nav-links{position:fixed;top:66px;left:0;right:0;flex-direction:column;align-items:stretch;
      background:rgba(10,25,47,0.97);backdrop-filter:blur(20px);
      padding:12px 24px 24px;border-bottom:1px solid var(--line);
      transform:translateY(-130%);opacity:0;transition:transform .3s ease, opacity .3s ease;
    }
    .nav-links.open{transform:translateY(0);opacity:1;}
    .nav-links a{padding:14px 8px;border-bottom:1px solid var(--line);border-radius:0;}
    .nav-toggle{display:block;}
  }

  /* ============ GLASS CARD BASE ============ */
  .glass{
    background:var(--glass);
    backdrop-filter:blur(18px) saturate(140%);
    -webkit-backdrop-filter:blur(18px) saturate(140%);
    border:1px solid var(--glass-border);
    border-radius:var(--radius);
  }

  /* ============ HERO ============ */
  header.hero{
    min-height:100vh;
    display:flex;align-items:center;
    padding:130px 0 80px;
    position:relative;
  }
  .hero-grid{
    display:grid;grid-template-columns:1.1fr 0.9fr;gap:56px;align-items:center;
  }
  .eyebrow{
    display:inline-flex;align-items:center;gap:8px;
    font-family:'JetBrains Mono',monospace;font-size:12px;letter-spacing:0.06em;
    color:var(--green);text-transform:uppercase;
    padding:6px 14px;border-radius:20px;
    background:rgba(0,245,160,0.08);border:1px solid rgba(0,245,160,0.25);
    margin-bottom:24px;
  }
  .hero h1{
    font-size:clamp(38px,5.4vw,62px);
    font-weight:700;line-height:1.06;
    margin-bottom:20px;
  }
  .hero h1 .accent{
    background:linear-gradient(90deg, var(--green), var(--cyan));
    -webkit-background-clip:text;background-clip:text;color:transparent;
  }
  .hero-sub{
    font-size:18px;color:var(--text-secondary);max-width:520px;margin-bottom:36px;
  }
  .hero-actions{display:flex;gap:14px;flex-wrap:wrap;margin-bottom:44px;}
  .btn{
    padding:13px 26px;border-radius:9px;font-weight:600;font-size:14.5px;
    display:inline-flex;align-items:center;gap:8px;
    transition:transform .2s, box-shadow .2s, background .2s, border-color .2s;
    cursor:pointer;border:1px solid transparent;
  }
  .btn-primary{
    background:linear-gradient(90deg, var(--green), var(--cyan));
    color:#03140F;
  }
  .btn-primary:hover{transform:translateY(-2px);box-shadow:0 10px 30px rgba(0,245,160,0.25);}
  .btn-ghost{
    background:rgba(136,255,214,0.04);
    border:1px solid var(--glass-border);
    color:var(--text-primary);
  }
  .btn-ghost:hover{border-color:rgba(136,255,214,0.4);transform:translateY(-2px);}

  .hero-stats{display:flex;gap:32px;flex-wrap:wrap;}
  .hstat-num{font-family:'Space Grotesk',sans-serif;font-size:26px;font-weight:700;color:var(--text-primary);}
  .hstat-label{font-size:12.5px;color:var(--text-muted);margin-top:2px;}

  /* ---- Signature element: live alert console ---- */
  .console{
    padding:0;overflow:hidden;
    box-shadow:0 30px 70px -20px rgba(0,0,0,0.6);
  }
  .console-bar{
    display:flex;align-items:center;justify-content:space-between;
    padding:14px 18px;border-bottom:1px solid var(--line);
    background:rgba(255,255,255,0.02);
  }
  .console-dots{display:flex;gap:7px;}
  .console-dots span{width:9px;height:9px;border-radius:50%;background:rgba(255,255,255,0.14);}
  .console-title{font-family:'JetBrains Mono',monospace;font-size:12px;color:var(--text-secondary);letter-spacing:0.03em;}
  .console-live{display:flex;align-items:center;gap:6px;font-family:'JetBrains Mono',monospace;font-size:11px;color:var(--green);}
  .console-body{
    padding:18px;height:340px;overflow:hidden;
    font-family:'JetBrains Mono',monospace;font-size:12.5px;
    display:flex;flex-direction:column;gap:10px;
  }
  .log-line{
    display:flex;gap:10px;align-items:flex-start;
    opacity:0;animation:logIn .5s forwards;
    padding-bottom:10px;border-bottom:1px dashed var(--line);
  }
  @keyframes logIn{to{opacity:1;}}
  .log-time{color:var(--text-muted);white-space:nowrap;}
  .log-tag{
    padding:1px 7px;border-radius:5px;font-size:10.5px;font-weight:600;white-space:nowrap;height:fit-content;
  }
  .tag-benign{background:rgba(0,245,160,0.12);color:var(--green);}
  .tag-investigating{background:rgba(34,217,242,0.12);color:var(--cyan);}
  .tag-escalated{background:rgba(255,180,84,0.14);color:var(--amber);}
  .log-msg{color:var(--text-secondary);}
  .console-footer{
    padding:12px 18px;border-top:1px solid var(--line);
    display:flex;justify-content:space-between;
    font-family:'JetBrains Mono',monospace;font-size:11px;color:var(--text-muted);
  }

  @media (max-width:900px){
    .hero-grid{grid-template-columns:1fr;}
    .console{order:-1;}
  }

  /* ============ SECTION SHELL ============ */
  section{padding:110px 0;position:relative;}
  .section-head{margin-bottom:52px;max-width:640px;}
  .section-eyebrow{
    font-family:'JetBrains Mono',monospace;font-size:12px;color:var(--cyan);
    text-transform:uppercase;letter-spacing:0.08em;margin-bottom:12px;display:block;
  }
  .section-head h2{font-size:clamp(26px,3.4vw,38px);font-weight:600;margin-bottom:14px;}
  .section-head p{color:var(--text-secondary);font-size:16px;}

  /* ============ ABOUT ============ */
  .about-grid{display:grid;grid-template-columns:1fr 1fr;gap:48px;align-items:start;}
  .about-text p{color:var(--text-secondary);margin-bottom:18px;font-size:15.5px;}
  .about-list{list-style:none;display:flex;flex-direction:column;gap:14px;margin-top:8px;}
  .about-list li{display:flex;gap:12px;align-items:flex-start;font-size:14.5px;color:var(--text-secondary);}
  .check{
    flex-shrink:0;width:20px;height:20px;border-radius:6px;
    background:rgba(0,245,160,0.1);border:1px solid rgba(0,245,160,0.3);
    display:flex;align-items:center;justify-content:center;color:var(--green);font-size:11px;margin-top:1px;
  }
  .about-card{padding:28px;}
  .about-card h3{font-size:15px;margin-bottom:18px;color:var(--text-primary);font-weight:600;}
  .cert-row{display:flex;justify-content:space-between;align-items:center;padding:12px 0;border-bottom:1px solid var(--line);font-size:14px;}
  .cert-row:last-child{border-bottom:none;}
  .cert-badge{font-family:'JetBrains Mono',monospace;font-size:10.5px;padding:3px 9px;border-radius:5px;background:rgba(34,217,242,0.1);color:var(--cyan);}

  /* ============ SKILLS ============ */
  .skills-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;}
  .skill-card{padding:26px;transition:border-color .25s, transform .25s;}
  .skill-card:hover{border-color:rgba(0,245,160,0.3);transform:translateY(-4px);}
  .skill-card h3{font-size:14.5px;margin-bottom:20px;display:flex;align-items:center;gap:9px;color:var(--text-primary);}
  .skill-card h3 .dot{width:8px;height:8px;border-radius:50%;}
  .skill-item{margin-bottom:15px;}
  .skill-item:last-child{margin-bottom:0;}
  .skill-item-top{display:flex;justify-content:space-between;font-size:13px;margin-bottom:7px;}
  .skill-item-top span:first-child{color:var(--text-primary);font-weight:500;}
  .skill-item-top span:last-child{color:var(--text-muted);font-family:'JetBrains Mono',monospace;font-size:10.5px;}
  .seg-bar{display:flex;gap:3px;}
  .seg{height:5px;flex:1;border-radius:3px;background:rgba(255,255,255,0.07);}
  .seg.filled{background:linear-gradient(90deg,var(--green),var(--cyan));}

  @media (max-width:900px){.skills-grid{grid-template-columns:1fr 1fr;}}
  @media (max-width:600px){.skills-grid{grid-template-columns:1fr;}.about-grid{grid-template-columns:1fr;}}

  /* ============ PROJECTS ============ */
  .projects-grid{display:grid;grid-template-columns:1fr 1fr;gap:22px;}
  .project-card{padding:0;overflow:hidden;transition:transform .25s, border-color .25s;position:relative;}
  .project-card:hover{transform:translateY(-4px);border-color:rgba(34,217,242,0.3);}
  .project-top{padding:24px 24px 0;}
  .project-status{
    display:inline-flex;align-items:center;gap:6px;
    font-family:'JetBrains Mono',monospace;font-size:10.5px;
    color:var(--amber);background:rgba(255,180,84,0.1);
    padding:4px 10px;border-radius:20px;margin-bottom:16px;
  }
  .project-status .sd{width:5px;height:5px;border-radius:50%;background:var(--amber);}
  .project-card h3{font-size:18px;margin-bottom:10px;}
  .project-card .obj{color:var(--text-secondary);font-size:14px;margin-bottom:16px;}
  .project-tools{font-family:'JetBrains Mono',monospace;font-size:11.5px;color:var(--text-muted);margin-bottom:18px;}
  .project-mitre{display:flex;flex-wrap:wrap;gap:7px;padding:18px 24px 24px;border-top:1px solid var(--line);margin-top:4px;}
  .mitre-tag{font-family:'JetBrains Mono',monospace;font-size:10.5px;padding:4px 9px;border-radius:5px;background:rgba(0,245,160,0.08);color:var(--green);border:1px solid rgba(0,245,160,0.18);}

  @media (max-width:900px){.projects-grid{grid-template-columns:1fr;}}

  /* ============ CERTIFICATIONS TIMELINE ============ */
  .cert-groups{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;margin-bottom:24px;}
  .cert-group{padding:24px;}
  .cert-group-head{display:flex;align-items:center;gap:10px;margin-bottom:18px;}
  .cert-group-head .dot{width:9px;height:9px;border-radius:50%;}
  .cert-group-head h3{font-size:14px;}
  .cert-item{font-size:13.5px;color:var(--text-secondary);padding:9px 0;border-bottom:1px solid var(--line);}
  .cert-item:last-child{border-bottom:none;}
  .planned-row{
    display:flex;justify-content:space-between;align-items:center;
    padding:14px 22px;border-bottom:1px solid var(--line);font-size:14px;
  }
  .planned-row:last-child{border-bottom:none;}
  .planned-row .prov{color:var(--text-muted);font-family:'JetBrains Mono',monospace;font-size:11.5px;}
  @media (max-width:900px){.cert-groups{grid-template-columns:1fr;}}

  /* ============ LEARNING FOCUS ============ */
  .learning-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px;}
  .learn-card{padding:22px;}
  .learn-card h4{font-size:14.5px;margin-bottom:9px;color:var(--cyan);}
  .learn-card p{font-size:13.5px;color:var(--text-secondary);margin-bottom:10px;}
  .learn-card .res{font-family:'JetBrains Mono',monospace;font-size:11px;color:var(--text-muted);}
  @media (max-width:900px){.learning-grid{grid-template-columns:1fr 1fr;}}
  @media (max-width:600px){.learning-grid{grid-template-columns:1fr;}}

  /* ============ GITHUB STATS ============ */
  .gh-stats{display:flex;flex-direction:column;gap:18px;align-items:center;}
  .gh-stats img{max-width:100%;border-radius:var(--radius);border:1px solid var(--glass-border);}
  .gh-row{display:flex;gap:18px;width:100%;flex-wrap:wrap;justify-content:center;}
  .gh-row img{flex:1;min-width:280px;}

  /* ============ CONTACT / FOOTER ============ */
  .contact-card{padding:56px;text-align:center;}
  .contact-card h2{font-size:clamp(26px,3.6vw,36px);margin-bottom:16px;}
  .contact-card p{color:var(--text-secondary);max-width:520px;margin:0 auto 34px;}
  .contact-actions{display:flex;gap:14px;justify-content:center;flex-wrap:wrap;}

  footer{padding:36px 0 50px;text-align:center;}
  footer p{color:var(--text-muted);font-size:13px;font-family:'JetBrains Mono',monospace;}

  ::selection{background:rgba(0,245,160,0.25);color:var(--text-primary);}
</style>
</head>
<body>

<nav>
  <div class="nav-inner">
    <div class="brand">
      <div class="brand-mark">S7</div>
      <span>Subathran J</span>
      <span class="status-dot" aria-hidden="true"></span>
    </div>
    <button class="nav-toggle" id="navToggle" aria-label="Toggle menu">☰</button>
    <div class="nav-links" id="navLinks">
      <a href="#about">About</a>
      <a href="#skills">Skills</a>
      <a href="#projects">Projects</a>
      <a href="#certifications">Certifications</a>
      <a href="#github">GitHub</a>
      <a href="https://drive.google.com/file/d/1sNqIXZ3o07MNx1AlF5ufAMvCul-_cxaj/view?usp=sharing" class="nav-cta" target="_blank" rel="noopener">Resume</a>
    </div>
  </div>
</nav>

<header class="hero">
  <div class="wrap hero-grid">
    <div>
      <span class="eyebrow"><span class="status-dot"></span> Open to SOC Analyst L1 / Internship roles</span>
      <h1>Watching the logs<br>so threats don't <span class="accent">go unnoticed.</span></h1>
      <p class="hero-sub">I'm Subathran, a cybersecurity student building real SOC skills through home labs — Splunk, Wazuh, Windows Event Logs, and MITRE ATT&CK mapping, one investigation at a time.</p>
      <div class="hero-actions">
        <a href="#projects" class="btn btn-primary">View lab projects</a>
        <a href="mailto:subathranjayaraman05@gmail.com" class="btn btn-ghost">Get in touch</a>
      </div>
      <div class="hero-stats">
        <div><div class="hstat-num">6</div><div class="hstat-label">Home lab projects</div></div>
        <div><div class="hstat-num">10</div><div class="hstat-label">Certifications earned</div></div>
        <div><div class="hstat-num">3</div><div class="hstat-label">SIEM platforms studied</div></div>
      </div>
    </div>

    <div class="glass console">
      <div class="console-bar">
        <div class="console-dots"><span></span><span></span><span></span></div>
        <div class="console-title">alert_feed.log</div>
        <div class="console-live"><span class="status-dot"></span>LIVE</div>
      </div>
      <div class="console-body" id="consoleBody"></div>
      <div class="console-footer">
        <span>SOURCE: home-lab-siem</span>
        <span id="clock">00:00:00</span>
      </div>
    </div>
  </div>
</header>

<section id="about">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="section-eyebrow">// 01 — about</span>
      <h2>Building SOC skills the hands-on way</h2>
      <p>Every certification and lab here reflects time spent actually doing the work, not just reading about it.</p>
    </div>
    <div class="about-grid">
      <div class="about-text reveal">
        <p>I'm a cybersecurity student with a focused interest in Security Operations and Blue Team practices. Over the past year I've built practical skills through home labs, structured courses, and self-directed learning — studying how SOC analysts detect threats, investigate alerts, and respond to incidents in real environments.</p>
        <p>My learning is hands-on. I build labs using Splunk, Wazuh, and Windows Server to practice what I study: writing detection rules, analysing Windows Event Logs, and tracing attack paths using the MITRE ATT&CK framework.</p>
        <ul class="about-list">
          <li><span class="check">✓</span>Foundational understanding of the SOC alert triage workflow (L1 → escalation)</li>
          <li><span class="check">✓</span>Hands-on experience analysing Windows Event Logs and Sysmon data</li>
          <li><span class="check">✓</span>Familiarity with SIEM platforms through self-built home labs</li>
          <li><span class="check">✓</span>Knowledge of MITRE ATT&CK tactics and techniques applied to lab scenarios</li>
        </ul>
      </div>
      <div class="glass about-card reveal">
        <h3>Quick facts</h3>
        <div class="cert-row"><span>Location</span><span class="cert-badge">India · Remote/Hybrid</span></div>
        <div class="cert-row"><span>Role target</span><span class="cert-badge">SOC Analyst L1</span></div>
        <div class="cert-row"><span>Focus</span><span class="cert-badge">Threat Detection</span></div>
        <div class="cert-row"><span>Focus</span><span class="cert-badge">Incident Response</span></div>
        <div class="cert-row"><span>Status</span><span class="cert-badge">Actively applying</span></div>
      </div>
    </div>
  </div>
</section>

<section id="skills">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="section-eyebrow">// 02 — technical skills</span>
      <h2>Skill proficiency</h2>
      <p>Self-assessed honestly against lab work and coursework — not professional experience.</p>
    </div>
    <div class="skills-grid" id="skillsGrid"></div>
  </div>
</section>

<section id="projects">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="section-eyebrow">// 03 — home lab projects</span>
      <h2>Cybersecurity home labs</h2>
      <p>Self-built environments simulating real SOC workflows. Repos are being documented and pushed — status shown per project.</p>
    </div>
    <div class="projects-grid" id="projectsGrid"></div>
  </div>
</section>

<section id="certifications">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="section-eyebrow">// 04 — certifications</span>
      <h2>Certifications</h2>
      <p>Earned through Cisco Networking Academy, GUVI, and Udemy — with more in progress.</p>
    </div>
    <div class="cert-groups" id="certGroups"></div>
    <div class="glass reveal" id="plannedCerts"></div>
  </div>
</section>

<section id="learning">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="section-eyebrow">// 05 — currently studying</span>
      <h2>Current learning focus</h2>
      <p>What's actively on the bench right now.</p>
    </div>
    <div class="learning-grid" id="learningGrid"></div>
  </div>
</section>

<section id="github">
  <div class="wrap">
    <div class="section-head reveal">
      <span class="section-eyebrow">// 06 — activity</span>
      <h2>GitHub activity</h2>
      <p>Contribution history and language breakdown, pulled live from GitHub.</p>
    </div>
    <div class="gh-stats reveal">
      <div class="gh-row">
        <img src="https://github-readme-stats.vercel.app/api?username=subathran07&show_icons=true&theme=algolia&include_all_commits=true&count_private=true&hide_border=true&bg_color=0D2340&title_color=00F5A0&icon_color=22D9F2&text_color=8FA3C4&border_radius=14" alt="GitHub stats for subathran07" loading="lazy">
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=subathran07&layout=compact&langs_count=6&theme=algolia&hide_border=true&bg_color=0D2340&title_color=00F5A0&text_color=8FA3C4&border_radius=14" alt="Top languages for subathran07" loading="lazy">
      </div>
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=subathran07&theme=algolia&hide_border=true&background=0D2340&stroke=00F5A0&ring=22D9F2&fire=00F5A0&currStreakNum=E6F1FF&sideNums=8FA3C4&currStreakLabel=22D9F2&sideLabels=8FA3C4&dates=5C6E8C&border_radius=14" alt="GitHub streak stats" loading="lazy">
      <img src="https://github-readme-activity-graph.vercel.app/graph?username=subathran07&bg_color=0D2340&color=00F5A0&line=22D9F2&point=E6F1FF&area=true&area_color=0D4F6B&hide_border=true&border_radius=14&title_color=00F5A0" alt="GitHub contribution graph" loading="lazy">
    </div>
  </div>
</section>

<section id="contact">
  <div class="wrap">
    <div class="glass contact-card reveal">
      <h2>Let's connect</h2>
      <p>Actively looking for SOC Analyst internships, entry-level Security Analyst roles, and Blue Team opportunities. If you're hiring, I'd love to talk.</p>
      <div class="contact-actions">
        <a href="https://linkedin.com/in/subathran07" target="_blank" rel="noopener" class="btn btn-primary">LinkedIn</a>
        <a href="mailto:subathranjayaraman05@gmail.com" class="btn btn-ghost">Email</a>
        <a href="https://drive.google.com/file/d/1sNqIXZ3o07MNx1AlF5ufAMvCul-_cxaj/view?usp=sharing" target="_blank" rel="noopener" class="btn btn-ghost">Resume</a>
        <a href="https://github.com/subathran07" target="_blank" rel="noopener" class="btn btn-ghost">GitHub</a>
      </div>
    </div>
  </div>
</section>

<footer>
  <p>// building skills one lab at a time — subathran07</p>
</footer>

<script>
// ---------- data ----------
const skillGroups = [
  {name:"SOC operations", color:"var(--green)", items:[
    ["Alert triage",2],["Log analysis",3],["Incident response",2],["Security monitoring",2],["Threat detection",2]
  ]},
  {name:"SIEM & platforms", color:"var(--cyan)", items:[
    ["Splunk",1],["Wazuh",1],["Microsoft Sentinel",1]
  ]},
  {name:"Networking", color:"var(--green)", items:[
    ["TCP/IP",2],["DNS / HTTP / HTTPS",2],["Traffic analysis",2],["Network defense",2]
  ]},
  {name:"Security tools", color:"var(--cyan)", items:[
    ["Wireshark",3],["Nmap",2],["Burp Suite",1]
  ]},
  {name:"Operating systems", color:"var(--green)", items:[
    ["Windows 10 / Server",3],["Linux",2],["Kali Linux",2]
  ]},
  {name:"Threat intel & frameworks", color:"var(--cyan)", items:[
    ["MITRE ATT&CK",2],["Cyber Kill Chain",2],["IOC analysis",1],["Threat hunting",1]
  ]}
];
const levelLabel = {1:"Learning",2:"Familiar",3:"Hands-on"};

const skillsGrid = document.getElementById('skillsGrid');
skillGroups.forEach(g=>{
  const card = document.createElement('div');
  card.className = 'glass skill-card reveal';
  let itemsHtml = g.items.map(([name,lvl])=>`
    <div class="skill-item">
      <div class="skill-item-top"><span>${name}</span><span>${levelLabel[lvl]}</span></div>
      <div class="seg-bar">
        ${[1,2,3].map(i=>`<div class="seg ${i<=lvl?'filled':''}"></div>`).join('')}
      </div>
    </div>`).join('');
  card.innerHTML = `<h3><span class="dot" style="background:${g.color}"></span>${g.name}</h3>${itemsHtml}`;
  skillsGrid.appendChild(card);
});

const projects = [
  {title:"SOC alert investigation lab", obj:"Simulate an L1 analyst workflow — triage, investigate, and document alerts using a structured IR template.", tools:"Splunk Free · Windows Event Logs · Sysmon · VirusTotal", mitre:["T1110 Brute force","T1078 Valid accounts"]},
  {title:"Wazuh home lab", obj:"Deploy an open-source SIEM/XDR to understand agent-based monitoring, rule tuning, and alerting.", tools:"Wazuh Manager · Wazuh Agent · Ubuntu Server · OpenSearch", mitre:["FIM alerting","Rule tuning"]},
  {title:"Active Directory security lab", obj:"Build an AD environment to study authentication events and common AD attack patterns.", tools:"Windows Server 2019 · Sysmon · Splunk", mitre:["T1136 Create account","T1098 Account manipulation","T1110.001 Password guessing"]},
  {title:"Splunk detection lab", obj:"Ingest and visualise security data — the core daily skills of an L1 SOC analyst.", tools:"Splunk Free · BOTS dataset · Sysmon", mitre:["SPL detection logic","Dashboarding"]},
  {title:"Network traffic analysis lab", obj:"Examine real and simulated packet captures to identify anomalous traffic patterns.", tools:"Wireshark · Nmap · tcpdump · Malware-Traffic PCAPs", mitre:["T1071 App layer protocol","T1046 Network service discovery"]},
  {title:"Threat hunting lab", obj:"Practise hypothesis-driven hunting and map findings to MITRE ATT&CK.", tools:"Splunk · Sysmon · ATT&CK Navigator", mitre:["T1059.001 PowerShell","T1027 Obfuscated files","T1543 System process"]},
];

const projectsGrid = document.getElementById('projectsGrid');
projects.forEach(p=>{
  const card = document.createElement('div');
  card.className = 'glass project-card reveal';
  card.innerHTML = `
    <div class="project-top">
      <span class="project-status"><span class="sd"></span>Planned — repo in progress</span>
      <h3>${p.title}</h3>
      <p class="obj">${p.obj}</p>
      <p class="project-tools">${p.tools}</p>
    </div>
    <div class="project-mitre">${p.mitre.map(m=>`<span class="mitre-tag">${m}</span>`).join('')}</div>
  `;
  projectsGrid.appendChild(card);
});

const certGroups = [
  {name:"Cisco Networking Academy", color:"var(--green)", items:["Introduction to Cybersecurity","Endpoint Security","Cyber Threat Management","Network Defense","Ethical Hacker"]},
  {name:"GUVI", color:"var(--cyan)", items:["Advanced Cyber Security & Ethical Hacking","Cyber Security & Ethical Hacking for Beginners","Ethical Hacking","Dark Web"]},
  {name:"Udemy", color:"var(--green)", items:["ISO/IEC 27001:2022 — Info Security Controls"]},
];
const certGroupsEl = document.getElementById('certGroups');
certGroups.forEach(g=>{
  const card = document.createElement('div');
  card.className = 'glass cert-group reveal';
  card.innerHTML = `<div class="cert-group-head"><span class="dot" style="background:${g.color}"></span><h3>${g.name}</h3></div>` +
    g.items.map(i=>`<div class="cert-item">${i}</div>`).join('');
  certGroupsEl.appendChild(card);
});

const planned = [
  ["Google Cybersecurity Certificate","Coursera / Google","Q3 2025"],
  ["CompTIA Security+","CompTIA","2025–2026"],
  ["Splunk Core Certified User","Splunk","2025–2026"],
  ["Blue Team Labs Online — SOC L1","BTL Online","2025–2026"],
];
document.getElementById('plannedCerts').innerHTML =
  `<div style="padding:20px 22px 4px;font-family:'JetBrains Mono',monospace;font-size:11.5px;color:var(--text-muted);text-transform:uppercase;letter-spacing:0.06em;">Next up</div>` +
  planned.map(([name,prov,time])=>`
    <div class="planned-row">
      <span>${name}</span>
      <span class="prov">${prov} · ${time}</span>
    </div>`).join('');

const learning = [
  ["Splunk","SPL queries, index management, detection rules, BOTS challenges","Splunk Free · BOTS dataset"],
  ["Wazuh","Agent management, rule customisation, FIM, alert review","Self-hosted home lab"],
  ["Microsoft Sentinel","KQL basics, data connectors, analytic rules","Microsoft Learn"],
  ["Threat hunting","Hypothesis creation, Sysmon analysis, hunt playbooks","ThreatHunter Playbook · Sigma"],
  ["Incident response","NIST SP 800-61 lifecycle, containment, IR reporting","NIST documentation"],
  ["Active Directory","Auth event IDs, Kerberoasting detection, AD hardening","Home lab · IppSec · TCM"],
];
document.getElementById('learningGrid').innerHTML = learning.map(([t,d,r])=>`
  <div class="glass learn-card reveal">
    <h4>${t}</h4>
    <p>${d}</p>
    <div class="res">${r}</div>
  </div>`).join('');

// ---------- console log feed ----------
const feed = [
  {t:"09:41:02", tag:"benign", txt:"Login success — user jdoe, source 10.0.4.2"},
  {t:"09:41:15", tag:"investigating", txt:"5x failed logins — Event ID 4625, host WIN10-04"},
  {t:"09:41:19", tag:"investigating", txt:"Correlating 4625→4624 for brute-force pattern"},
  {t:"09:41:33", tag:"escalated", txt:"Encoded PowerShell in process args — Sysmon EID 1"},
  {t:"09:41:40", tag:"benign", txt:"FIM: config file modified — signed installer, closed"},
  {t:"09:41:52", tag:"investigating", txt:"Unusual outbound connection — port 4444, host WIN10-04"},
  {t:"09:42:08", tag:"escalated", txt:"IOC match — hash flagged on VirusTotal, ticket opened"},
  {t:"09:42:20", tag:"benign", txt:"Scheduled scan completed — 0 findings"},
];
const tagLabel = {benign:"RESOLVED", investigating:"INVESTIGATING", escalated:"ESCALATED"};
const consoleBody = document.getElementById('consoleBody');
let feedIndex = 0;

function pushLog(){
  const item = feed[feedIndex % feed.length];
  feedIndex++;
  const line = document.createElement('div');
  line.className = 'log-line';
  line.innerHTML = `
    <span class="log-time">${item.t}</span>
    <span class="log-tag tag-${item.tag}">${tagLabel[item.tag]}</span>
    <span class="log-msg">${item.txt}</span>`;
  consoleBody.appendChild(line);
  if(consoleBody.children.length > 7){
    consoleBody.removeChild(consoleBody.firstElementChild);
  }
  consoleBody.scrollTop = consoleBody.scrollHeight;
}

const reducedMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;
if(!reducedMotion){
  pushLog();
  setInterval(pushLog, 2200);
} else {
  feed.slice(0,5).forEach(()=>pushLog());
}

// ---------- clock ----------
function tickClock(){
  const now = new Date();
  document.getElementById('clock').textContent = now.toTimeString().slice(0,8);
}
tickClock();
setInterval(tickClock, 1000);

// ---------- nav toggle ----------
const navToggle = document.getElementById('navToggle');
const navLinks = document.getElementById('navLinks');
navToggle.addEventListener('click', ()=> navLinks.classList.toggle('open'));
navLinks.querySelectorAll('a').forEach(a => a.addEventListener('click', ()=> navLinks.classList.remove('open')));

// ---------- scroll reveal ----------
const revealEls = document.querySelectorAll('.reveal');
const io = new IntersectionObserver((entries)=>{
  entries.forEach(e=>{
    if(e.isIntersecting){
      e.target.classList.add('in');
      io.unobserve(e.target);
    }
  });
},{threshold:0.12});
revealEls.forEach(el=>io.observe(el));

// re-observe dynamically injected reveal cards
setTimeout(()=>{
  document.querySelectorAll('.reveal:not(.in)').forEach(el=>io.observe(el));
}, 50);
</script>
</body>
</html>
