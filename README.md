## 👾 Suzane Bianca

**`Desenvolvedora`**

### Sobre mim:

### 💻 Linguagens e Tecnologias

<img 
  align="left"
  alt="SWIFT"
  title="SWIFT"
  width="30px"
  style="padding-right: 10px"
  src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/swift/swift-original.svg"
/>

<img 
  align="left"
  alt="C++"
  title="C++"
  width="30px"
  style="padding-right: 10px"
  src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/cplusplus/cplusplus-original.svg"     
/>

<img 
  align="left"
  alt="PYTHON"
  title="PYTHON"
  width="30px"
  style="padding-right: 10px"
  src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg"      
/>

<img 
  align="left"
  alt="PYTHON"
  title="PYTHON"
  width="30px"
  style="padding-right: 10px"
  src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg"      
/>

<img 
  align="left"
  alt="JAVA"
  title="JAVA"
  width="30px"
  style="padding-right: 10px"
  src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/java/java-original.svg"   
/>

<img 
  align="left"
  alt="HTML"
  title="HTML"
  width="30px"
  style="padding-right: 10px"
  src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/html5/html5-original.svg"
/>

<img 
  align="left"
  alt="CSS"
  title="CSS"
  width="30px"
  style="padding-right: 10px"
  src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/css3/css3-original.svg"
/>

<img 
  align="left"
  alt="GIT"
  title="GIT"
  width="30px"
  style="padding-right: 10px"
  src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/git/git-original.svg"
/>

<img 
  align="left"
  alt="GITHUB"
  title="GITHUB"
  width="30px"
  style="padding-right: 10px"
  src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/github/github-original.svg"        
/>

<img 
  align="left"
  alt="GODOT"
  title="GODOT"
  width="30px"
  style="padding-right: 10px"
  src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/godot/godot-original.svg"            
/>

<br/>
<br/>

### 📈 Estatísticas

```bash
name: Update README cards

on:
  schedule:
    - cron: "0 0 * * *" # Runs once daily at midnight
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest

    permissions:
      contents: write

    steps:
      - uses: actions/checkout@v6

      - name: Generate stats card
        uses: stats-organization/github-readme-stats-action@v2
        with:
          card: stats
          options: username=${{ github.repository_owner }}&show_icons=true
          path: profile/stats.svg
          token: ${{ secrets.GITHUB_TOKEN }}

      - name: Generate top languages card
        uses: stats-organization/github-readme-stats-action@v2
        with:
          card: top-langs
          options: username=${{ github.repository_owner }}&layout=compact&langs_count=6
          path: profile/top-langs.svg
          token: ${{ secrets.GITHUB_TOKEN }}

      - name: Generate pin card
        uses: stats-organization/github-readme-stats-action@v2
        with:
          card: pin
          options: username=stats-organization&repo=github-readme-stats
          path: profile/pin-stats-organization-github-readme-stats.svg
          token: ${{ secrets.GITHUB_TOKEN }}

      - name: Commit cards
        run: |
          git config user.name "github-actions[bot]"
          git config user.email "41898282+github-actions[bot]@users.noreply.github.com"
          git add profile/*.svg
          git commit -m "Update README cards" || exit 0
          git push

```
