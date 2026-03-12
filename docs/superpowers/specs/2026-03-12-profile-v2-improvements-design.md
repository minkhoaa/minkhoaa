# GitHub Profile README v2 Improvements

## Goal

Iterate on the existing profile README: replace "Environment" with DevOps/Cloud skills, upgrade featured projects from pin cards to custom HTML cards with tech badges, add multi-line typing SVG, and add "Currently Exploring" section.

## Changes

### 1. Typing SVG — multi-line rotation

Replace single static line with 3 rotating lines:
- `Building scalable distributed systems`
- `Microservices · Event-Driven · Cloud-Native`
- `C# · .NET · Docker · Azure`

URL format: `readme-typing-svg.demolab.com/?lines=Line1;Line2;Line3`
Semicolons separate lines. Spaces encoded as `+`.

### 2. "Environment" → "DevOps & Cloud"

Remove: Arch Linux, Niri, Fish, Kitty badges.

Add (same `for-the-badge` style, `color=1F222E`, `logoColor=white`):
- Nginx (logo: nginx)
- GitHub Actions (logo: githubactions)
- Azure (logo: microsoftazure)
- Google Cloud (logo: googlecloud)
- DigitalOcean (logo: digitalocean)

Rationale: `khoa@archlinux` in header already signals Linux identity. Niri/Fish/Kitty are personal preferences, not professional skills.

### 3. Featured Projects — custom HTML cards

Replace `github-readme-stats` pin cards with custom HTML table. Each project gets:
- Project name as link (bold)
- 1-2 line description highlighting architecture and what it solves
- Small `flat` style tech badges (monochrome, `color=21262d`, `logoColor=8b949e`) showing key technologies

**Langfens — AI-powered IELTS Platform**
- Description: 13 microservices, event-driven architecture, AI-powered grading and speech analysis
- Tech: .NET 8, PostgreSQL, RabbitMQ, Redis, Elasticsearch, GPT-4o, Whisper

**Peerzee — Full-stack Web Application**
- Description: Microservices architecture with speech processing, containerized deployment
- Tech: Next.js, NestJS, Whisper, Docker, Playwright

**Foodify — Social Media Backend**
- Description: Food-sharing social platform with auth, feed, social features, image CDN
- Tech: .NET 8, PostgreSQL, Redis, Cloudinary, JWT

Card layout: full-width rows (1 project per row), not 2-column grid. This gives more space for description and tech badges.

### 4. "Currently Exploring" section

New section between Tech Stack and Featured Projects. Centered, same badge style but `flat` style instead of `for-the-badge` to visually differentiate from core skills.

Badges:
- RAG (text-only, `flat`, `color=21262d`)
- LangChain (logo: langchain, `flat`, `color=21262d`)

### 5. Other Projects — keep as pin cards

No change to the Other Projects section. Pin cards are appropriate for secondary projects.

## Unchanged sections

- Header (typing SVG update only, identity line stays)
- Languages & Frameworks badges
- Infrastructure badges
- GitHub Stats (stats + streak + activity graph)
- Contact badges
- Other Projects section

## Color palette

Same as v1 — no color changes. All new badges use `1F222E` (for-the-badge) or `21262d` (flat) backgrounds with white/`8b949e` logo colors.
