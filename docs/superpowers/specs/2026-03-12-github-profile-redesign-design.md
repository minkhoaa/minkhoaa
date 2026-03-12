# GitHub Profile README Redesign

## Goal

Redesign the `minkhoaa/minkhoaa` profile README to be visually impressive, professional, and recruiter-attractive. Target audience: all types of recruiters (startups, enterprise, freelance). Balance technical depth, project showcase, and personal brand equally.

## Design Direction

**Hybrid: Terminal header + Resume body.** Terminal aesthetic in the header to express Linux developer identity, structured resume-style body for scannability by both HR and technical leads. Dark monochrome theme throughout. No emojis, no flashy/unprofessional icons.

## Sections

### 1. Header

- **Typing SVG** from `readme-typing-svg.demolab.com`
  - Text: `Building scalable distributed systems`
  - Font: Fira Code (fallback: JetBrains Mono, Source Code Pro)
  - Colors: monochrome (white/gray on transparent)
  - Centered, with cursor animation
- **Identity line** below the typing SVG:
  - Format: `khoa@archlinux · .NET Backend Developer · Ho Chi Minh City`
  - Rendered as plain centered text in gray (`#8b949e`). The terminal green/blue coloring from the color palette is NOT used here because GitHub Markdown does not support inline `style` color attributes. The identity line is uniformly gray.
- **Section dividers**: use standard Markdown horizontal rules (`---`) between all major sections.

### 2. Tech Stack

shields.io badges using `style=for-the-badge` with dark monochrome colors (`color=1F222E`, `logoColor=white`). Grouped into 3 categories, each with a centered bold label.

Note on URL format: color values in URL parameters omit the `#` prefix (e.g., `color=1F222E`, not `color=#1F222E`).

**Languages & Frameworks:**
- C# (logo: csharp — verify slug works, fallback: use `logo=dotnet` with label `C%23`)
- .NET (logo: dotnet)
- TypeScript (logo: typescript)
- NestJS (logo: nestjs)
- Java (logo: openjdk)

**Infrastructure:**
- PostgreSQL (logo: postgresql)
- Redis (logo: redis)
- RabbitMQ (logo: rabbitmq)
- Elasticsearch (logo: elasticsearch)
- Docker (logo: docker)

**Environment:**
- Arch Linux (logo: archlinux)
- Niri (text-only badge: `https://img.shields.io/badge/Niri-1F222E?style=for-the-badge`)
- Fish (text-only badge: `https://img.shields.io/badge/Fish-1F222E?style=for-the-badge`)
- Kitty (text-only badge: `https://img.shields.io/badge/Kitty-1F222E?style=for-the-badge`)

### 3. Featured Projects

Use `github-readme-stats` pin cards (`/api/pin/?username=minkhoaa&repo=REPO`). Dark theme matching the overall palette (`theme=dark`, `bg_color=0d1117`, `hide_border=true`, `title_color=58a6ff`, `icon_color=8b949e`, `text_color=8b949e`).

**Featured (2-column layout using HTML table, 3 projects = 2 rows, last row has 1 card left-aligned):**

| Project | Description |
|---------|-------------|
| Project_Langfens_Microservice | AI-powered IELTS learning platform. 13 microservices, event-driven architecture with RabbitMQ, AI grading (GPT-4o), Whisper STT. .NET 8, PostgreSQL, Redis, Elasticsearch. |
| peerzee-fullstack | Full-stack web app with microservices. Next.js frontend, NestJS backend, Whisper service. Docker containerized, Playwright tested. |
| Foodify-Social-Media-Backend | Social media backend for food sharing. .NET 8, JWT auth + OTP, PostgreSQL, Redis, Cloudinary. Repository pattern, service layer. |

**Other Projects (smaller pin cards, 3-column layout):**

| Project | Description |
|---------|-------------|
| Clinic_Management_API | Clinical management system (C#) |
| EnglishApp-Backend | Language learning backend (C#) |
| porfolio | Personal portfolio site (TypeScript) |

### 4. GitHub Stats

Three widgets, all with matching dark theme:

- **Stats card** + **Streak card** side-by-side (HTML table, 2 columns, each `<td>` with `width="50%"`)
  - Stats: `github-readme-stats.vercel.app/api?username=minkhoaa&show_icons=true&bg_color=0d1117&hide_border=true&title_color=58a6ff&text_color=8b949e&icon_color=8b949e`
  - Streak: `streak-stats.demolab.com/?user=minkhoaa&theme=dark&hide_border=true&background=0d1117&ring=58a6ff&fire=58a6ff&currStreakNum=c9d1d9&sideNums=8b949e&dates=484f58&currStreakLabel=8b949e&sideLabels=8b949e`
- **Activity Graph** full-width below
  - `github-readme-activity-graph.vercel.app/graph/?username=minkhoaa&bg_color=0d1117&color=8b949e&line=58a6ff&point=ffffff&hide_border=true`
  - Note: this Vercel deployment may become unreliable. If it breaks, consider self-hosting or removing this widget.

### 5. Contact

shields.io badges (`style=for-the-badge`, dark monochrome) centered:

- LinkedIn: links to `https://linkedin.com/in/min-khoaa`
- Facebook: links to `https://facebook.com/min.khoaaa`
- Email: TBD — ask owner for real email before implementation. Use placeholder `mailto:your@email.com` if not provided.

## Color Palette

All color values omit the `#` prefix when used in URL parameters.

| Element | Color | Usage |
|---------|-------|-------|
| Background | `#0d1117` | All widget bg_color |
| Title/accent | `#58a6ff` | Repo names, headings in stats |
| Primary text | `#c9d1d9` | Badge text, main content |
| Secondary text | `#8b949e` | Descriptions, subtitles, identity line |
| Muted | `#484f58` | Section labels, date text in streak |
| Surface | `#1F222E` | Badge backgrounds |
| Border | `#21262d` | Card borders (in widgets) |

## GitHub Markdown Rendering Notes

- Inline `style` attributes with `color` do NOT work on GitHub — text colors cannot be customized in Markdown.
- Custom `<hr>` styling does not work — use standard `---` for dividers.
- HTML tables work for layout (2-column, 3-column) but are not responsive on mobile — narrow viewports will still scroll horizontally, which is acceptable.
- `<p align="center">` works for centering content.

## Constraints

- No emojis anywhere in the README
- No bright/rainbow colors — monochrome dark palette only
- No flashy GIFs or animated images
- Only animation: Typing SVG (text-only, subtle)
- All widgets must use consistent dark theme
- Profile must look good in both GitHub dark and light mode (transparent backgrounds where possible, fallback to `#0d1117` for widgets)
- Pure Markdown + HTML — no external dependencies beyond shields.io, github-readme-stats, streak-stats, and activity-graph

## Out of Scope

- WakaTime integration (requires setup)
- Snake contribution animation (requires GitHub Action setup)
- Custom banner image (would need design tools)
- Profile view counter
- Top Languages card (deliberately removed — tech stack is shown via badges instead)
