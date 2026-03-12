# GitHub Profile README Redesign

## Goal

Redesign the `minkhoaa/minkhoaa` profile README to be visually impressive, professional, and recruiter-attractive. Target audience: all types of recruiters (startups, enterprise, freelance). Balance technical depth, project showcase, and personal brand equally.

## Design Direction

**Hybrid: Terminal header + Resume body.** Terminal aesthetic in the header to express Linux developer identity, structured resume-style body for scannability by both HR and technical leads. Dark monochrome theme throughout. No emojis, no flashy/unprofessional icons.

## Sections

### 1. Header

- **Typing SVG** from `readme-typing-svg.demolab.com`
  - Text: `Building scalable distributed systems`
  - Font: Fira Code
  - Colors: monochrome (white/gray on transparent)
  - Centered, with cursor animation
- **Identity line** below the typing SVG:
  - Format: `khoa@archlinux · .NET Backend Developer · Ho Chi Minh City`
  - Plain text, centered, subtle gray

### 2. Tech Stack

shields.io badges using `style=for-the-badge` with dark monochrome colors (`color=1F222E`, `logoColor=white`). Grouped into 3 categories, each with a subtle uppercase label:

**Languages & Frameworks:**
- C# (logo: csharp)
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
- Niri (no standard logo, text-only badge)
- Fish (no standard logo, text-only badge)
- Kitty (no standard logo, text-only badge)

### 3. Featured Projects

Use `github-readme-stats` pin cards (`/api/pin/?username=minkhoaa&repo=REPO`). Dark theme matching the overall palette (`theme=dark`, `bg_color=0d1117`, `hide_border=true`, `title_color=58a6ff`, `icon_color=8b949e`, `text_color=8b949e`).

**Featured (2-column layout using HTML table):**

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

Three widgets, all with matching dark theme (`bg_color=0d1117`, `hide_border=true`, `title_color=58a6ff`, `text_color=8b949e`, `icon_color=8b949e`):

- **Stats card** + **Streak card** side-by-side (HTML table, 2 columns)
  - Stats: `github-readme-stats.vercel.app/api?username=minkhoaa`
  - Streak: `github-readme-streak-stats.herokuapp.com/?user=minkhoaa`
- **Activity Graph** full-width below
  - `github-readme-activity-graph.vercel.app/graph/?username=minkhoaa`
  - Colors: `bg_color=0d1117`, `color=8b949e`, `line=58a6ff`, `point=ffffff`

### 5. Contact

shields.io badges (`style=for-the-badge`, dark monochrome) centered:

- LinkedIn: links to `https://linkedin.com/in/min-khoaa`
- Facebook: links to `https://facebook.com/min.khoaaa`
- Email: placeholder `mailto:your@email.com`

## Color Palette

| Element | Color | Usage |
|---------|-------|-------|
| Background | `#0d1117` | All widget bg_color |
| Title/accent | `#58a6ff` | Repo names, headings in stats |
| Primary text | `#c9d1d9` | Badge text, main content |
| Secondary text | `#8b949e` | Descriptions, subtitles |
| Muted | `#484f58` | Section labels, dividers |
| Surface | `#1F222E` | Badge backgrounds |
| Border | `#21262d` | Card borders (in widgets) |
| Terminal green | `#7ee787` | Username in identity line |
| Terminal blue | `#79c0ff` | Hostname in identity line |

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
