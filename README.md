<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0
<defs>
<!-- Background gradient: deep slate, intentional cool cast -->
<linearGradient id="bg" x1="0" y1="0" x2="1" y2="1">
<stop offset="0" stop-color="#0a0f1a"/>
<stop offset="0.55" stop-color="#0d1320"/>
<stop offset="1" stop-color="#070b14"/>
</linearGradient>
<radialGradient id="aura" cx="0.78" cy="0.42" r="0.55">
<stop offset="0" stop-color="#1e3a5f" stop-opacity="0.55"/>
<stop offset="1" stop-color="#0a0f1a" stop-opacity="0"/>
</radialGradient>
<linearGradient id="shieldFill" x1="0" y1="0" x2="0" y2="1">
<stop offset="0" stop-color="#14213a"/>
<stop offset="1" stop-color="#0c1424"/>
</linearGradient>
<linearGradient id="steel" x1="0" y1="0" x2="1" y2="0">
<stop offset="0" stop-color="#7da7d9"/>
<stop offset="1" stop-color="#4f7fb5"/>
</linearGradient>
<linearGradient id="nameGrad" x1="0" y1="0" x2="1" y2="0">
<stop offset="0" stop-color="#eaf1fb"/>
<stop offset="1" stop-color="#acc4e6"/>
</linearGradient>
<filter id="glow" x="-60%" y="-60%" width="220%" height="220%">
<feGaussianBlur stdDeviation="6" result="b"/>
<feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
</filter>
<filter id="soft" x="-40%" y="-40%" width="180%" height="180%">
<feGaussianBlur stdDeviation="2.2"/>
</filter>
<!-- Cloud symbol -->
<g id="cloud">
<ellipse cx="0" cy="0" rx="34" ry="22"/>
<ellipse cx="30" cy="6" rx="26" ry="18"/>
<ellipse cx="-30" cy="7" rx="24" ry="16"/>
<rect x="-52" y="4" width="104" height="18" rx="9"/>
</g>
</defs>
<!-- Base -->
<rect width="1200" height="300" fill="url(#bg)"/>
<rect width="1200" height="300" fill="url(#aura)"/>
<!-- Faint infrastructure grid -->
<g stroke="#21304a" stroke-width="1" opacity="0.25">
<line x1="0" y1="75" x2="1200" y2="75"/>
<line x1="0" y1="150" x2="1200" y2="150"/>
<line x1="0" y1="225" x2="1200" y2="225"/>
<line x1="300" y1="0" x2="300" y2="300"/>
<line x1="600" y1="0" x2="600" y2="300"/>
<line x1="900" y1="0" x2="900" y2="300"/>
</g>
<!-- Drifting clouds (slow, layered, low opacity) -->
<g fill="#9fb8d8">
<g opacity="0.06">
<use href="#cloud"/>
<animateTransform attributeName="transform" type="translate" from="-140 60" to="1360 60
</g>
<g opacity="0.10">
<use href="#cloud" transform="scale(0.7)"/>
<animateTransform attributeName="transform" type="translate" from="-200 215" to="1360 2
</g>
<g opacity="0.05">
<use href="#cloud" transform="scale(1.25)"/>
<animateTransform attributeName="transform" type="translate" from="-260 130" to="1420 1
</g>
</g>
<!-- Flowing telemetry line: name -> shield (automation/monitoring motif) -->
<g stroke="url(#steel)" stroke-width="1.6" fill="none" opacity="0.5">
<path id="flow" d="M 70 215 H 560 C 660 215 690 150 820 150" stroke-dasharray="6 12">
<animate attributeName="stroke-dashoffset" from="180" to="0" dur="3.2s" repeatCount="in
</path>
</g>
<circle r="3" fill="#ff9d2e">
<animateMotion dur="3.2s" repeatCount="indefinite" rotate="auto">
<mpath href="#flow"/>
</animateMotion>
</circle>
<!-- Left text block -->
<text x="64" y="132" font-family="Georgia, 'Times New Roman', serif" font-size="62" font-we
<text x="68" y="170" font-family="'Segoe UI', Helvetica, Arial, sans-serif" font-size="17"
<!-- Cloud-shield signature (right) -->
<g transform="translate(880,150)">
<!-- pulsing aura -->
<g filter="url(#soft)">
<path d="M0,-78 L56,-54 L56,8 C56,56 0,86 0,86 C0,86 -56,56 -56,8 L-56,-54 Z" fill="#3f
<animate attributeName="opacity" values="0.10;0.30;0.10" dur="4.5s" repeatCount="inde
</path>
</g>
<!-- shield body -->
<path d="M0,-72 L52,-50 L52,8 C52,52 0,80 0,80 C0,80 -52,52 -52,8 L-52,-50 Z"
fill="url(#shieldFill)" stroke="url(#steel)" stroke-width="2.5"/>
<!-- cloud crest on shield -->
<g fill="#cfe0f5" opacity="0.92" transform="translate(0,-26) scale(0.62)">
<use href="#cloud"/>
</g>
<!-- lock -->
<g transform="translate(0,22)">
<path d="M-12,-4 a12,12 0 0,1 24,0" fill="none" stroke="#ff9d2e" stroke-width="4.5" str
<rect x="-16" y="-4" width="32" height="26" rx="5" fill="#0c1424" stroke="#ff9d2e" stro
<circle cx="0" cy="7" r="3.2" fill="#ff9d2e"/>
<rect x="-1.6" y="7" width="3.2" height="8" rx="1.6" fill="#ff9d2e"/>
</g>
<!-- orbiting node -->
<g>
<circle cx="0" cy="0" r="3" fill="#7da7d9">
<animateTransform attributeName="transform" type="rotate" from="0 0 0" to="360 0 0" d
</circle>
<g>
<circle cx="74" cy="0" r="3.4" fill="#9fc2ef"/>
<animateTransform attributeName="transform" type="rotate" from="0 0 0" to="360 0 0" d
</g>
<g>
<circle cx="-74" cy="0" r="2.6" fill="#5a86c0"/>
<animateTransform attributeName="transform" type="rotate" from="180 0 0" to="540 0 0"
</g>
</g>
</g>
<!-- floating accent dots -->
<g fill="#7da7d9">
<circle cx="1080" cy="70" r="2.4" opacity="0.7">
<animate attributeName="cy" values="70;58;70" dur="6s" repeatCount="indefinite"/>
</circle>
<circle cx="1130" cy="200" r="2" opacity="0.5">
<animate attributeName="cy" values="200;212;200" dur="7s" repeatCount="indefinite"/>
</circle>
<circle cx="770" cy="230" r="2.2" opacity="0.6">
<animate attributeName="cy" values="230;220;230" dur="5.5s" repeatCount="indefinite"/>
</circle>
</g>
<!-- bottom hairline accent -->
<rect x="64" y="186" width="190" height="2" rx="1" fill="url(#steel)" opacity="0.8"/>
</svg>







<p align="center">
  <img src="profile.majed.png" width="100%">
</p>
## Hi there 👋

I'm Majed.

Cloud Engineer | Cybersecurity | Cloud Security | Automation

- ☁️ Focused on AWS and cloud infrastructure
- 🔒 Interested in cloud security and monitoring
- 🛠️ Building hands-on labs and automation projects
- 🐧 Working with Linux, Python, and GitHub
