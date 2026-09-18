<!-- README.md --> <div align="center"> <img src="./assets/hero.svg" width="900" alt="Beni"/> <br> <img src="./assets/focus.svg" width="820" alt="Current focus"/> </div> <br> <h2 align="center">CURRENTLY BUILDING</h2> <div align="center">

PYTHON · MATHEMATICS · MACHINE LEARNING · AI SYSTEMS · AI ENGINEERING

</div> <br> <div align="center"> <img src="./assets/ai-system.svg" width="820" alt="AI Engineering"/> </div> <br> <h2 align="center">BACKGROUND</h2> <div align="center">

Web Design · WordPress · Elementor · Plugin Development · JavaScript · Tailwind CSS · Figma · Vibe Coding

</div> <br> <h2 align="center">ACTIVITY</h2> <div align="center"> <img src="./assets/contributions.svg" width="900" alt="GitHub contribution graph"/> </div> <br> <div align="center"> <img src="./assets/streak.svg" width="495" alt="GitHub streak"/> </div> <br> <div align="center"> <a href="https://github.com/Hajisul"> <img src="https://img.shields.io/badge/GitHub-000?style=flat-square&logo=github&logoColor=fff"/> </a> <a href="https://github.com/Hajisul?tab=repositories"> <img src="https://img.shields.io/badge/Repositories-000?style=flat-square&logo=github&logoColor=fff"/> </a> </div> <br> <div align="center">

<sub>Building systems, not just interfaces.</sub>

</div> <!-- assets/hero.svg --> <svg xmlns="http://www.w3.org/2000/svg" width="900" height="230" viewBox="0 0 900 230"> <rect width="900" height="230" rx="18" fill="#050505"/> <g fill="none" stroke="#222"> <path d="M0 46H900M0 92H900M0 138H900M0 184H900"/> <path d="M90 0V230M180 0V230M270 0V230M360 0V230M450 0V230M540 0V230M630 0V230M720 0V230M810 0V230"/> </g> <text x="50%" y="105" text-anchor="middle" fill="#fff" font-family="monospace" font-size="68" font-weight="700">BENI</text> <text x="50%" y="145" text-anchor="middle" fill="#777" font-family="monospace" font-size="16">BUILDING TOWARD AI ENGINEERING</text> <circle cx="450" cy="175" r="3" fill="#fff"> <animate attributeName="r" values="2;7;2" dur="1.8s" repeatCount="indefinite"/> <animate attributeName="opacity" values=".3;1;.3" dur="1.8s" repeatCount="indefinite"/> </circle> </svg> <!-- assets/focus.svg --> <svg xmlns="http://www.w3.org/2000/svg" width="820" height="250" viewBox="0 0 820 250"> <rect width="820" height="250" rx="18" fill="#050505"/> <g font-family="monospace"> <text x="42" y="38" fill="#777" font-size="13">CURRENT_PATH / 2026</text> <g stroke="#333" stroke-width="2"> <path d="M90 125H730"/> </g> <g fill="#050505" stroke="#fff" stroke-width="2"> <circle cx="100" cy="125" r="18"/> <circle cx="245" cy="125" r="18"/> <circle cx="390" cy="125" r="18"/> <circle cx="535" cy="125" r="18"/> <circle cx="680" cy="125" r="18"/> </g> <g fill="#fff" font-size="12" text-anchor="middle"> <text x="100" y="169">PYTHON</text> <text x="245" y="169">MATH</text> <text x="390" y="169">ML</text> <text x="535" y="169">AI SYSTEMS</text> <text x="680" y="169">AI ENG.</text> </g> <circle cx="100" cy="125" r="5" fill="#fff"> <animate attributeName="cx" values="100;245;390;535;680;100" dur="7s" repeatCount="indefinite"/> </circle> <g fill="#777" font-size="11"> <text x="42" y="220">learn → understand → implement → deploy → engineer</text> </g> </g> </svg> <!-- assets/ai-system.svg --> <svg xmlns="http://www.w3.org/2000/svg" width="820" height="250" viewBox="0 0 820 250"> <rect width="820" height="250" rx="18" fill="#050505"/> <g stroke="#292929" stroke-width="1"> <path d="M0 50H820M0 100H820M0 150H820M0 200H820"/> <path d="M82 0V250M164 0V250M246 0V250M328 0V250M410 0V250M492 0V250M574 0V250M656 0V250M738 0V250"/> </g> <g font-family="monospace"> <g fill="#050505" stroke="#aaa" stroke-width="1.5"> <rect x="55" y="90" width="125" height="60" rx="8"/> <rect x="245" y="90" width="125" height="60" rx="8"/> <rect x="435" y="90" width="125" height="60" rx="8"/> <rect x="625" y="90" width="125" height="60" rx="8"/> </g> <g fill="#fff" font-size="14" text-anchor="middle"> <text x="117" y="125">DATA</text> <text x="307" y="125">MODEL</text> <text x="497" y="125">INFERENCE</text> <text x="687" y="125">SYSTEM</text> </g> <g stroke="#777" stroke-width="2"> <path d="M180 120H245"/> <path d="M370 120H435"/> <path d="M560 120H625"/> </g> <circle cx="180" cy="120" r="4" fill="#fff"> <animate attributeName="cx" values="180;245;370;435;560;625" dur="4s" repeatCount="indefinite"/> </circle>

<text x="410" y="40" text-anchor="middle" fill="#777" font-size="13">FROM MODELS → TO REAL SYSTEMS</text>
</g>
</svg>

<!-- .github/workflows/profile.yml -->

name: Update GitHub Profile

on:
schedule:
- cron: "0 3 * * *"
workflow_dispatch:

permissions:
contents: write

jobs:
contributions:
runs-on: ubuntu-latest
