# Setup — Sathishkumar S GitHub Profile README

This is a "special" GitHub profile README — the one that shows on your
profile page above your pinned repos.

## 1. Create the special repo
Create a new **public** repository named **exactly** your username:

```
SathishkumarSivakumar
```

(GitHub auto-detects a repo with this exact name and shows its README on
your profile page.)

## 2. Add these files, keeping this exact structure

```
SathishkumarSivakumar/
├── README.md
├── assets/
│   ├── header.svg
│   ├── footer.svg
│   ├── divider.svg
│   ├── skills-radar.svg     (new — radar chart in Tech Stack section)
│   └── stats-strip.svg      (new — impact numbers under the hero)
└── .github/
    └── workflows/
        └── snake.yml        (optional — animates your contribution graph)
```

The header/footer/divider SVGs are custom-designed for this README (dark
navy + cyan + amber, matching your portfolio site) — they're referenced
with **relative paths** (`./assets/header.svg`), so the `assets` folder
must sit next to `README.md` in the repo root.

## 3. Push it
```bash
git init
git add .
git commit -m "Update profile README"
git branch -M main
git remote add origin https://github.com/SathishkumarSivakumar/SathishkumarSivakumar.git
git push -u origin main
```

## 4. Enable the contribution snake (optional but recommended)
The snake animation needs a one-time Action run:
1. Push `.github/workflows/snake.yml` (already included).
2. Go to your repo → **Actions** tab → run "Generate Snake Animation" manually once (or wait for the daily cron).
3. It creates an `output` branch with the generated SVGs — the README already points at it, so it'll just start working.
4. Make sure **Settings → Actions → General → Workflow permissions** is set to "Read and write permissions" or the push step will fail.

## 5. Things worth double-checking / personalizing
- **GitHub stats accuracy**: `count_private=true` in the stats badge only shows private-repo counts to *you* when logged in — visitors see public-only, which is normal.
- **Streak stats service**: uses `streak-stats.demolab.com` (the actively maintained mirror — the old `herokuapp.com` one is dead).
- **Mosquito-repellent project**: no public repo link was available, so it's listed without a "View on GitHub" link. Add one if you publish it.
- I removed the Naukri/Indeed badges from the earlier draft since those links weren't pointing to your actual profiles — happy to add them back with the real URLs if you want them in.

## Color tokens used (for future edits)
| Token | Hex |
|---|---|
| Background | `#070b10` |
| Surface | `#0d141b` |
| Cyan (primary accent) | `#5fe3c8` |
| Amber (secondary accent) | `#f2a154` |
| Text | `#e9eef2` |
| Muted text | `#8ea0ac` |
<!--
  Sathishkumar S — GitHub Profile README
  Design system: dark navy (#070b10) · cyan (#5fe3c8) · amber (#f2a154)
  matches sathishkumar-sivakumar.netlify.app for a consistent personal brand.

  SETUP
  1. Create a repo named EXACTLY: SathishkumarSivakumar (must match your username)
  2. Add this file as README.md at the repo root
  3. Add the /assets folder (header.svg, footer.svg, divider.svg) alongside it
  4. (Optional) Add .github/workflows/snake.yml to animate your contribution graph
-->

<a name="top"></a>
<div align="center">
<img src="./assets/header.svg" width="100%" alt="Sathishkumar S — Data Science & AI Engineering" />
</div>

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=2800&pause=1000&color=5FE3C8&center=true&vCenter=true&width=720&lines=Turning+raw+data+into+decisions+people+trust;Python+%7C+SQL+%7C+Machine+Learning+%7C+NLP+%7C+Power+BI;Shipping+dashboards%2C+not+just+notebooks." alt="Typing headline" />

<br/>

<img src="./assets/waveform.svg" width="100%" alt="" />

<br/>

<img src="https://img.shields.io/badge/OPEN%20TO-Data%20Science%20Roles-5fe3c8?style=for-the-badge&labelColor=070b10" alt="Open to work" />
<img src="https://img.shields.io/badge/BASED%20IN-Chennai%2C%20India-f2a154?style=for-the-badge&labelColor=070b10" alt="Location" />
<img src="https://img.shields.io/badge/FOCUS-ML%20%C2%B7%20NLP%20%C2%B7%20BI-e9eef2?style=for-the-badge&labelColor=070b10" alt="Focus" />

<br/><br/>

<a href="mailto:kumar109662@gmail.com"><img src="https://img.shields.io/badge/-Email-070b10?style=for-the-badge&logo=gmail&logoColor=EA4335" alt="Email" /></a>
<a href="https://www.linkedin.com/in/sathishkumar-sivakumar/"><img src="https://img.shields.io/badge/-LinkedIn-070b10?style=for-the-badge&logo=linkedin&logoColor=0A66C2" alt="LinkedIn" /></a>
<a href="https://github.com/SathishkumarSivakumar"><img src="https://img.shields.io/badge/-GitHub-070b10?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" /></a>
<a href="https://sathishkumar-sivakumar.netlify.app"><img src="https://img.shields.io/badge/-Portfolio-070b10?style=for-the-badge&logo=vercel&logoColor=5fe3c8" alt="Portfolio" /></a>
<a href="tel:+919789704124"><img src="https://img.shields.io/badge/-Call-070b10?style=for-the-badge&logo=whatsapp&logoColor=25D366" alt="Phone" /></a>

<br/><br/>

<img src="https://komarev.com/ghpvc/?username=SathishkumarSivakumar&label=PROFILE%20VIEWS&color=070b10&style=for-the-badge" alt="Profile views" />
<img src="https://img.shields.io/github/followers/SathishkumarSivakumar?label=FOLLOWERS&style=for-the-badge&color=070b10&labelColor=070b10" alt="Followers" />

<br/><br/>

<!-- quick nav -->
<sub>
<a href="#01-nbspprofile">Profile</a> ·
<a href="#02-nbsptech-stack">Tech Stack</a> ·
<a href="#04-nbspfeatured-projects">Projects</a> ·
<a href="#05-nbspexperience--education">Experience</a> ·
<a href="#06-nbspgithub-analytics">GitHub Analytics</a> ·
<a href="#09-nbspquick-facts">Quick Facts</a> ·
<a href="#10-nbsplets-connect">Contact</a>
</sub>

</div>

<img src="./assets/stats-strip.svg" width="100%" alt="Impact at a glance — 2+ projects, 2 internships, 2 certifications, 8.3 CGPA" />

<img src="./assets/divider.svg" width="100%" alt="" />

## `01` &nbsp;Profile

<table>
<tr>
<td width="56%" valign="top">

I'm a **Data Science & AI Engineer** who enjoys the full journey of a
dataset — from a messy CSV all the way to a clean, decision-ready
dashboard or a working ML model.

**What I actually do**

- Design and query relational schemas in **MySQL** — joins, views, stored procedures, triggers, indexing
- Clean, transform and explore data with **Pandas · NumPy**
- Build and evaluate models with **Scikit-learn** — regression, classification, clustering
- Apply **NLP** — text cleaning, TF-IDF / Count Vectorizer, sentiment classification
- Ship decision-ready reporting in **Power BI** and **Excel**
- Translate model output into a narrative a non-technical stakeholder can act on

**How I work**

> Understand the question before touching the data.
> A simple model shipped beats a complex model half-explained.
> Every chart on a dashboard should answer something someone actually asked.

</td>
<td width="44%" valign="top">

```python
class SathishkumarS:
    role     = "Data Science & AI Engineer"
    location = "Chennai, India"
    stack    = ["Python", "SQL", "Power BI"]
    ml       = ["Scikit-learn", "NLP", "Pandas"]
    cgpa     = 8.3   # B.E, EEE

    def pipeline(self, raw_data):
        clean    = self.validate(raw_data)
        features = self.engineer(clean)
        model    = self.train(features)
        return self.explain(model)

    def open_to(self):
        return [
            "Data Science",
            "Data Analytics",
            "AI / ML Engineering",
            "BI Development",
        ]

me = SathishkumarS()
print(me.pipeline(raw_data="chaos"))
# >> "a dashboard someone opens every morning"
```

</td>
</tr>
</table>

<img src="./assets/divider.svg" width="100%" alt="" />

## `02` &nbsp;Tech Stack

<div align="center">

**Languages &amp; Database**

<img src="https://skillicons.dev/icons?i=python,mysql,vscode,git,github,anaconda&theme=dark" alt="Languages & tools" />

<br/><br/>

**Data · ML · NLP**

<img src="https://img.shields.io/badge/-Pandas-070b10?style=for-the-badge&logo=pandas&logoColor=150458" alt="Pandas" />
<img src="https://img.shields.io/badge/-NumPy-070b10?style=for-the-badge&logo=numpy&logoColor=4DABCF" alt="NumPy" />
<img src="https://img.shields.io/badge/-scikit--learn-070b10?style=for-the-badge&logo=scikitlearn&logoColor=F7931E" alt="Scikit-learn" />
<img src="https://img.shields.io/badge/-Jupyter-070b10?style=for-the-badge&logo=jupyter&logoColor=F37626" alt="Jupyter" />
<img src="https://img.shields.io/badge/-NLTK%20%2F%20NLP-070b10?style=for-the-badge&logo=python&logoColor=5fe3c8" alt="NLP" />

<br/>

**Visualisation &amp; BI**

<img src="https://img.shields.io/badge/-Power%20BI-070b10?style=for-the-badge&logo=powerbi&logoColor=F2C811" alt="Power BI" />
<img src="https://img.shields.io/badge/-DAX-070b10?style=for-the-badge&logo=microsoft&logoColor=f2a154" alt="DAX" />
<img src="https://img.shields.io/badge/-Excel-070b10?style=for-the-badge&logo=microsoftexcel&logoColor=217346" alt="Excel" />
<img src="https://img.shields.io/badge/-Matplotlib-070b10?style=for-the-badge&logo=plotly&logoColor=e9eef2" alt="Matplotlib" />

</div>

<br/>

| Layer | Tools | Confidence |
| :-- | :-- | :-- |
| Data acquisition &amp; storage | MySQL · joins · views · stored procedures · triggers | `████████░░` Strong |
| Wrangling &amp; EDA | Pandas · NumPy · Jupyter Notebook | `█████████░` Strong |
| Modelling | Scikit-learn · regression · classification · clustering | `████████░░` Strong |
| NLP | Text cleaning · TF-IDF · Count Vectorizer · sentiment models | `███████░░░` Working |
| Reporting &amp; BI | Power BI · DAX · Power Query · Excel | `███████░░░` Working |
| Version control | Git · GitHub · VS Code | `████████░░` Strong |

<div align="center">
<br/>
<img src="./assets/skills-radar.svg" width="440" alt="Skill proficiency radar — Python, SQL, Machine Learning, NLP, Power BI, Database Design" />
</div>

<div align="right"><sub><a href="#top">↑ back to top</a></sub></div>

<img src="./assets/divider.svg" width="100%" alt="" />

## `03` &nbsp;How a Project Moves Through My Hands

```text
   RAW SOURCES          CLEAN & EXPLORE         MODEL / QUERY          DELIVER
  ┌─────────────┐      ┌────────────────┐      ┌───────────────┐     ┌───────────────┐
  │  SQL / CSV  │  ──▶ │  Validate      │  ──▶ │  Feature eng   │ ──▶ │  Power BI      │
  │  Excel      │      │  Handle nulls  │      │  Train / tune  │     │  dashboard     │
  │  Raw text   │      │  EDA + charts  │      │  Evaluate      │     │  or SQL schema │
  └─────────────┘      └────────────────┘      └───────────────┘     └───────────────┘
         │                      │                      │                     │
         └──────────────── versioned in Git · documented in notebooks ───────┘
```

<img src="./assets/divider.svg" width="100%" alt="" />

## `04` &nbsp;Featured Projects

<table>
<tr>
<td width="50%" valign="top">

### 🏥 Apollocare Hospital Management System
Full relational database for a hospital — patients, doctors,
appointments, billing, pharmacy and medical records — built with
joins, subqueries, views, stored procedures and triggers, with
indexing for query performance.

`MySQL` `Database Design` `Stored Procedures` `Triggers`

[**View on GitHub →**](https://github.com/SathishkumarSivakumar/ApolloCare-Hospital-Management-System)

</td>
<td width="50%" valign="top">

### 🛒 Amazon User Review Analysis — NLP
NLP-based sentiment analysis on Amazon reviews: text cleaning,
tokenization and feature extraction with TF-IDF and Count
Vectorizer, then classification with Scikit-learn.

`Python` `NLP` `TF-IDF` `Scikit-learn`

[**View on GitHub →**](https://github.com/SathishkumarSivakumar/Project-Amazon-NLP-)

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🦟 AI-Enhanced Herbal Mosquito Repellent Kit
Final-year project — a Python-based detection system that
identifies when a mosquito enters the room and automatically
activates an herbal repellent kit, switching off once it's gone.

`Python` `Machine Learning` `Automation`

*Hardware-integrated project — repo private*

</td>
<td width="50%" valign="top">

### 📌 More on the way
Currently building out additional end-to-end ML and BI projects —
this space fills in as each one ships.

`In progress`

[**See all repos →**](https://github.com/SathishkumarSivakumar?tab=repositories)

</td>
</tr>
</table>

<div align="right"><sub><a href="#top">↑ back to top</a></sub></div>

<img src="./assets/divider.svg" width="100%" alt="" />

## `05` &nbsp;Experience &amp; Education

<table>
<tr>
<td width="50%" valign="top">

**SQL Developer Intern** — Besant Technology
`Jan – Mar 2024`
Developed and optimized SQL queries and database objects in
MySQL — joins, views, stored procedures, functions, triggers and
indexes — focused on query performance.

**Data Science Intern** — Coapps.ai
`May 2024`
Completed a Data Science internship covering the full lifecycle
from EDA to model building, with a satisfactory performance record.

</td>
<td width="50%" valign="top">

**B.E., Electrical &amp; Electronics Engineering**
Kongunadu College of Engineering and Technology
`CGPA: 8.3`

**Certifications**
- Data Science — Coapps *(May 2024)*
- SQL (Basic / Intermediate) — HackerRank

</td>
</tr>
</table>

<div align="right"><sub><a href="#top">↑ back to top</a></sub></div>

<img src="./assets/divider.svg" width="100%" alt="" />

## `06` &nbsp;GitHub Analytics

<div align="center">

<img height="168" src="https://github-readme-stats.vercel.app/api?username=SathishkumarSivakumar&show_icons=true&hide_border=true&bg_color=070b10&title_color=5fe3c8&icon_color=f2a154&text_color=e9eef2&border_color=1b2530&count_private=true" alt="GitHub stats" />
<img height="168" src="https://streak-stats.demolab.com?user=SathishkumarSivakumar&hide_border=true&background=070b10&ring=5fe3c8&fire=f2a154&currStreakLabel=5fe3c8&sideLabels=e9eef2&currStreakNum=e9eef2&sideNums=e9eef2&dates=8ea0ac" alt="Streak stats" />

<img height="168" src="https://github-readme-stats.vercel.app/api/top-langs/?username=SathishkumarSivakumar&layout=compact&hide_border=true&bg_color=070b10&title_color=5fe3c8&text_color=e9eef2&border_color=1b2530" alt="Top languages" />

<br/>

<img width="98%" src="https://github-readme-activity-graph.vercel.app/graph?username=SathishkumarSivakumar&bg_color=070b10&color=5fe3c8&line=5fe3c8&point=f2a154&area=true&hide_border=true" alt="Contribution activity graph" />

<br/>

<img width="90%" src="https://github-profile-trophy.vercel.app/?username=SathishkumarSivakumar&no-frame=true&no-bg=true&margin-w=6&margin-h=6&column=7&theme=darkhub" alt="GitHub trophies" />

<br/>

<img width="98%" src="https://raw.githubusercontent.com/SathishkumarSivakumar/SathishkumarSivakumar/output/github-contribution-grid-snake-dark.svg" alt="Contribution snake" />
<sub>↑ animates once you add <code>.github/workflows/snake.yml</code> — see setup note below</sub>

</div>

<img src="./assets/divider.svg" width="100%" alt="" />

## `07` &nbsp;Currently Sharpening

```text
Deep Learning     ███████░░░░░░░░  45%   TensorFlow · Keras · CNN / RNN foundations
Advanced SQL      █████████░░░░░░  62%   Window functions · query tuning
MLOps basics      █████░░░░░░░░░░  32%   Docker · experiment tracking
LLM applications  ██████░░░░░░░░░  38%   Prompting · embeddings · RAG
```

<div align="right"><sub><a href="#top">↑ back to top</a></sub></div>

<img src="./assets/divider.svg" width="100%" alt="" />

## `08` &nbsp;Timeline

<table>
<tr><td width="14%" align="center"><b>2024</b></td><td width="86%">🎓 Graduated B.E. Electrical &amp; Electronics Engineering — CGPA 8.3, Kongunadu College of Engineering and Technology</td></tr>
<tr><td align="center"><b>Jan '24</b></td><td>🗄️ Started SQL Developer Internship at Besant Technology — joins, views, stored procedures, triggers</td></tr>
<tr><td align="center"><b>May '24</b></td><td>🧠 Data Science Internship at Coapps.ai + Data Science certification</td></tr>
<tr><td align="center"><b>2024</b></td><td>🏥 Built Apollocare Hospital Management System — full relational DB design</td></tr>
<tr><td align="center"><b>2024</b></td><td>🛒 Shipped Amazon Review NLP sentiment classifier (TF-IDF + Scikit-learn)</td></tr>
<tr><td align="center"><b>2024</b></td><td>🦟 Final-year project — AI-Enhanced Herbal Mosquito Repellent Kit</td></tr>
<tr><td align="center"><b>Now</b></td><td>📈 Deepening Deep Learning, MLOps basics and LLM application skills — open to full-time roles</td></tr>
</table>

<div align="right"><sub><a href="#top">↑ back to top</a></sub></div>

<img src="./assets/divider.svg" width="100%" alt="" />

## `09` &nbsp;Quick Facts

<div align="center">

| | |
|---|---|
| 🦟 | Built an AI system whose entire job is detecting mosquitoes and firing back with herbal repellent |
| 🗄️ | Thinks in `JOIN`s before breakfast — SQL is where the DS journey actually started |
| 📊 | Believes a dashboard has failed if someone has to ask "so what does this mean?" |
| ☕ | Cleaner code, and cleaner data, after coffee #2 |
| 🎯 | 8.3 CGPA in Electrical & Electronics Engineering — proof that a non-CS background is not a blocker |
| 🌱 | Currently teaching myself Deep Learning and MLOps, one broken Docker container at a time |

</div>

<div align="right"><sub><a href="#top">↑ back to top</a></sub></div>

<img src="./assets/divider.svg" width="100%" alt="" />

## `10` &nbsp;Let's Connect

<div align="center">

I'm open to **Data Science, Analytics, and AI Engineering** roles —
full-time, Chennai or remote. Always happy to talk data.

<a href="mailto:kumar109662@gmail.com"><img src="https://img.shields.io/badge/Email%20me-5fe3c8?style=for-the-badge&labelColor=070b10&logo=gmail&logoColor=5fe3c8" alt="Email me" /></a>
<a href="https://www.linkedin.com/in/sathishkumar-sivakumar/"><img src="https://img.shields.io/badge/Connect%20on%20LinkedIn-5fe3c8?style=for-the-badge&labelColor=070b10&logo=linkedin&logoColor=5fe3c8" alt="LinkedIn" /></a>
<a href="https://github.com/SathishkumarSivakumar?tab=repositories"><img src="https://img.shields.io/badge/Browse%20Repos-5fe3c8?style=for-the-badge&labelColor=070b10&logo=github&logoColor=5fe3c8" alt="Repos" /></a>
<a href="https://sathishkumar-sivakumar.netlify.app"><img src="https://img.shields.io/badge/View%20Portfolio-f2a154?style=for-the-badge&labelColor=070b10&logo=vercel&logoColor=f2a154" alt="Portfolio" /></a>

<br/><br/>

> ### "Turning data into insights, and insights into impact."

<br/>

<sub><a href="#top">↑ back to top</a></sub>

</div>

<img src="./assets/footer.svg" width="100%" alt="" />
[profile-readme (1).zip](https://github.com/user-attachments/files/31449157/profile-readme.1.zip)
