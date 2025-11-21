<div align="center">
  <svg viewBox="0 0 900 520" xmlns="http://www.w3.org/2000/svg" role="img" aria-labelledby="title desc">
    <title id="title">Matthew Halden // Terminal Blog</title>
    <desc id="desc">A retro terminal-inspired card with animated typing and blinking cursor.</desc>
    <defs>
      <linearGradient id="matrix" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" stop-color="#0f172a" />
        <stop offset="50%" stop-color="#0b1323" />
        <stop offset="100%" stop-color="#0a0f1d" />
      </linearGradient>
      <pattern id="grid" width="22" height="22" patternUnits="userSpaceOnUse">
        <path d="M 22 0 L 0 0 0 22" fill="none" stroke="#0d213f" stroke-width="1" opacity="0.5" />
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
        text { font-family: "IBM Plex Mono", "Fira Code", "SFMono-Regular", Menlo, Consolas, monospace; }
        .title { fill: #8ef6ff; font-size: 22px; letter-spacing: 1.6px; }
        .section { fill: #7dd3fc; font-size: 14px; }
        .body { fill: #d0e7ff; font-size: 15px; }
      </style>
    </defs>

    <rect x="0" y="0" width="900" height="520" fill="url(#matrix)" />
    <rect x="0" y="0" width="900" height="520" fill="url(#grid)" opacity="0.28">
      <animate attributeName="opacity" values="0.18;0.28;0.18" dur="8s" repeatCount="indefinite" />
    </rect>
    <rect x="28" y="28" width="844" height="464" rx="18" ry="18" fill="#0a162d" stroke="#1e3a8a" stroke-width="2.2" filter="url(#glow)" />

    <rect x="52" y="52" width="796" height="40" rx="9" ry="9" fill="#0f203f" stroke="#1b3b73" />
    <circle cx="76" cy="72" r="8" fill="#10b981" opacity="0.9">
      <animate attributeName="opacity" values="0.55;1;0.55" dur="3s" repeatCount="indefinite" />
    </circle>
    <circle cx="102" cy="72" r="8" fill="#f59e0b" opacity="0.9">
      <animate attributeName="opacity" values="0.55;1;0.55" dur="2.4s" repeatCount="indefinite" />
    </circle>
    <circle cx="128" cy="72" r="8" fill="#ef4444" opacity="0.9">
      <animate attributeName="opacity" values="0.55;1;0.55" dur="2.1s" repeatCount="indefinite" />
    </circle>
    <text x="156" y="76" class="section" dominant-baseline="middle">matthew@earth:~</text>

    <g transform="translate(68,120)">
      <text x="0" y="0" class="title">// TERMINAL BLOG — rendered in GH Markdown</text>
      <text x="0" y="34" class="section">$ whoami</text>
      <text x="110" y="34" class="body">Matthew Halden — building delightful developer experiences &amp; friendly interfaces.</text>

      <text x="0" y="68" class="section">$ uptime</text>
      <text x="110" y="68" class="body">Calgary, AB · fueled by espresso &amp; curiosity · shipping small wins daily.</text>

      <text x="0" y="102" class="section">$ focus</text>
      <text x="110" y="102" class="body">Designing humane tooling · modern web stacks · interactive docs · playful UX.</text>

      <text x="0" y="136" class="section">$ stack</text>
      <text x="110" y="136" class="body">TypeScript / React · Next.js · Node · CSS-in-JS · d3 · Go APIs · cloud bits.</text>

      <text x="0" y="170" class="section">$ reading</text>
      <text x="110" y="170" class="body">Pattern Language · Shape Up · Designing Data-Intensive Apps · Atomic Habits.</text>

      <text x="0" y="204" class="section">$ open-tabs</text>
      <text x="110" y="204" class="body">Tactile web toys · calm productivity · meaningful docs · better onboarding.</text>

      <clipPath id="typing-mask">
        <rect x="0" y="0" width="620" height="28">
          <animate attributeName="width" values="0;620;620;0" keyTimes="0;0.65;0.82;1" dur="7.5s" repeatCount="indefinite" />
        </rect>
      </clipPath>
      <text x="0" y="248" class="section">$ now</text>
      <g transform="translate(110,248)">
        <text class="body" clip-path="url(#typing-mask)">crafting a retro-coded blog feel right inside this README — stay awhile.</text>
        <rect x="4" y="-16" width="12" height="22" fill="#7dd3fc" opacity="0.95">
          <animate attributeName="x" values="4;616;616;4" keyTimes="0;0.65;0.82;1" dur="7.5s" repeatCount="indefinite" />
          <animate attributeName="opacity" values="1;0;1" dur="1.4s" repeatCount="indefinite" />
        </rect>
      </g>
    </g>

    <text x="68" y="474" class="section" opacity="0.8">CTRL+C to exit · CTRL+N to keep exploring · rendered with SVG + CSS animation</text>
  </svg>
</div>

---

### 💾 What you'll find here
- Code experiments, web toys, and explorations into calm productivity.
- Occasional notes about design systems, developer experience, and learning in public.
- Retro terminal vibes because shiny pixels should still feel human.

### 🎛️ Make it yours
Want this style? Tweak the SVG colors, gradients, or the animated typing line in `README.md` to match your handle. Add more `$ commands` to narrate your story.
