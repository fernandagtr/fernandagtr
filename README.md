# 👩🏻‍💻 Fernanda Oliveira

**`Estudante Segurança da Informação`**

Me chamo Fernanda Oliveira, tenho 20 anos e de São Paulo. Estou cursando Segurança da Informação na Universidade Paulista - UNIP. Estou implementando em conjunto com o head de TI da minha empresa a área de segurança da informação. Atuando fortemente na GRC garantindo que a empresa opere com ética, em conformidade com leis e normas, gerenciando os riscos de forma proativa e que mantenha com uma governança eficiente.
/>
</a>
<a href="https://github.com/fernandagtr/fernandagtr?tab=repositories&sort=stargazers">
<img alt="total stars" tittle="Total stars on Github" src="https://custon-icon-badges.demolab.com/github/stars/fernandagtr?color=55960c&style-for-the-badge&labelColor488207&logo=star"/>
/>
</a>
<a href="https://github.com/fernandagtr?tab=followers">
<img
alt="followers"
title="Follow me on Github"
scr="https//custom-icon-badges.demolab.com/gitbub/followers/fernandagtr?color=236ad3&labelcolorColor=1155ba&style=for-the-badge&logo=person-add&label=Follow&logoColor=while"

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
      # Summary Cards
      - uses: actions/checkout@v2
      - uses: vn7n24fzkq/github-profile-summary-cards@release
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        with:
          USERNAME: ${{ github.repository_owner }}

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

