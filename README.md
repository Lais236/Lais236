## Bem Vindo(a)! 👋

- 👩🏻‍💻 Estou cursando Desenvolvimento de Sistemas
- ✉ Entre em contato: laisjonnsson@gmail.com
##
<div>
 <a href="https://github.com/Lais236/github-readme-stats"> <img height=200 align="center" src="https://github-readme-stats.vercel.app/api?username=Lais236&theme=dracula&rank_icon=github" />
<div>
   <a href="https://instagram.com/jonnssonlais/" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
<div>
name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: rafaballerini
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  
