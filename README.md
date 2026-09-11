<div align="center">

<!-- ============ ANIMATED WAVE BANNER ============ -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,25&height=220&section=header&text=YOUR_NAME&fontSize=65&fontColor=39FF14&animation=fadeIn&fontAlignY=35&desc=just%20here%20to%20build%20stuff%20and%20see%20what%20happens&descAlignY=53&descSize=18&descColor=B026FF" />

<!-- ============ TYPING ANIMATION ============ -->
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=26&duration=3000&pause=1000&color=39FF14&center=true&vCenter=true&width=650&lines=building+things+for+no+reason;shipping+code+at+3am;seeing+what+happens;probably+breaking+prod+rn;send+help" />

<br/>

<!-- ============ SOCIAL BADGES ============ -->
<a href="https://linkedin.com/in/YOUR_LINK"><img src="https://img.shields.io/badge/LinkedIn-39FF14?style=for-the-badge&logo=linkedin&logoColor=black" /></a>
<a href="https://twitter.com/YOUR_HANDLE"><img src="https://img.shields.io/badge/Twitter-B026FF?style=for-the-badge&logo=twitter&logoColor=white" /></a>
<a href="mailto:YOUR_EMAIL"><img src="https://img.shields.io/badge/Email-0D1117?style=for-the-badge&logo=gmail&logoColor=39FF14" /></a>
<a href="https://YOUR_PORTFOLIO.com"><img src="https://img.shields.io/badge/Portfolio-0D1117?style=for-the-badge&logo=vercel&logoColor=B026FF" /></a>

</div>

<br/>

<!-- ============ TERMINAL-STYLE INTRO ============ -->
```yaml
$ whoami
role: "figuring it out"
status: "shipping stuff, breaking stuff, fixing stuff"
current_focus: "whatever's interesting this week"
philosophy: "build first, ask questions never"
```

<br/>

<div align="center">

### 🛠️ `tech_stack --all`

<img src="https://skillicons.dev/icons?i=js,ts,python,react,nextjs,nodejs,go,rust,docker,kubernetes,git,linux,aws,gcp,postgres,mongodb,redis,graphql&theme=dark&perline=9" />

</div>

<br/>

<div align="center">

### 📊 `github_stats.fetch()`

<img height="165em" src="https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=github_dark&hide_border=true&bg_color=0D1117&title_color=39FF14&icon_color=B026FF&text_color=C9D1D9&include_all_commits=true&count_private=true" />
<img height="165em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_USERNAME&layout=compact&theme=github_dark&hide_border=true&bg_color=0D1117&title_color=39FF14&text_color=C9D1D9&langs_count=10" />

<br/>

<img src="https://github-readme-streak-stats.herokuapp.com/?user=YOUR_USERNAME&theme=github-dark-blue&hide_border=true&background=0D1117&ring=39FF14&fire=B026FF&currStreakLabel=39FF14&sideLabels=C9D1D9" />

<br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=YOUR_USERNAME&theme=react-dark&bg_color=0D1117&color=39FF14&line=B026FF&point=39FF14&hide_border=true&area=true" width="90%"/>

</div>

<br/>

<div align="center">

### 🏆 `trophies.unlock()`

<img src="https://github-profile-trophy.vercel.app/?username=YOUR_USERNAME&theme=algolia&no-frame=true&no-bg=true&margin-w=12&row=1&column=7" />

</div>

<br/>

<div align="center">

### 🐍 `contribution_graph.eat()`

<!-- Snake animation -- requires a GitHub Action, see setup notes below -->
<img src="https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_USERNAME/output/github-contribution-grid-snake-dark.svg" width="90%"/>

</div>

<br/>

<div align="center">

### 🧊 `contribution_calendar.render(mode="3d")`

<!-- 3D isometric contribution calendar -- requires a GitHub Action, see setup notes below -->
<img src="https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_USERNAME/output/github-profile-3d-contrib/profile-night-green.svg" width="90%"/>

</div>

<br/>

<div align="center">

### 🎧 `now_playing.stream()`

<!-- Spotify widget -- get your UID from spotify-github-profile.vercel.app -->
<img src="https://spotify-github-profile.vercel.app/api/view?uid=YOUR_SPOTIFY_UID&cover_image=true&theme=default&show_offline=true&background_color=0D1117&bar_color=39FF14&bar_color_cover=false" />

</div>

<br/>

<div align="center">

### ⌨️ `wakatime.hours()`

<!-- WakaTime weekly coding stats -- requires wakatime account + waka-readme-stats action -->
<!--START_SECTION:waka-->
```txt
From: WakaTime setup needed — see notes below
```
<!--END_SECTION:waka-->

</div>

<br/>

<div align="center">

<img src="https://komarev.com/ghpvc/?username=YOUR_USERNAME&label=PROFILE+VIEWS&color=39FF14&style=for-the-badge" />

<br/><br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,25&height=120&section=footer" />

</div>
# Setup: `.github/workflows/` files needed

Create these in the repo named exactly your GitHub username (e.g. `octocat/octocat`).

---

## 1. Snake animation — `.github/workflows/snake.yml`
```yaml
name: generate snake
on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch: {}
  push:
    branches: [main]
jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
      - uses: crazy-max/ghaction-github-pages@v3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

## 2. 3D contribution calendar — `.github/workflows/profile-3d.yml`
```yaml
name: GitHub-Profile-3D-Contrib
on:
  schedule:
    - cron: "0 18 * * *"
  workflow_dispatch:
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: yoshi389111/github-profile-3d-contrib@0.7.1
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          USERNAME: ${{ github.repository_owner }}
      - name: Commit & Push
        run: |
          git config user.name github-actions
          git config user.email github-actions@github.com
          git add -A .
          git commit -m "generated" || exit 0
          git push
```
Then swap `profile-night-green.svg` in the README for whichever style you like — options are `profile-green-animate.svg`, `profile-season.svg`, `profile-night-view.svg`, `profile-night-rainbow.svg`, `profile-gitblock.svg`, all inside `profile-3d-contrib/` on the `output` branch.

## 3. WakaTime hours — `.github/workflows/waka.yml`
Requires a free WakaTime account (tracks coding time via editor plugin) and a `WAKATIME_API_KEY` secret.
```yaml
name: Waka Readme
on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch: {}
jobs:
  update-readme:
    runs-on: ubuntu-latest
    steps:
      - uses: athul/waka-readme@master
        with:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
          GH_TOKEN: ${{ secrets.GH_TOKEN }}
```
If you don't code with a WakaTime-tracked editor day to day, delete that whole section from the README instead — an empty/broken stat block looks worse than no stat block.

## 4. Spotify widget
No Action needed — just get your UID by logging in at spotify-github-profile.vercel.app and swap `YOUR_SPOTIFY_UID` in the README.

---

**Order of operations:** push the README first (the plain widgets like stats/trophies/streak work immediately), then add workflows one at a time and manually trigger each once via the Actions tab (`Run workflow`) so the SVGs generate before you rely on the auto-schedule.
