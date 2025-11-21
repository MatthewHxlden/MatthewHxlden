<div align="center" style="width:100%;">
  <svg viewBox="0 0 1600 620" xmlns="http://www.w3.org/2000/svg" role="img" aria-labelledby="title desc" style="width:100vw;max-width:100%;height:80vh;min-height:520px;">
    <title id="title">Matt // Retro Terminal Spread</title>
    <desc id="desc">A full-width retro terminal banner with a blinking cursor, typing animation, and optional scratchpad inputs.</desc>
    <defs>
      <linearGradient id="matrix" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" stop-color="#0f172a" />
        <stop offset="50%" stop-color="#0b1323" />
        <stop offset="100%" stop-color="#0a0f1d" />
      </linearGradient>
      <pattern id="grid" width="26" height="26" patternUnits="userSpaceOnUse">
        <path d="M 26 0 L 0 0 0 26" fill="none" stroke="#0d213f" stroke-width="1" opacity="0.5" />
      </pattern>
      <filter id="glow">
        <feGaussianBlur stdDeviation="4" result="coloredBlur" />
        <feMerge>
          <feMergeNode in="coloredBlur" />
          <feMergeNode in="SourceGraphic" />
        </feMerge>
      </filter>
      <style>
        @keyframes headerPulse { 0%, 100% { opacity: 0.8; } 50% { opacity: 1; } }
        @keyframes faintGlow { from { opacity: 0.15; } to { opacity: 0.35; } }
        @keyframes cursorBlink { 0%, 45% { opacity: 1; } 50%, 100% { opacity: 0; } }
        @keyframes typeLine {
          0% { width: 0; }
          65% { width: 640px; }
          80% { width: 640px; }
          100% { width: 0; }
        }
        text { font-family: "IBM Plex Mono", "Fira Code", "SFMono-Regular", Menlo, Consolas, monospace; }
        .title { fill: #8ef6ff; font-size: 26px; letter-spacing: 1.8px; }
        .section { fill: #7dd3fc; font-size: 15px; }
        .body { fill: #d0e7ff; font-size: 16px; }
        .logo { fill: #0ea5e9; }
      </style>
    </defs>

    <rect x="0" y="0" width="1600" height="620" fill="url(#matrix)" />
    <rect x="0" y="0" width="1600" height="620" fill="url(#grid)" opacity="0.28">
      <animate attributeName="opacity" values="0.18;0.28;0.18" dur="8s" repeatCount="indefinite" />
    </rect>
    <rect x="46" y="46" width="1508" height="528" rx="22" ry="22" fill="#0a162d" stroke="#1e3a8a" stroke-width="2.6" filter="url(#glow)" />

    <rect x="84" y="84" width="1432" height="48" rx="12" ry="12" fill="#0f203f" stroke="#1b3b73" />
    <circle cx="120" cy="108" r="10" fill="#10b981" opacity="0.9">
      <animate attributeName="opacity" values="0.55;1;0.55" dur="3s" repeatCount="indefinite" />
    </circle>
    <circle cx="152" cy="108" r="10" fill="#f59e0b" opacity="0.9">
      <animate attributeName="opacity" values="0.55;1;0.55" dur="2.4s" repeatCount="indefinite" />
    </circle>
    <circle cx="184" cy="108" r="10" fill="#ef4444" opacity="0.9">
      <animate attributeName="opacity" values="0.55;1;0.55" dur="2.1s" repeatCount="indefinite" />
    </circle>

    <g transform="translate(228,108)">
      <text x="0" y="0" class="section" dominant-baseline="middle">matthew@matty.lol:~</text>
      <a href="https://matty.lol" target="_blank" rel="noreferrer noopener">
        <circle cx="-78" cy="0" r="14" class="logo" opacity="0.95" />
        <text x="-78" y="4" text-anchor="middle" class="body" font-size="12" fill="#0f172a" font-weight="700">M</text>
      </a>
    </g>

    <g transform="translate(108,184)">
      <text x="0" y="0" class="title">// terminal log</text>

      <text x="0" y="40" class="section">$ whoami</text>
      <text x="126" y="40" class="body">Matt — developer &amp; cryptocurrency trader.</text>

      <text x="0" y="78" class="section">$ status</text>
      <text x="126" y="78" class="body">Always learning new things.</text>

      <text x="0" y="116" class="section">$ site</text>
      <a href="https://matty.lol" target="_blank" rel="noreferrer noopener">
        <text x="126" y="116" class="body" text-decoration="underline">matty.lol</text>
      </a>

      <text x="0" y="154" class="section">$ echo</text>
      <g transform="translate(126,154)">
        <rect x="0" y="-20" width="940" height="30" fill="none" clip-path="url(#typing-mask)" />
        <clipPath id="typing-mask">
          <rect x="0" y="-22" width="940" height="30">
            <animate attributeName="width" dur="8s" repeatCount="indefinite" keyTimes="0;0.65;0.82;1" values="0;940;940;0" />
          </rect>
        </clipPath>
        <text class="body" clip-path="url(#typing-mask)">blog-style vibes, typewriter flow, blinking cursor — you're in.</text>
        <rect x="6" y="-18" width="12" height="24" fill="#7dd3fc" opacity="0.95">
          <animate attributeName="x" values="6;938;938;6" keyTimes="0;0.65;0.82;1" dur="8s" repeatCount="indefinite" />
          <animate attributeName="opacity" values="1;0;1" dur="1.4s" repeatCount="indefinite" />
        </rect>
      </g>

      <text x="0" y="196" class="section">$ menu</text>
      <text x="126" y="196" class="body">Select an option below or type in the scratchpad.</text>
      <text x="126" y="234" class="body" opacity="0.75">Tip: use the scratchpad to jot anything &mdash; it stays on your device.</text>
    </g>

    <text x="108" y="558" class="section" opacity="0.8">Fullscreen-friendly spread with a local scratchpad; GitHub keeps it static, but the vibe stays interactive.</text>
  </svg>
</div>

<div align="center">
  <table style="max-width: 1100px; width: 100%; border: 1px solid #1e3a8a; border-radius: 12px; background: #0a162d; color: #d0e7ff; font-family: 'IBM Plex Mono', 'Fira Code', monospace; padding: 18px;">
    <tr>
      <td style="width: 35%; vertical-align: top; padding-right: 16px;">
        <div style="margin-bottom: 10px; color: #7dd3fc; font-weight: 700;">Scratchpad</div>
        <textarea aria-label="Type here" placeholder="Type anything here—it's local to you." style="width: 100%; height: 120px; background: #0f203f; color: #d0e7ff; border: 1px solid #1e3a8a; border-radius: 8px; padding: 10px; resize: vertical;"></textarea>
        <div style="margin-top: 8px; font-size: 12px; color: #7dd3fc;">Local-only input (GitHub READMEs don't run scripts).</div>
      </td>
      <td style="width: 65%; vertical-align: top;">
        <div style="margin-bottom: 10px; color: #7dd3fc; font-weight: 700;">Menu</div>
        <label style="display: block; margin-bottom: 6px;"><input type="radio" name="menu" checked> View profile summary (above)</label>
        <label style="display: block; margin-bottom: 6px;"><input type="radio" name="menu"> Jump to <a href="https://matty.lol" style="color: #8ef6ff;">matty.lol</a></label>
        <label style="display: block; margin-bottom: 6px;"><input type="radio" name="menu"> See projects on this page</label>
        <label style="display: block; margin-bottom: 6px;"><input type="radio" name="menu"> Leave a note in the scratchpad</label>
        <div style="margin-top: 10px; font-size: 13px; color: #9fbadf;">These toggles are for the vibe—GitHub keeps interactions local and static.</div>
      </td>
    </tr>
  </table>
</div>
