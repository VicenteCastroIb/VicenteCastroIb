

    <linearGradient id="ringGrad" x1="0%" y1="0%" x2="100%" y2="100%"><svg width="1200" height="280" viewBox="0 0 1200 280" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" role="img" aria-label="Vicente Castro — Full-Stack Developer">
  <defs>
    <linearGradient id="bgGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#0b1120"/>
      <stop offset="50%" stop-color="#111827"/>
      <stop offset="100%" stop-color="#0b1120"/>
    </linearGradient>
    <linearGradient id="nameGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#22d3ee"/>
      <stop offset="50%" stop-color="#818cf8"/>
      <stop offset="100%" stop-color="#c084fc"/>
    </linearGradient>
    <linearGradient id="ringGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#22d3ee"/>
      <stop offset="100%" stop-color="#c084fc"/>
    </linearGradient>
    <linearGradient id="monoGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#1e293b"/>
      <stop offset="100%" stop-color="#0f172a"/>
    </linearGradient>
    <linearGradient id="borderGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#22d3ee" stop-opacity="0.55"/>
      <stop offset="50%" stop-color="#6366f1" stop-opacity="0.35"/>
      <stop offset="100%" stop-color="#c084fc" stop-opacity="0.55"/>
    </linearGradient>
    <clipPath id="bannerClip">
      <rect x="1" y="1" width="1198" height="278" rx="22"/>
    </clipPath>
    <filter id="blur1" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="45"/>
    </filter>
  </defs>

  <style>
    .blob { animation-iteration-count: infinite; animation-timing-function: ease-in-out; animation-direction: alternate; }
    .b1 { animation-name: blobMove1; animation-duration: 11s; }
    .b2 { animation-name: blobMove2; animation-duration: 13s; }
    @keyframes blobMove1 { 0% { transform: translate(0,0); } 100% { transform: translate(70px,-25px); } }
    @keyframes blobMove2 { 0% { transform: translate(0,0); } 100% { transform: translate(-80px,30px); } }

    .particle { opacity: 0; animation-name: drift; animation-iteration-count: infinite; animation-timing-function: ease-in-out; }
    @keyframes drift {
      0%   { opacity: 0; transform: translateY(0px); }
      10%  { opacity: .55; }
      50%  { transform: translateY(-16px); }
      90%  { opacity: .55; }
      100% { opacity: 0; transform: translateY(-2px); }
    }

    .badge { opacity: 0; animation: badgeIn .6s ease-out forwards; }
    @keyframes badgeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

    .tag { opacity: 0; animation: tagFade 16s ease-in-out infinite; }
    @keyframes tagFade {
      0%   { opacity: 0; transform: translateY(6px); }
      3%   { opacity: 1; transform: translateY(0); }
      20%  { opacity: 1; transform: translateY(0); }
      23%  { opacity: 0; transform: translateY(-6px); }
      100% { opacity: 0; }
    }

    .pulseDot { animation: pulse 2s ease-in-out infinite; transform-origin: center; }
    @keyframes pulse { 0%,100% { opacity: 1; transform: scale(1); } 50% { opacity: .35; transform: scale(1.6); } }

    .cursor { animation: blink 1s steps(1) infinite; }
    @keyframes blink { 0%,49% { opacity: 1; } 50%,100% { opacity: 0; } }

    text { font-family: 'Segoe UI', 'Helvetica Neue', Arial, sans-serif; }
    .mono { font-family: 'Consolas', 'SF Mono', Menlo, monospace; }
  </style>

  <g clip-path="url(#bannerClip)">
    <rect x="0" y="0" width="1200" height="280" fill="url(#bgGrad)"/>

    <circle class="blob b1" cx="220" cy="150" r="150" fill="#22d3ee" opacity="0.16" filter="url(#blur1)"/>
    <circle class="blob b2" cx="960" cy="190" r="180" fill="#a855f7" opacity="0.14" filter="url(#blur1)"/>

    <g class="mono" fill="#a5b4fc">
      <text class="particle" x="860" y="60" font-size="20" style="animation-duration:6s; animation-delay:.2s">&lt;/&gt;</text>
      <text class="particle" x="1020" y="110" font-size="16" style="animation-duration:7s; animation-delay:1.4s">{ }</text>
      <text class="particle" x="930" y="220" font-size="18" style="animation-duration:5.5s; animation-delay:.8s">=&gt;</text>
      <text class="particle" x="1100" y="70" font-size="14" style="animation-duration:6.5s; animation-delay:2s">01</text>
      <text class="particle" x="780" y="150" font-size="15" style="animation-duration:8s; animation-delay:.5s">&lt;/&gt;</text>
    </g>

    <!-- avatar monogram -->
    <g transform="translate(110,140)">
      <circle r="68" fill="url(#monoGrad)" stroke="url(#ringGrad)" stroke-width="2"/>
      <circle r="76" fill="none" stroke="url(#ringGrad)" stroke-width="1.5" stroke-dasharray="6 10" opacity="0.6">
        <animateTransform attributeName="transform" type="rotate" from="0 0 0" to="360 0 0" dur="18s" repeatCount="indefinite"/>
      </circle>
      <text x="0" y="16" text-anchor="middle" font-size="40" font-weight="700" fill="url(#nameGrad)">VC</text>
      <circle cx="50" cy="50" r="9" fill="#0b1120"/>
      <circle class="pulseDot" cx="50" cy="50" r="9" fill="none"/>
      <circle cx="50" cy="50" r="5.5" fill="#34d399"/>
    </g>

    <!-- name + tagline -->
    <text x="215" y="108" font-size="38" font-weight="700" fill="url(#nameGrad)">Vicente Castro</text>

    <g class="mono">
      <text class="tag" x="216" y="142" font-size="18" fill="#cbd5e1" style="animation-delay:0s">Full-Stack Developer<tspan class="cursor" fill="#22d3ee">|</tspan></text>
      <text class="tag" x="216" y="142" font-size="18" fill="#cbd5e1" style="animation-delay:4s">Next.js · TypeScript · Java · Spring Boot<tspan class="cursor" fill="#22d3ee">|</tspan></text>
      <text class="tag" x="216" y="142" font-size="18" fill="#cbd5e1" style="animation-delay:8s">Real projects, real clients<tspan class="cursor" fill="#22d3ee">|</tspan></text>
      <text class="tag" x="216" y="142" font-size="18" fill="#cbd5e1" style="animation-delay:12s">Open to freelance &amp; contract work<tspan class="cursor" fill="#22d3ee">|</tspan></text>
    </g>

    <!-- tech badges -->
    <g font-size="14" font-weight="600">
      <g class="badge" style="animation-delay:.05s">
        <rect x="216" y="170" width="100" height="32" rx="16" fill="#0f172a" stroke="#38bdf8" stroke-opacity=".55"/>
        <text x="266" y="191" text-anchor="middle" fill="#e2e8f0">Next.js</text>
      </g>
      <g class="badge" style="animation-delay:.12s">
        <rect x="326" y="170" width="118" height="32" rx="16" fill="#0f172a" stroke="#3178c6" stroke-opacity=".7"/>
        <text x="385" y="191" text-anchor="middle" fill="#e2e8f0">TypeScript</text>
      </g>
      <g class="badge" style="animation-delay:.19s">
        <rect x="454" y="170" width="90" height="32" rx="16" fill="#0f172a" stroke="#61dafb" stroke-opacity=".7"/>
        <text x="499" y="191" text-anchor="middle" fill="#e2e8f0">React</text>
      </g>
      <g class="badge" style="animation-delay:.26s">
        <rect x="554" y="170" width="82" height="32" rx="16" fill="#0f172a" stroke="#ed8b00" stroke-opacity=".7"/>
        <text x="595" y="191" text-anchor="middle" fill="#e2e8f0">Java</text>
      </g>
      <g class="badge" style="animation-delay:.33s">
        <rect x="646" y="170" width="126" height="32" rx="16" fill="#0f172a" stroke="#6db33f" stroke-opacity=".7"/>
        <text x="709" y="191" text-anchor="middle" fill="#e2e8f0">Spring Boot</text>
      </g>
      <g class="badge" style="animation-delay:.4s">
        <rect x="782" y="170" width="118" height="32" rx="16" fill="#0f172a" stroke="#336791" stroke-opacity=".8"/>
        <text x="841" y="191" text-anchor="middle" fill="#e2e8f0">PostgreSQL</text>
      </g>
      <g class="badge" style="animation-delay:.47s">
        <rect x="910" y="170" width="92" height="32" rx="16" fill="#0f172a" stroke="#38bdf8" stroke-opacity=".55"/>
        <text x="956" y="191" text-anchor="middle" fill="#e2e8f0">Tailwind</text>
      </g>
      <g class="badge" style="animation-delay:.54s">
        <rect x="1012" y="170" width="88" height="32" rx="16" fill="#0f172a" stroke="#94a3b8" stroke-opacity=".7"/>
        <text x="1056" y="191" text-anchor="middle" fill="#e2e8f0">Git</text>
      </g>
    </g>

    <!-- stats + status -->
    <text x="216" y="228" font-size="14" fill="#94a3b8" class="mono">38 Repositories&#160;&#160;·&#160;&#160;23 Stars&#160;&#160;·&#160;&#160;Pull Shark Achievement</text>

    <g transform="translate(966,26)">
      <rect x="0" y="0" width="220" height="30" rx="15" fill="#0f172a" stroke="#34d399" stroke-opacity=".6"/>
      <circle cx="20" cy="15" r="4" fill="#0b1120"/>
      <circle class="pulseDot" cx="20" cy="15" r="4" fill="none"/>
      <circle cx="20" cy="15" r="3" fill="#34d399"/>
      <text x="34" y="20" font-size="12.5" fill="#d1fae5" class="mono">Open to freelance work</text>
    </g>

    <text x="600" y="260" text-anchor="middle" font-size="12.5" fill="#64748b" class="mono">github.com/VicenteCastroIb&#160;&#160;·&#160;&#160;linkedin.com/in/vicente-castro1&#160;&#160;·&#160;&#160;Chile</text>

    <rect x="1" y="1" width="1198" height="278" rx="22" fill="none" stroke="url(#borderGrad)" stroke-width="2"/>
  </g>
</svg>

      <stop offset="0%" stop-color="#22d3ee"/>
      <stop offset="100%" stop-color="#c084fc"/>
    </linearGradient>
    <linearGradient id="monoGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#1e293b"/>
      <stop offset="100%" stop-color="#0f172a"/>
    </linearGradient>
    <linearGradient id="borderGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#22d3ee" stop-opacity="0.55"/>
      <stop offset="50%" stop-color="#6366f1" stop-opacity="0.35"/>
      <stop offset="100%" stop-color="#c084fc" stop-opacity="0.55"/>
    </linearGradient>
    <clipPath id="bannerClip">
      <rect x="1" y="1" width="1198" height="278" rx="22"/>
    </clipPath>
    <filter id="blur1" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="45"/>
    </filter>
  </defs>

  <style>
    .blob { animation-iteration-count: infinite; animation-timing-function: ease-in-out; animation-direction: alternate; }
    .b1 { animation-name: blobMove1; animation-duration: 11s; }
    .b2 { animation-name: blobMove2; animation-duration: 13s; }
    @keyframes blobMove1 { 0% { transform: translate(0,0); } 100% { transform: translate(70px,-25px); } }
    @keyframes blobMove2 { 0% { transform: translate(0,0); } 100% { transform: translate(-80px,30px); } }

    .particle { opacity: 0; animation-name: drift; animation-iteration-count: infinite; animation-timing-function: ease-in-out; }
    @keyframes drift {
      0%   { opacity: 0; transform: translateY(0px); }
      10%  { opacity: .55; }
      50%  { transform: translateY(-16px); }
      90%  { opacity: .55; }
      100% { opacity: 0; transform: translateY(-2px); }
    }

    .badge { opacity: 0; animation: badgeIn .6s ease-out forwards; }
    @keyframes badgeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

    .tag { opacity: 0; animation: tagFade 16s ease-in-out infinite; }
    @keyframes tagFade {
      0%   { opacity: 0; transform: translateY(6px); }
      3%   { opacity: 1; transform: translateY(0); }
      20%  { opacity: 1; transform: translateY(0); }
      23%  { opacity: 0; transform: translateY(-6px); }
      100% { opacity: 0; }
    }

    .pulseDot { animation: pulse 2s ease-in-out infinite; transform-origin: center; }
    @keyframes pulse { 0%,100% { opacity: 1; transform: scale(1); } 50% { opacity: .35; transform: scale(1.6); } }

    .cursor { animation: blink 1s steps(1) infinite; }
    @keyframes blink { 0%,49% { opacity: 1; } 50%,100% { opacity: 0; } }

    text { font-family: 'Segoe UI', 'Helvetica Neue', Arial, sans-serif; }
    .mono { font-family: 'Consolas', 'SF Mono', Menlo, monospace; }
  </style>

  <g clip-path="url(#bannerClip)">
    <rect x="0" y="0" width="1200" height="280" fill="url(#bgGrad)"/>

    <circle class="blob b1" cx="220" cy="150" r="150" fill="#22d3ee" opacity="0.16" filter="url(#blur1)"/>
    <circle class="blob b2" cx="960" cy="190" r="180" fill="#a855f7" opacity="0.14" filter="url(#blur1)"/>

    <g class="mono" fill="#a5b4fc">
      <text class="particle" x="860" y="60" font-size="20" style="animation-duration:6s; animation-delay:.2s">&lt;/&gt;</text>
      <text class="particle" x="1020" y="110" font-size="16" style="animation-duration:7s; animation-delay:1.4s">{ }</text>
      <text class="particle" x="930" y="220" font-size="18" style="animation-duration:5.5s; animation-delay:.8s">=&gt;</text>
      <text class="particle" x="1100" y="70" font-size="14" style="animation-duration:6.5s; animation-delay:2s">01</text>
      <text class="particle" x="780" y="150" font-size="15" style="animation-duration:8s; animation-delay:.5s">&lt;/&gt;</text>
    </g>

    <!-- avatar monogram -->
    <g transform="translate(110,140)">
      <circle r="68" fill="url(#monoGrad)" stroke="url(#ringGrad)" stroke-width="2"/>
      <circle r="76" fill="none" stroke="url(#ringGrad)" stroke-width="1.5" stroke-dasharray="6 10" opacity="0.6">
        <animateTransform attributeName="transform" type="rotate" from="0 0 0" to="360 0 0" dur="18s" repeatCount="indefinite"/>
      </circle>
      <text x="0" y="16" text-anchor="middle" font-size="40" font-weight="700" fill="url(#nameGrad)">VC</text>
      <circle cx="50" cy="50" r="9" fill="#0b1120"/>
      <circle class="pulseDot" cx="50" cy="50" r="9" fill="none"/>
      <circle cx="50" cy="50" r="5.5" fill="#34d399"/>
    </g>

    <!-- name + tagline -->
    <text x="215" y="108" font-size="38" font-weight="700" fill="url(#nameGrad)">Vicente Castro</text>

    <g class="mono">
      <text class="tag" x="216" y="142" font-size="18" fill="#cbd5e1" style="animation-delay:0s">Full-Stack Developer<tspan class="cursor" fill="#22d3ee">|</tspan></text>
      <text class="tag" x="216" y="142" font-size="18" fill="#cbd5e1" style="animation-delay:4s">Next.js · TypeScript · Java · Spring Boot<tspan class="cursor" fill="#22d3ee">|</tspan></text>
      <text class="tag" x="216" y="142" font-size="18" fill="#cbd5e1" style="animation-delay:8s">Real projects, real clients<tspan class="cursor" fill="#22d3ee">|</tspan></text>
      <text class="tag" x="216" y="142" font-size="18" fill="#cbd5e1" style="animation-delay:12s">Open to freelance &amp; contract work<tspan class="cursor" fill="#22d3ee">|</tspan></text>
    </g>

    <!-- tech badges -->
    <g font-size="14" font-weight="600">
      <g class="badge" style="animation-delay:.05s">
        <rect x="216" y="170" width="100" height="32" rx="16" fill="#0f172a" stroke="#38bdf8" stroke-opacity=".55"/>
        <text x="266" y="191" text-anchor="middle" fill="#e2e8f0">Next.js</text>
      </g>
      <g class="badge" style="animation-delay:.12s">
        <rect x="326" y="170" width="118" height="32" rx="16" fill="#0f172a" stroke="#3178c6" stroke-opacity=".7"/>
        <text x="385" y="191" text-anchor="middle" fill="#e2e8f0">TypeScript</text>
      </g>
      <g class="badge" style="animation-delay:.19s">
        <rect x="454" y="170" width="90" height="32" rx="16" fill="#0f172a" stroke="#61dafb" stroke-opacity=".7"/>
        <text x="499" y="191" text-anchor="middle" fill="#e2e8f0">React</text>
      </g>
      <g class="badge" style="animation-delay:.26s">
        <rect x="554" y="170" width="82" height="32" rx="16" fill="#0f172a" stroke="#ed8b00" stroke-opacity=".7"/>
        <text x="595" y="191" text-anchor="middle" fill="#e2e8f0">Java</text>
      </g>
      <g class="badge" style="animation-delay:.33s">
        <rect x="646" y="170" width="126" height="32" rx="16" fill="#0f172a" stroke="#6db33f" stroke-opacity=".7"/>
        <text x="709" y="191" text-anchor="middle" fill="#e2e8f0">Spring Boot</text>
      </g>
      <g class="badge" style="animation-delay:.4s">
        <rect x="782" y="170" width="118" height="32" rx="16" fill="#0f172a" stroke="#336791" stroke-opacity=".8"/>
        <text x="841" y="191" text-anchor="middle" fill="#e2e8f0">PostgreSQL</text>
      </g>
      <g class="badge" style="animation-delay:.47s">
        <rect x="910" y="170" width="92" height="32" rx="16" fill="#0f172a" stroke="#38bdf8" stroke-opacity=".55"/>
        <text x="956" y="191" text-anchor="middle" fill="#e2e8f0">Tailwind</text>
      </g>
      <g class="badge" style="animation-delay:.54s">
        <rect x="1012" y="170" width="88" height="32" rx="16" fill="#0f172a" stroke="#94a3b8" stroke-opacity=".7"/>
        <text x="1056" y="191" text-anchor="middle" fill="#e2e8f0">Git</text>
      </g>
    </g>

    <!-- stats + status -->
    <text x="216" y="228" font-size="14" fill="#94a3b8" class="mono">38 Repositories&#160;&#160;·&#160;&#160;23 Stars&#160;&#160;·&#160;&#160;Pull Shark Achievement</text>

    <g transform="translate(966,26)">
      <rect x="0" y="0" width="220" height="30" rx="15" fill="#0f172a" stroke="#34d399" stroke-opacity=".6"/>
      <circle cx="20" cy="15" r="4" fill="#0b1120"/>
      <circle class="pulseDot" cx="20" cy="15" r="4" fill="none"/>
      <circle cx="20" cy="15" r="3" fill="#34d399"/>
      <text x="34" y="20" font-size="12.5" fill="#d1fae5" class="mono">Open to freelance work</text>
    </g>

    <text x="600" y="260" text-anchor="middle" font-size="12.5" fill="#64748b" class="mono">github.com/VicenteCastroIb&#160;&#160;·&#160;&#160;linkedin.com/in/vicente-castro1&#160;&#160;·&#160;&#160;Chile</text>

    <rect x="1" y="1" width="1198" height="278" rx="22" fill="none" stroke="url(#borderGrad)" stroke-width="2"/>
  </g>
</svg>

- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
