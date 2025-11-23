---
layout: none
---

<style>
  :root {
    color-scheme: dark;
    --bg: #050b16;
    --panel: #0b172d;
    --panel-2: #0f203f;
    --frame: #1e3a8a;
    --accent: #7dd3fc;
    --text: #d0e7ff;
    --muted: #9fbadf;
    --grid: rgba(13, 33, 63, 0.5);
    --glow: rgba(126, 199, 255, 0.4);
  }
  * { box-sizing: border-box; }
  html, body {
    margin: 0;
    width: 100%;
    height: 100%;
    background: radial-gradient(circle at 20% 20%, rgba(20, 92, 162, 0.35), transparent 32%),
                radial-gradient(circle at 80% 0%, rgba(120, 53, 15, 0.25), transparent 34%),
                var(--bg);
    color: var(--text);
    font-family: "IBM Plex Mono", "Fira Code", "SFMono-Regular", Menlo, Consolas, monospace;
  }
  .page {
    min-height: 100vh;
    padding: 32px 18px 42px;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .terminal {
    width: min(1200px, 100%);
    background: linear-gradient(135deg, rgba(10, 22, 45, 0.94), rgba(8, 18, 35, 0.9));
    border: 2px solid var(--frame);
    border-radius: 18px;
    box-shadow: 0 18px 50px rgba(0, 0, 0, 0.55), 0 0 22px var(--glow);
    overflow: hidden;
  }
  .terminal__top {
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 14px 18px;
    background: linear-gradient(90deg, #0f203f, #0a162d);
    border-bottom: 1px solid rgba(30, 58, 138, 0.7);
  }
  .lights { display: flex; gap: 10px; }
  .light {
    width: 14px; height: 14px; border-radius: 50%; opacity: 0.8; position: relative;
    box-shadow: 0 0 12px currentColor;
  }
  .light.green { color: #10b981; background: currentColor; animation: pulse 3s infinite; }
  .light.amber { color: #f59e0b; background: currentColor; animation: pulse 2.4s infinite; }
  .light.red   { color: #ef4444; background: currentColor; animation: pulse 2.1s infinite; }
  @keyframes pulse { 0%, 100% { opacity: 0.55; } 50% { opacity: 1; } }
  .brand {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    color: var(--accent);
    letter-spacing: 0.8px;
    font-size: 14px;
  }
  .brand__logo {
    width: 32px; height: 32px; border-radius: 50%; background: #0ea5e9; color: #050b16;
    display: grid; place-items: center; font-weight: 700; font-size: 16px; text-decoration: none;
    box-shadow: 0 0 16px rgba(14, 165, 233, 0.55);
  }
  .grid {
    background-image: linear-gradient(var(--grid) 1px, transparent 1px),
                      linear-gradient(90deg, var(--grid) 1px, transparent 1px);
    background-size: 28px 28px;
    background-position: -12px -12px;
    position: relative;
  }
  .grid::after {
    content: "";
    position: absolute;
    inset: 0;
    backdrop-filter: blur(1px);
    pointer-events: none;
    opacity: 0.2;
  }
  .content {
    position: relative;
    padding: 30px 32px 26px;
  }
  .prompt { color: var(--accent); font-size: 15px; margin-top: 10px; }
  .line { color: var(--text); font-size: 18px; margin: 6px 0 14px; }
  .type-row {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 18px;
    margin: 8px 0 18px;
    white-space: nowrap;
  }
  .type {
    --typing-width: 720px;
    position: relative;
    display: inline-block;
    width: var(--typing-width);
    border-right: 2px solid var(--accent);
    overflow: hidden;
    white-space: nowrap;
    animation: typing 8s steps(45, end) infinite, blink 1.3s step-end infinite;
  }
  @keyframes typing {
    0%   { width: 0; }
    60%  { width: var(--typing-width); }
    75%  { width: var(--typing-width); }
    100% { width: 0; }
  }
  @keyframes blink { 0%, 55% { border-color: var(--accent); } 60%, 100% { border-color: transparent; } }
  .columns {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 18px;
    margin-top: 10px;
  }
  @media (max-width: 860px) {
    .columns { grid-template-columns: 1fr; }
    .type { --typing-width: 92vw; max-width: 92vw; }
  }
  .panel {
    background: var(--panel-2);
    border: 1px solid rgba(30, 58, 138, 0.65);
    border-radius: 12px;
    padding: 16px 14px 18px;
    box-shadow: inset 0 0 0 1px rgba(0,0,0,0.35);
  }
  .panel h3 { margin: 0 0 10px; color: var(--accent); font-size: 15px; letter-spacing: 0.6px; }
  .note { color: var(--muted); font-size: 13px; margin-top: 8px; line-height: 1.5; }
  textarea, label input[type="radio"] {
    accent-color: var(--accent);
  }
  textarea {
    width: 100%;
    height: 140px;
    background: #0b172d;
    color: var(--text);
    border: 1px solid var(--frame);
    border-radius: 10px;
    padding: 12px;
    font-family: inherit;
    font-size: 14px;
    resize: vertical;
  }
  .menu label { display: block; margin-bottom: 8px; color: var(--text); font-size: 14px; }
  .footer {
    padding: 12px 20px 16px;
    background: rgba(15, 32, 63, 0.6);
    border-top: 1px solid rgba(30, 58, 138, 0.7);
    color: var(--muted);
    font-size: 13px;
  }
</style>

<div class="page">
  <div class="terminal grid" role="img" aria-label="Retro terminal card introducing Matt, with typing line and local-only inputs.">
    <div class="terminal__top">
      <div class="lights">
        <span class="light green"></span>
        <span class="light amber"></span>
        <span class="light red"></span>
      </div>
      <div class="brand">
        <a class="brand__logo" href="https://matty.lol" target="_blank" rel="noreferrer noopener">M</a>
        <span>matthew@matty.lol:~</span>
      </div>
    </div>

    <div class="content">
      <div class="prompt">$ whoami</div>
      <div class="line">Matt — developer &amp; cryptocurrency trader.</div>

      <div class="prompt">$ status</div>
      <div class="line">Always learning new things.</div>

      <div class="prompt">$ echo</div>
      <div class="type-row">
        <span class="type">blog-style console vibes — type locally, explore options, enjoy the glow.</span>
      </div>

      <div class="prompt">$ menu</div>
      <div class="line">Pick a path or type in the scratchpad.</div>

      <div class="columns">
        <div class="panel">
          <h3>Scratchpad</h3>
          <textarea aria-label="Scratchpad" placeholder="Type anything here — it stays on your device."></textarea>
          <div class="note">Input is local-only. GitHub Pages does not run scripts, so nothing is stored or sent.</div>
        </div>
        <div class="panel menu">
          <h3>Menu</h3>
          <label><input type="radio" name="menu" checked> View this profile summary</label>
          <label><input type="radio" name="menu"> Jump to <a href="https://matty.lol" style="color: var(--accent);">matty.lol</a></label>
          <label><input type="radio" name="menu"> Browse projects below</label>
          <label><input type="radio" name="menu"> Leave a note in the scratchpad</label>
          <div class="note">Radio choices are for the vibe — GitHub Pages keeps them static.</div>
        </div>
      </div>
    </div>

    <div class="footer">Fullscreen retro terminal — built inside README.md for GitHub Pages.</div>
  </div>
</div>
