# GitHub Profile README Redesign — Implementation Plan

> **For agentic workers:** REQUIRED: Use superpowers:subagent-driven-development (if subagents available) or superpowers:executing-plans to implement this plan. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Rewrite `README.md` in `minkhoaa/minkhoaa` with a hybrid terminal-header + resume-body design using dark monochrome theme, shields.io badges, pin cards, stats widgets, and activity graph.

**Architecture:** Single-file implementation (`README.md`). Pure Markdown + inline HTML. All visual elements come from external services (shields.io, github-readme-stats, streak-stats, activity-graph). No build step, no CI, no generated files.

**Tech Stack:** Markdown, HTML tables, shields.io, github-readme-stats, streak-stats.demolab.com, github-readme-activity-graph

**Spec:** `docs/superpowers/specs/2026-03-12-github-profile-redesign-design.md`

---

## Chunk 1: Build and verify README

### Task 1: Verify external service URLs

Before writing any content, verify that all external services return valid responses.

**Files:** None (verification only)

- [ ] **Step 1: Verify Typing SVG service**

```bash
curl -s -o /dev/null -w "%{http_code}" "https://readme-typing-svg.demolab.com/?lines=Building+scalable+distributed+systems&font=Fira+Code&center=true&width=440&height=45&color=c9d1d9&vCenter=true&pause=1000&size=22"
```

Expected: `200`

- [ ] **Step 2: Verify shields.io C# badge slug**

```bash
curl -s -o /dev/null -w "%{http_code}" "https://img.shields.io/badge/C%23-1F222E?style=for-the-badge&logo=csharp&logoColor=white"
```

Expected: `200`. If not 200, use fallback: `logo=dotnet` with label `C%23`.

- [ ] **Step 3: Verify streak-stats URL**

```bash
curl -s -o /dev/null -w "%{http_code}" "https://streak-stats.demolab.com/?user=minkhoaa&theme=dark&hide_border=true"
```

Expected: `200`

- [ ] **Step 4: Verify activity graph URL**

```bash
curl -s -o /dev/null -w "%{http_code}" "https://github-readme-activity-graph.vercel.app/graph/?username=minkhoaa&bg_color=0d1117&color=8b949e&line=58a6ff&point=ffffff&hide_border=true"
```

Expected: `200`

- [ ] **Step 5: Verify github-readme-stats pin card URL**

```bash
curl -s -o /dev/null -w "%{http_code}" "https://github-readme-stats.vercel.app/api/pin/?username=minkhoaa&repo=Project_Langfens_Microservice&theme=dark&bg_color=0d1117&hide_border=true&title_color=58a6ff&icon_color=8b949e&text_color=8b949e"
```

Expected: `200`

---

### Task 2: Write the complete README.md

**Files:**
- Modify: `README.md` (complete rewrite)

- [ ] **Step 1: Write the README**

Replace the entire contents of `README.md` with:

```markdown
<p align="center">
  <img src="https://readme-typing-svg.demolab.com/?lines=Building+scalable+distributed+systems&font=Fira+Code&center=true&width=500&height=45&color=c9d1d9&vCenter=true&pause=1000&size=22" alt="Typing SVG" />
</p>

<p align="center">
  <code>khoa@archlinux</code> · .NET Backend Developer · Ho Chi Minh City
</p>

---

<h3 align="center">Languages & Frameworks</h3>

<p align="center">
  <img src="https://img.shields.io/badge/C%23-1F222E?style=for-the-badge&logo=csharp&logoColor=white" alt="C#" />
  <img src="https://img.shields.io/badge/.NET-1F222E?style=for-the-badge&logo=dotnet&logoColor=white" alt=".NET" />
  <img src="https://img.shields.io/badge/TypeScript-1F222E?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/NestJS-1F222E?style=for-the-badge&logo=nestjs&logoColor=white" alt="NestJS" />
  <img src="https://img.shields.io/badge/Java-1F222E?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java" />
</p>

<h3 align="center">Infrastructure</h3>

<p align="center">
  <img src="https://img.shields.io/badge/PostgreSQL-1F222E?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Redis-1F222E?style=for-the-badge&logo=redis&logoColor=white" alt="Redis" />
  <img src="https://img.shields.io/badge/RabbitMQ-1F222E?style=for-the-badge&logo=rabbitmq&logoColor=white" alt="RabbitMQ" />
  <img src="https://img.shields.io/badge/Elasticsearch-1F222E?style=for-the-badge&logo=elasticsearch&logoColor=white" alt="Elasticsearch" />
  <img src="https://img.shields.io/badge/Docker-1F222E?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
</p>

<h3 align="center">Environment</h3>

<p align="center">
  <img src="https://img.shields.io/badge/Arch_Linux-1F222E?style=for-the-badge&logo=archlinux&logoColor=white" alt="Arch Linux" />
  <img src="https://img.shields.io/badge/Niri-1F222E?style=for-the-badge" alt="Niri" />
  <img src="https://img.shields.io/badge/Fish-1F222E?style=for-the-badge" alt="Fish" />
  <img src="https://img.shields.io/badge/Kitty-1F222E?style=for-the-badge" alt="Kitty" />
</p>

---

### Featured Projects

<table>
  <tr>
    <td width="50%">
      <a href="https://github.com/minkhoaa/Project_Langfens_Microservice">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=minkhoaa&repo=Project_Langfens_Microservice&theme=dark&bg_color=0d1117&hide_border=true&title_color=58a6ff&icon_color=8b949e&text_color=8b949e" alt="Langfens" />
      </a>
    </td>
    <td width="50%">
      <a href="https://github.com/minkhoaa/peerzee-fullstack">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=minkhoaa&repo=peerzee-fullstack&theme=dark&bg_color=0d1117&hide_border=true&title_color=58a6ff&icon_color=8b949e&text_color=8b949e" alt="Peerzee" />
      </a>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <a href="https://github.com/minkhoaa/Foodify-Social-Media-Backend">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=minkhoaa&repo=Foodify-Social-Media-Backend&theme=dark&bg_color=0d1117&hide_border=true&title_color=58a6ff&icon_color=8b949e&text_color=8b949e" alt="Foodify" />
      </a>
    </td>
    <td width="50%"></td>
  </tr>
</table>

### Other Projects

<table>
  <tr>
    <td width="33%">
      <a href="https://github.com/minkhoaa/Clinic_Management_API">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=minkhoaa&repo=Clinic_Management_API&theme=dark&bg_color=0d1117&hide_border=true&title_color=58a6ff&icon_color=8b949e&text_color=8b949e" alt="Clinic Management" />
      </a>
    </td>
    <td width="33%">
      <a href="https://github.com/minkhoaa/EnglishApp-Backend">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=minkhoaa&repo=EnglishApp-Backend&theme=dark&bg_color=0d1117&hide_border=true&title_color=58a6ff&icon_color=8b949e&text_color=8b949e" alt="EnglishApp" />
      </a>
    </td>
    <td width="33%">
      <a href="https://github.com/minkhoaa/porfolio">
        <img src="https://github-readme-stats.vercel.app/api/pin/?username=minkhoaa&repo=porfolio&theme=dark&bg_color=0d1117&hide_border=true&title_color=58a6ff&icon_color=8b949e&text_color=8b949e" alt="Portfolio" />
      </a>
    </td>
  </tr>
</table>

---

### GitHub Stats

<table>
  <tr>
    <td width="50%">
      <img src="https://github-readme-stats.vercel.app/api?username=minkhoaa&show_icons=true&bg_color=0d1117&hide_border=true&title_color=58a6ff&text_color=8b949e&icon_color=8b949e" alt="GitHub Stats" />
    </td>
    <td width="50%">
      <img src="https://streak-stats.demolab.com/?user=minkhoaa&theme=dark&hide_border=true&background=0d1117&ring=58a6ff&fire=58a6ff&currStreakNum=c9d1d9&sideNums=8b949e&dates=484f58&currStreakLabel=8b949e&sideLabels=8b949e" alt="GitHub Streak" />
    </td>
  </tr>
</table>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph/?username=minkhoaa&bg_color=0d1117&color=8b949e&line=58a6ff&point=ffffff&hide_border=true" alt="Activity Graph" />
</p>

---

<p align="center">
  <a href="https://linkedin.com/in/min-khoaa">
    <img src="https://img.shields.io/badge/LinkedIn-1F222E?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="https://facebook.com/min.khoaaa">
    <img src="https://img.shields.io/badge/Facebook-1F222E?style=for-the-badge&logo=facebook&logoColor=white" alt="Facebook" />
  </a>
  <a href="mailto:your@email.com">
    <img src="https://img.shields.io/badge/Email-1F222E?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
</p>
```

Note: Replace `mailto:your@email.com` with the real email address if provided by the owner.

- [ ] **Step 2: Commit the rewritten README**

```bash
git add README.md
git commit -m "Redesign profile README with dark monochrome theme

Hybrid terminal header + resume body approach:
- Typing SVG animation header with Fira Code font
- shields.io badges (for-the-badge, dark monochrome) for tech stack
- github-readme-stats pin cards for featured + other projects
- Stats card, streak card, and activity graph
- Contact badges for LinkedIn, Facebook, Email"
```

---

### Task 3: Push and verify on GitHub

- [ ] **Step 1: Push to remote**

```bash
git push origin main
```

- [ ] **Step 2: Verify profile renders correctly**

Open `https://github.com/minkhoaa` in a browser and verify:
1. Typing SVG animates correctly
2. All shields.io badges render with dark background and white logos
3. Pin cards show correct repo info
4. Stats card, streak card, and activity graph render with matching dark theme
5. Contact badges link to correct URLs
6. No broken images or layout issues

- [ ] **Step 3: If any badge/widget is broken, fix the URL and push again**

Common fixes:
- C# badge: change `logo=csharp` to `logo=dotnet` with label `C%23`
- Activity graph: if Vercel deployment is down, remove the activity graph section
- Streak stats: verify `streak-stats.demolab.com` is reachable
