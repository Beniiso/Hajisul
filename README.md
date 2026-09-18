<div align="center">

<img src="./assets/hero.svg" width="900">

<br>

<img src="./assets/focus.svg" width="900">

<br>

<h3>BUILDING TOWARD AI ENGINEERING</h3>

<p>
Python · Mathematics · Machine Learning · AI Systems
</p>

<br>

<img src="./assets/contribution-graph.svg" width="900">

<br>

<img src="./assets/activity.svg" width="900">

<br>

<sub>
Web Design · WordPress · Elementor · JavaScript · Tailwind CSS · Plugin Development · Vibe Coding
</sub>

</div>

---

<!-- assets/hero.svg -->

<svg xmlns="http://www.w3.org/2000/svg" width="900" height="220" viewBox="0 0 900 220">
<rect width="900" height="220" rx="16" fill="#050505"/>
<g stroke="#181818">
<path d="M0 55H900M0 110H900M0 165H900"/>
<path d="M90 0V220M180 0V220M270 0V220M360 0V220M450 0V220M540 0V220M630 0V220M720 0V220M810 0V220"/>
</g>
<text x="450" y="105" text-anchor="middle" fill="#fff" font-family="monospace" font-size="70" font-weight="700">BENI</text>
<text x="450" y="142" text-anchor="middle" fill="#666" font-family="monospace" font-size="14">BUILD • LEARN • ENGINEER</text>
<circle cx="450" cy="174" r="3" fill="#fff">
<animate attributeName="r" values="2;7;2" dur="1.5s" repeatCount="indefinite"/>
<animate attributeName="opacity" values=".2;1;.2" dur="1.5s" repeatCount="indefinite"/>
</circle>
</svg>

<!-- assets/focus.svg -->

<svg xmlns="http://www.w3.org/2000/svg" width="900" height="260" viewBox="0 0 900 260">
<rect width="900" height="260" rx="16" fill="#050505"/>
<text x="45" y="40" fill="#555" font-family="monospace" font-size="13">CURRENT_FOCUS // 2026</text>

<g stroke="#292929" stroke-width="2">
<path d="M90 130H810"/>
</g>

<g fill="#050505" stroke="#aaa" stroke-width="2">
<circle cx="100" cy="130" r="19"/>
<circle cx="275" cy="130" r="19"/>
<circle cx="450" cy="130" r="19"/>
<circle cx="625" cy="130" r="19"/>
<circle cx="800" cy="130" r="19"/>
</g>

<g fill="#fff" font-family="monospace" font-size="12" text-anchor="middle">
<text x="100" y="177">PYTHON</text>
<text x="275" y="177">MATH</text>
<text x="450" y="177">ML</text>
<text x="625" y="177">AI SYSTEMS</text>
<text x="800" y="177">AI ENG.</text>
</g>

<circle cx="100" cy="130" r="5" fill="#fff">
<animate attributeName="cx" values="100;275;450;625;800;100" dur="7s" repeatCount="indefinite"/>
</circle>

<text x="450" y="225" text-anchor="middle" fill="#555" font-family="monospace" font-size="11">
learn → understand → implement → deploy
</text>
</svg>

<!-- .github/workflows/contributions.yml -->

name: Generate Contribution Graph

on:
schedule:
- cron: "0 0 * * *"
workflow_dispatch:
push:
branches:
- main

permissions:
contents: write

jobs:
generate:
runs-on: ubuntu-latest

```
steps:
  - uses: actions/checkout@v6

  - uses: leereilly/contribution-graph-art@v1
    with:
      github_user_name: ${{ github.repository_owner }}
      github_token: ${{ secrets.GITHUB_TOKEN }}
      output_path: assets/contribution-graph.svg
      animation_mode: tetromino
      tetromino_count: "4"
      palette: github-dark
      animation_duration: "8"

  - name: Commit
    run: |
      git config user.name "github-actions[bot]"
      git config user.email "41898282+github-actions[bot]@users.noreply.github.com"
      git add assets/contribution-graph.svg
      git diff --cached --quiet || git commit -m "chore: update contribution graph"
      git push
```

<!-- .github/workflows/activity.yml -->

name: Generate Activity

on:
schedule:
- cron: "17 3 * * *"
workflow_dispatch:
push:
branches:
- main

permissions:
contents: write

jobs:
generate:
runs-on: ubuntu-latest

```
steps:
  - uses: actions/checkout@v6

  - uses: seijikohara/profile-cards-action@v1
    with:
      github-token: ${{ secrets.GITHUB_TOKEN }}
      username: ${{ github.repository_owner }}
      cards: contributions,rhythm
      output-dir: assets
      themes: dark
      commit: true
      commit-message: "chore: update activity"
```

<!-- assets/activity.svg -->

<svg xmlns="http://www.w3.org/2000/svg" width="900" height="220" viewBox="0 0 900 220">
<rect width="900" height="220" rx="16" fill="#050505"/>
<text x="40" y="42" fill="#777" font-family="monospace" font-size="13">ACTIVITY / SYSTEM OUTPUT</text>
<path d="M40 165 L90 150 L140 158 L190 125 L240 140 L290 95 L340 115 L390 75 L440 105 L490 60 L540 92 L590 48 L640 80 L690 55 L740 70 L790 38 L850 50"
fill="none" stroke="#fff" stroke-width="2"/>
<circle cx="40" cy="165" r="4" fill="#fff">
<animate attributeName="cx" values="40;850;40" dur="5s" repeatCount="indefinite"/>
</circle>
<g fill="#444" font-family="monospace" font-size="10">
<text x="40" y="190">LOW</text>
<text x="820" y="190">HIGH</text>
</g>
</svg>
