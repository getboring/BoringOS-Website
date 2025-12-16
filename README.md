# BoringOS Website

Marketing website for BoringOS — a Linux distribution for normal people.

**Live site:** [boringos.com](https://boringos.com) (or your Vercel URL)

## Quick Start

```bash
# Clone the repo
git clone https://github.com/yourusername/boringos-site.git
cd boringos-site

# Preview locally
npx serve public

# Open http://localhost:3000
```

## Deploy to Vercel

### Option 1: Vercel CLI
```bash
npm i -g vercel
vercel --prod
```

### Option 2: Git Integration
1. Push to GitHub
2. Connect repo to Vercel
3. Auto-deploys on every push to `main`

## Project Structure

```
boringos-site/
├── public/
│   ├── index.html           # Main landing page
│   ├── mockingbird.html     # Mockingbird release features
│   └── what-is-this.html    # "What is BoringOS?" explainer
├── assets/
│   └── screenshots/         # UI screenshots (add these!)
├── docs/
│   ├── brand-guidelines.md  # Voice, tone, messaging
│   └── build-manifest.md    # Technical specs
├── CLAUDE.md                # Claude Code instructions
├── package.json
├── vercel.json
└── README.md
```

## URLs

| Page | URL | Purpose |
|------|-----|---------|
| Home | `/` | Main landing, download CTA |
| Mockingbird | `/mockingbird` | Current release features |
| What Is This? | `/what-is-this` | Beginner explainer |

## Screenshots Needed

The site uses placeholder text like `[Screenshot: description]`. Replace these with actual screenshots:

1. `desktop-clean.png` — GNOME desktop with dock
2. `firefox-webpage.png` — Browser showing a website
3. `thunderbird-inbox.png` — Email client with messages
4. `libreoffice-writer.png` — Document being edited
5. `libreoffice-calc.png` — Spreadsheet with data
6. `loupe-photo.png` — Photo viewer
7. `celluloid-video.png` — Video player
8. `rhythmbox-music.png` — Music library
9. `files-app.png` — File manager
10. `gnome-software.png` — App store
11. `chess-game.png` — Chess in progress
12. `gcompris-activity.png` — Kids educational game

Place in `/assets/screenshots/` and update HTML `src` attributes.

## Brand Guidelines

See `/docs/brand-guidelines.md` for:
- Voice and tone rules
- Content formula
- Good/bad examples
- What to say and never say

## Tech Stack

- **Framework:** None (static HTML/CSS)
- **Hosting:** Vercel
- **Fonts:** Inter (Google Fonts)

## About BoringOS

BoringOS is a Linux distribution built on:
- Fedora Silverblue
- Universal Blue
- BlueBuild

Curated by Cody Boring in Tennessee.

---

**"Your computer. Minus the nonsense."**
