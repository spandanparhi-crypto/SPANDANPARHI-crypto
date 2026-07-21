<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Spandan Parhi — GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;500;700&family=Orbitron:wght@400;700;900&family=Space+Grotesk:wght@300;400;500;700&display=swap" rel="stylesheet"/>
<style>
*{margin:0;padding:0;box-sizing:border-box;}
:root{--g:#39FF14;--c:#00FFFF;--m:#B44FE8;--o:#FF6B35;--dk:#080c10;--dk2:#0d1117;--dk3:#161b22;--card:#0e1318;--card2:#111827;}
body{background:var(--dk2);color:#cdd9e5;font-family:'Space Grotesk',sans-serif;overflow-x:hidden;}
.wrap{max-width:680px;margin:0 auto;padding:20px 16px;}

/* ── HERO ── */
.hero{position:relative;border-radius:20px;padding:36px 28px 28px;margin-bottom:16px;overflow:hidden;background:var(--dk);text-align:center;}
.hero-border{position:absolute;inset:0;border-radius:20px;padding:1.5px;background:conic-gradient(from 0deg,var(--g),var(--c),var(--m),var(--o),var(--g));-webkit-mask:linear-gradient(#fff 0 0) content-box,linear-gradient(#fff 0 0);-webkit-mask-composite:destination-out;mask-composite:exclude;animation:borderSpin 4s linear infinite;}
@keyframes borderSpin{to{transform:rotate(360deg);}}
.hero-glow{position:absolute;top:-40px;left:50%;transform:translateX(-50%);width:320px;height:160px;background:radial-gradient(ellipse,rgba(57,255,20,0.12) 0%,transparent 70%);pointer-events:none;}
.scanline{position:absolute;top:0;left:0;right:0;height:1.5px;background:linear-gradient(90deg,transparent 0%,var(--g) 50%,transparent 100%);animation:scan 2.5s linear infinite;opacity:0.7;}
@keyframes scan{0%{top:-2px;opacity:0.7;}80%{opacity:0.7;}100%{top:102%;opacity:0;}}

/* ── AVATAR ── */
.av-wrap{width:100px;height:100px;margin:0 auto 18px;position:relative;}
.av-ring{position:absolute;inset:-5px;border-radius:50%;background:conic-gradient(var(--g),var(--c),var(--m),var(--o),var(--g));animation:ringrot 3s linear infinite;}
.av-ring-mask{position:absolute;inset:3px;border-radius:50%;background:var(--dk);}
.av-pulse{position:absolute;inset:-14px;border-radius:50%;border:1.5px solid rgba(57,255,20,0.3);animation:pulse 2s ease-out infinite;}
@keyframes pulse{0%{transform:scale(0.94);opacity:0.8;}100%{transform:scale(1.18);opacity:0;}}
@keyframes ringrot{to{transform:rotate(360deg);}}
.av-inner{position:absolute;inset:5px;border-radius:50%;background:linear-gradient(135deg,#0f2010,#0d1117);display:flex;align-items:center;justify-content:center;font-size:40px;z-index:2;}

/* ── HERO TEXT ── */
.hero-name{font-family:'Orbitron',monospace;font-size:22px;font-weight:900;letter-spacing:3px;margin-bottom:5px;color:#e8f4e8;}
.hero-name .hi{color:var(--g);text-shadow:0 0 24px rgba(57,255,20,0.55);}
.hero-sub{font-family:'Fira Code',monospace;font-size:11px;color:var(--c);letter-spacing:2px;margin-bottom:14px;opacity:0.8;}
.typing-row{font-family:'Fira Code',monospace;font-size:13px;color:#e8f4e8;margin-bottom:18px;min-height:22px;}
.typing-row .bracket{color:var(--g);opacity:0.6;}
.cur{display:inline-block;width:2px;height:14px;background:var(--c);margin-left:1px;vertical-align:middle;animation:blink 0.75s step-end infinite;}
@keyframes blink{0%,100%{opacity:1;}50%{opacity:0;}}

/* ── BADGES ── */
.badge-row{display:flex;flex-wrap:wrap;gap:6px;justify-content:center;margin-bottom:16px;}
.badge{padding:4px 11px;border-radius:20px;font-size:10px;font-weight:600;letter-spacing:0.8px;font-family:'Fira Code',monospace;}
.bg{color:var(--g);border:1px solid rgba(57,255,20,0.4);background:rgba(57,255,20,0.07);}
.bc{color:var(--c);border:1px solid rgba(0,255,255,0.35);background:rgba(0,255,255,0.06);}
.bm{color:var(--m);border:1px solid rgba(180,79,232,0.4);background:rgba(180,79,232,0.07);}
.bo{color:var(--o);border:1px solid rgba(255,107,53,0.4);background:rgba(255,107,53,0.07);}

/* ── META ROW ── */
.meta-row{display:flex;justify-content:center;align-items:center;gap:18px;flex-wrap:wrap;font-family:'Fira Code',monospace;font-size:11px;color:#8b949e;}
.meta-row span{display:flex;align-items:center;gap:6px;}
.dot-sm{width:5px;height:5px;border-radius:50%;}

/* ── SECTIONS ── */
.sec{background:var(--card);border:1px solid #1e2730;border-radius:14px;padding:18px 20px;margin-bottom:14px;position:relative;overflow:hidden;transition:border-color 0.25s,transform 0.2s;}
.sec:hover{border-color:rgba(57,255,20,0.3);transform:translateY(-2px);}
.sec-top-line{position:absolute;top:0;left:0;right:0;height:1px;background:linear-gradient(90deg,transparent,var(--g),transparent);opacity:0;transition:opacity 0.3s;}
.sec:hover .sec-top-line{opacity:0.6;}

/* ── SECTION HEADINGS ── */
.sh{font-family:'Orbitron',monospace;font-size:11px;font-weight:700;letter-spacing:1.5px;margin-bottom:16px;display:flex;align-items:center;gap:8px;}
.sh-g{color:var(--g);}
.sh-c{color:var(--c);}
.sh-m{color:var(--m);}
.sh-o{color:var(--o);}
.sh-arr{font-size:8px;opacity:0.45;}

/* ── CODE BLOCK ── */
.code-block{background:#060a0e;border:1px solid #1e2730;border-radius:10px;padding:18px;font-family:'Fira Code',monospace;font-size:12px;line-height:1.95;position:relative;}
.code-block::after{content:'python';position:absolute;top:8px;right:14px;font-family:'Orbitron',monospace;font-size:9px;color:#3d4f5e;letter-spacing:1px;}
.kw{color:#ff79c6;}
.fn{color:#50fa7b;}
.st{color:#8be9fd;}
.cm{color:#44475a;font-style:italic;}
.nv{color:var(--g);}
.nb{color:#ffb86c;}

/* ── LEARNING GRID ── */
.learn-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px;}
.learn-item{display:flex;align-items:center;gap:10px;padding:10px 14px;background:#060a0e;border-radius:10px;border:1px solid #1e2730;font-family:'Fira Code',monospace;font-size:11px;color:#8b949e;transition:all 0.25s;}
.learn-item:hover{border-color:var(--m);color:var(--m);background:rgba(180,79,232,0.05);}
.ld{width:6px;height:6px;border-radius:50%;flex-shrink:0;}

/* ── SKILL GRID ── */
.skill-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:8px;}
.skill-chip{background:#060a0e;border:1px solid #1e2730;border-radius:10px;padding:12px 8px;text-align:center;font-family:'Fira Code',monospace;font-size:10px;color:#8b949e;transition:all 0.25s;cursor:default;}
.skill-chip:hover{transform:translateY(-3px);}
.skill-chip .em{font-size:24px;display:block;margin-bottom:6px;}
.skill-chip.sg:hover{border-color:var(--g);color:var(--g);background:rgba(57,255,20,0.04);}
.skill-chip.sc:hover{border-color:var(--c);color:var(--c);background:rgba(0,255,255,0.04);}
.skill-chip.sm:hover{border-color:var(--m);color:var(--m);background:rgba(180,79,232,0.04);}
.skill-chip.so:hover{border-color:var(--o);color:var(--o);background:rgba(255,107,53,0.04);}

/* ── SKILL BARS ── */
.bar-wrap{margin-bottom:12px;}
.bar-head{display:flex;justify-content:space-between;font-family:'Fira Code',monospace;font-size:11px;margin-bottom:6px;}
.bar-name{color:#cdd9e5;}
.bar-pct{color:var(--g);}
.bar-track{height:4px;background:#1e2730;border-radius:4px;overflow:hidden;}
.bar-fill{height:100%;border-radius:4px;width:0;transition:width 1.4s cubic-bezier(0.4,0,0.2,1);}
.bf-g{background:linear-gradient(90deg,var(--g),var(--c));}
.bf-c{background:linear-gradient(90deg,var(--c),var(--m));}
.bf-m{background:linear-gradient(90deg,var(--m),var(--o));}

/* ── STAT CARDS ── */
.stat-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:8px;}
.stat-card{background:#060a0e;border:1px solid #1e2730;border-radius:10px;padding:14px 8px;text-align:center;transition:all 0.25s;}
.stat-card:hover{border-color:var(--c);transform:scale(1.05);}
.snum{font-family:'Orbitron',monospace;font-size:18px;font-weight:700;color:var(--g);display:block;margin-bottom:4px;}
.slbl{font-family:'Fira Code',monospace;font-size:9px;color:#44546a;letter-spacing:0.5px;}

/* ── GOAL BOX ── */
.goal-box{background:linear-gradient(135deg,rgba(57,255,20,0.04),rgba(0,255,255,0.04));border:1px solid rgba(57,255,20,0.2);border-radius:12px;padding:20px;text-align:center;}
.goal-txt{font-family:'Orbitron',monospace;font-size:13px;color:var(--g);letter-spacing:1px;line-height:1.7;}
.goal-sub{font-family:'Fira Code',monospace;font-size:11px;color:#44546a;margin-top:10px;letter-spacing:0.5px;}

/* ── CONNECT ── */
.connect-row{display:flex;gap:8px;margin-bottom:10px;}
.cbtn{flex:1;padding:12px 8px;border-radius:10px;text-align:center;border:1px solid;font-family:'Fira Code',monospace;font-size:11px;cursor:pointer;transition:all 0.25s;text-decoration:none;display:flex;align-items:center;justify-content:center;gap:7px;font-weight:500;}
.cb1{color:#0a84ff;border-color:rgba(10,132,255,0.35);background:rgba(10,132,255,0.05);}
.cb1:hover{background:rgba(10,132,255,0.14);border-color:#0a84ff;}
.cb2{color:#e6edf3;border-color:rgba(230,237,243,0.2);background:rgba(255,255,255,0.03);}
.cb2:hover{border-color:var(--g);color:var(--g);background:rgba(57,255,20,0.05);}
.cb3{color:#ff4545;border-color:rgba(255,69,69,0.35);background:rgba(255,69,69,0.05);}
.cb3:hover{background:rgba(255,69,69,0.14);border-color:#ff4545;}
.portfolio-btn{display:block;width:100%;padding:14px;border-radius:12px;text-align:center;border:1px solid rgba(57,255,20,0.3);background:rgba(57,255,20,0.04);font-family:'Orbitron',monospace;font-size:11px;color:var(--g);letter-spacing:2px;cursor:pointer;transition:all 0.3s;text-decoration:none;}
.portfolio-btn:hover{background:rgba(57,255,20,0.1);border-color:var(--g);letter-spacing:3px;}

/* ── FOOTER ── */
.footer{text-align:center;padding:18px 0 6px;font-family:'Fira Code',monospace;font-size:11px;color:#3d4f5e;border-top:1px solid #1e2730;margin-top:4px;}
.footer strong{color:var(--g);}
.footer-dots{display:flex;justify-content:center;gap:7px;margin-top:10px;}
.fd{width:4px;height:4px;border-radius:50%;animation:fdot 1.5s ease-in-out infinite;}
.fd:nth-child(1){background:var(--g);}
.fd:nth-child(2){background:var(--c);animation-delay:0.3s;}
.fd:nth-child(3){background:var(--m);animation-delay:0.6s;}
@keyframes fdot{0%,100%{transform:scale(1);opacity:0.4;}50%{transform:scale(1.6);opacity:1;}}
</style>
</head>
<body>
<div class="wrap">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-border"></div>
    <div class="hero-glow"></div>
    <div class="scanline"></div>

    <div class="av-wrap">
      <div class="av-ring"></div>
      <div class="av-ring-mask"></div>
      <div class="av-pulse"></div>
      <div class="av-inner">🤖</div>
    </div>

    <div class="hero-name">SPANDAN <span class="hi">PARHI</span></div>
    <div class="hero-sub">// ECE STUDENT · AI ENGINEER · PYTHON DEVELOPER</div>
    <div class="typing-row">
      <span class="bracket">&gt;&gt;&gt; </span><span id="typ"></span><span class="cur"></span>
    </div>

    <div class="badge-row">
      <span class="badge bg">Data Science</span>
      <span class="badge bc">Generative AI</span>
      <span class="badge bm">LLMs</span>
      <span class="badge bo">Machine Learning</span>
      <span class="badge bg">Agentic AI</span>
      <span class="badge bc">Power BI</span>
      <span class="badge bm">LangChain</span>
      <span class="badge bo">LangGraph</span>
    </div>

    <div class="meta-row">
      <span><div class="dot-sm" style="background:var(--g)"></div>📍 Odisha, India</span>
      <span style="color:#1e2730">|</span>
      <span><div class="dot-sm" style="background:var(--c)"></div>📧 spandanparhi019@gmail.com</span>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="sec">
    <div class="sec-top-line"></div>
    <div class="sh sh-g"><span class="sh-arr">▶</span> About Me</div>
    <div class="code-block">
<span class="cm"># Electronics &amp; Telecom → AI Engineer pipeline</span><br>
<span class="kw">class</span> <span class="fn">SpandanParhi</span>:<br>
&nbsp;&nbsp;<span class="kw">def</span> <span class="fn">__init__</span>(<span class="nv">self</span>):<br>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="nv">self</span>.degree &nbsp;= <span class="st">"Electronics &amp; Telecom Engg."</span><br>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="nv">self</span>.role &nbsp;&nbsp;&nbsp;= <span class="st">"Aspiring Data Scientist &amp; AI Engineer"</span><br>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="nv">self</span>.stack &nbsp;&nbsp;= [<span class="st">"Python"</span>, <span class="st">"SQL"</span>, <span class="st">"PowerBI"</span>]<br>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="nv">self</span>.passion = <span class="st">"Generative AI + Agentic Systems"</span><br>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="nv">self</span>.location = <span class="st">"Odisha, India 🇮🇳"</span><br><br>
&nbsp;&nbsp;<span class="kw">def</span> <span class="fn">goal</span>(<span class="nv">self</span>):<br>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="kw">return</span> <span class="nb">f</span><span class="st">"Transforming Data Into Intelligence 🚀"</span>
    </div>
  </div>

  <!-- CURRENTLY LEARNING -->
  <div class="sec">
    <div class="sec-top-line"></div>
    <div class="sh sh-m"><span class="sh-arr">▶</span> Currently Learning</div>
    <div class="learn-grid">
      <div class="learn-item"><div class="ld" style="background:var(--g);box-shadow:0 0 6px var(--g)"></div>Machine Learning</div>
      <div class="learn-item"><div class="ld" style="background:var(--c);box-shadow:0 0 6px var(--c)"></div>Deep Learning</div>
      <div class="learn-item"><div class="ld" style="background:var(--m);box-shadow:0 0 6px var(--m)"></div>LangChain</div>
      <div class="learn-item"><div class="ld" style="background:var(--o);box-shadow:0 0 6px var(--o)"></div>LangGraph</div>
      <div class="learn-item"><div class="ld" style="background:var(--g);box-shadow:0 0 6px var(--g)"></div>CrewAI</div>
      <div class="learn-item"><div class="ld" style="background:var(--c);box-shadow:0 0 6px var(--c)"></div>Agentic AI</div>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="sec">
    <div class="sec-top-line"></div>
    <div class="sh sh-c"><span class="sh-arr">▶</span> Tech Stack</div>
    <div class="skill-grid">
      <div class="skill-chip sg"><span class="em">🐍</span>Python</div>
      <div class="skill-chip sc"><span class="em">🗄️</span>MySQL</div>
      <div class="skill-chip sm"><span class="em">📊</span>Power BI</div>
      <div class="skill-chip so"><span class="em">🤖</span>LangChain</div>
      <div class="skill-chip sg"><span class="em">🧠</span>LangGraph</div>
      <div class="skill-chip sc"><span class="em">👥</span>CrewAI</div>
      <div class="skill-chip sm"><span class="em">🔢</span>NumPy</div>
      <div class="skill-chip so"><span class="em">🐼</span>Pandas</div>
      <div class="skill-chip sg"><span class="em">🐙</span>GitHub</div>
      <div class="skill-chip sc"><span class="em">🌐</span>HTML</div>
      <div class="skill-chip sm"><span class="em">🎨</span>CSS</div>
      <div class="skill-chip so"><span class="em">⚡</span>JavaScript</div>
    </div>
  </div>

  <!-- SKILL PROFICIENCY -->
  <div class="sec">
    <div class="sec-top-line"></div>
    <div class="sh sh-o"><span class="sh-arr">▶</span> Skill Proficiency</div>
    <div id="bars">
      <div class="bar-wrap">
        <div class="bar-head"><span class="bar-name">Python</span><span class="bar-pct">92%</span></div>
        <div class="bar-track"><div class="bar-fill bf-g" data-w="92"></div></div>
      </div>
      <div class="bar-wrap">
        <div class="bar-head"><span class="bar-name">Machine Learning</span><span class="bar-pct">78%</span></div>
        <div class="bar-track"><div class="bar-fill bf-c" data-w="78"></div></div>
      </div>
      <div class="bar-wrap">
        <div class="bar-head"><span class="bar-name">Generative AI / LLMs</span><span class="bar-pct">74%</span></div>
        <div class="bar-track"><div class="bar-fill bf-m" data-w="74"></div></div>
      </div>
      <div class="bar-wrap">
        <div class="bar-head"><span class="bar-name">Power BI &amp; Data Analytics</span><span class="bar-pct">81%</span></div>
        <div class="bar-track"><div class="bar-fill bf-g" data-w="81"></div></div>
      </div>
      <div class="bar-wrap">
        <div class="bar-head"><span class="bar-name">SQL</span><span class="bar-pct">76%</span></div>
        <div class="bar-track"><div class="bar-fill bf-c" data-w="76"></div></div>
      </div>
      <div class="bar-wrap">
        <div class="bar-head"><span class="bar-name">LangChain / LangGraph</span><span class="bar-pct">65%</span></div>
        <div class="bar-track"><div class="bar-fill bf-m" data-w="65"></div></div>
      </div>
    </div>
  </div>

  <!-- GITHUB STATS -->
  <div class="sec">
    <div class="sec-top-line"></div>
    <div class="sh sh-g"><span class="sh-arr">▶</span> GitHub Stats</div>
    <div class="stat-grid">
      <div class="stat-card"><span class="snum" id="s1">0</span><div class="slbl">COMMITS</div></div>
      <div class="stat-card"><span class="snum" id="s2">0</span><div class="slbl">REPOS</div></div>
      <div class="stat-card"><span class="snum" id="s3">0</span><div class="slbl">STARS</div></div>
      <div class="stat-card"><span class="snum" id="s4">0</span><div class="slbl">CONTRIB</div></div>
    </div>
  </div>

  <!-- GOAL -->
  <div class="sec">
    <div class="sec-top-line"></div>
    <div class="sh sh-c"><span class="sh-arr">▶</span> Goal &amp; Vision</div>
    <div class="goal-box">
      <div class="goal-txt">🚀 BUILD INTELLIGENT AI SYSTEMS<br>THAT SOLVE REAL-WORLD PROBLEMS</div>
      <div class="goal-sub">Open Source Learner · AI Enthusiast · Future AI Engineer</div>
    </div>
  </div>

  <!-- CONNECT -->
  <div class="sec">
    <div class="sec-top-line"></div>
    <div class="sh sh-m"><span class="sh-arr">▶</span> Connect With Me</div>
    <div class="connect-row">
      <a class="cbtn cb1" href="https://www.linkedin.com/in/spandan-parhi-852011414" target="_blank">💼 LinkedIn</a>
      <a class="cbtn cb2" href="https://github.com/spandanparhi-crypto" target="_blank">⚡ GitHub</a>
      <a class="cbtn cb3" href="mailto:spandanparhi019@gmail.com">✉️ Gmail</a>
    </div>
    <a class="portfolio-btn" href="https://fragile-green-8utzxh0t.edgeone.dev/" target="_blank">🌐 VIEW PORTFOLIO</a>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <strong>⚡ SPANDAN PARHI</strong> · Transforming Data Into Intelligence
    <div class="footer-dots">
      <div class="fd"></div>
      <div class="fd"></div>
      <div class="fd"></div>
    </div>
  </div>

</div>

<script>
// Typewriter
const roles = [
  "Data Science Engineer 📊",
  "Machine Learning Enthusiast 🧠",
  "Generative AI Explorer 🤖",
  "Agentic AI Builder ⚡",
  "Python Developer 🐍",
  "Building AI-Powered Solutions 🚀"
];
let ri = 0, ci = 0, del = false;
const el = document.getElementById('typ');
function type() {
  const r = roles[ri];
  if (!del) {
    el.textContent = r.slice(0, ++ci);
    if (ci === r.length) { del = true; setTimeout(type, 2000); return; }
  } else {
    el.textContent = r.slice(0, --ci);
    if (ci === 0) { del = false; ri = (ri + 1) % roles.length; }
  }
  setTimeout(type, del ? 40 : 80);
}
type();

// Count-up stats
function countUp(id, end, dur) {
  const e = document.getElementById(id);
  let c = 0;
  const step = end / 60;
  const t = setInterval(() => {
    c += step;
    if (c >= end) { e.textContent = end + (end >= 100 ? '+' : ''); clearInterval(t); }
    else e.textContent = Math.round(c);
  }, dur / 60);
}
setTimeout(() => {
  countUp('s1', 150, 1200);
  countUp('s2', 18, 1000);
  countUp('s3', 42, 1100);
  countUp('s4', 200, 1300);
}, 800);

// Skill bars on scroll
const ob = new IntersectionObserver(es => {
  es.forEach(e => {
    if (e.isIntersecting) {
      e.target.querySelectorAll('.bar-fill').forEach(b => b.style.width = b.dataset.w + '%');
      ob.unobserve(e.target);
    }
  });
}, { threshold: 0.3 });
const bd = document.getElementById('bars');
if (bd) ob.observe(bd);
</script>
</body>
</html>
