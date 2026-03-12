# GitHub Profile README v2 Improvements

## Goal

Iterate on the existing profile README: replace "Environment" with DevOps/Cloud skills, upgrade featured projects from pin cards to custom HTML cards with tech badges, add multi-line typing SVG, and add "Currently Exploring" section.

## Changes

### 1. Typing SVG — multi-line rotation

Replace single static line with 3 rotating lines:
- `Building scalable distributed systems`
- `Microservices · Event-Driven · Cloud-Native`
- `C# · .NET · Docker · Azure`

Only the `lines` parameter changes. All existing parameters remain: `font=Fira+Code`, `center=true`, `width=500`, `height=45`, `color=c9d1d9`, `vCenter=true`, `pause=1000`, `size=22`.

Full URL:
```
https://readme-typing-svg.demolab.com/?lines=Building+scalable+distributed+systems;Microservices+·+Event-Driven+·+Cloud-Native;C%23+·+.NET+·+Docker+·+Azure&font=Fira+Code&center=true&width=500&height=45&color=c9d1d9&vCenter=true&pause=1000&size=22
```

### 2. "Environment" → "DevOps & Cloud"

Remove: Arch Linux, Niri, Fish, Kitty badges.
Replace heading: `<h3 align="center">DevOps & Cloud</h3>`

Add (same `for-the-badge` style, `color=1F222E`, `logoColor=white`):
- Nginx (logo: `nginx`) — HAS LOGO
- GitHub Actions (logo: `githubactions`) — verify at implementation
- Azure (text-only, no working logo slug on shields.io)
- Google Cloud (logo: `googlecloud`) — verify at implementation
- DigitalOcean (logo: `digitalocean`) — verify at implementation

Rationale: `khoa@archlinux` in header already signals Linux identity. Niri/Fish/Kitty are personal preferences, not professional skills.

### 3. Featured Projects — custom HTML cards

Replace `github-readme-stats` pin cards with custom HTML table. Each project card is a full-width table row.

**HTML structure per card:**
```html
<table>
  <tr>
    <td>
      <h4><a href="https://github.com/minkhoaa/{repo-name}">Project Name</a></h4>
      <p>1-2 line description</p>
      <p>
        <img src="badge1" /> <img src="badge2" /> ...
      </p>
    </td>
  </tr>
</table>
```

- Project name: `<h4>` with link to `https://github.com/minkhoaa/{repo-name}`
- Description: `<p>` tag, plain text
- Tech badges: `<p>` tag on new line below description, `flat` style, `color=21262d`, `logoColor=8b949e`
- No visible table borders (GitHub default)
- No dividers between cards — whitespace separation

**Card content:**

**Langfens — AI-powered IELTS Platform**
- Repo: `Project_Langfens_Microservice`
- Description: 13 microservices, event-driven architecture, AI-powered grading and speech analysis
- Badges (with logo): `.NET` (dotnet), `PostgreSQL` (postgresql), `RabbitMQ` (rabbitmq), `Redis` (redis), `Elasticsearch` (elasticsearch)
- Badges (text-only, no logo available): `GPT-4o`, `Whisper`

**Peerzee — Full-stack Web Application**
- Repo: `peerzee-fullstack`
- Description: Microservices architecture with speech processing, containerized deployment
- Badges (with logo): `Next.js` (nextdotjs), `NestJS` (nestjs), `Docker` (docker)
- Badges (text-only): `Whisper`, `Playwright`

**Foodify — Social Media Backend**
- Repo: `Foodify-Social-Media-Backend`
- Description: Food-sharing social platform with auth, feed, social features, image CDN
- Badges (with logo): `.NET` (dotnet), `PostgreSQL` (postgresql), `Redis` (redis), `Cloudinary` (cloudinary), `JWT` (jsonwebtokens)

### 4. "Currently Exploring" section

Standalone section with its own `---` dividers, between Tech Stack block and Featured Projects.

Heading: `<h3 align="center">Currently Exploring</h3>`

Uses `flat` style badges (not `for-the-badge`) to visually differentiate from core skills. `color=21262d`, `logoColor=8b949e`.

Badges:
- RAG (text-only, no standard logo)
- LangChain (logo: `langchain`) — verified HAS LOGO

### 5. Other Projects — keep as pin cards

No change from current README state (8 projects across 3 rows of pin cards).

## Section order after changes

1. Header — typing SVG (updated) + identity line (unchanged)
2. `---`
3. Languages & Frameworks (unchanged)
4. Infrastructure (unchanged)
5. DevOps & Cloud (was Environment)
6. `---`
7. Currently Exploring (new)
8. `---`
9. Featured Projects (custom cards)
10. Other Projects (pin cards, unchanged)
11. `---`
12. GitHub Stats (unchanged)
13. `---`
14. Contact (unchanged)

## Color palette

Same as v1. New additions:
- `21262d` used as badge background for `flat` style badges (Currently Exploring + project tech badges). Originally designated as "Border" in v1 palette, now dual-use as flat badge surface.

## Badge logo verification summary

| Slug | Has Logo |
|------|----------|
| nginx | verify |
| githubactions | verify |
| microsoftazure | NO — use text-only |
| googlecloud | verify |
| digitalocean | verify |
| cloudinary | YES |
| jsonwebtokens | YES |
| langchain | YES |
| openai | NO — not used |
| playwright | NO — use text-only |
| nextdotjs | verify |
