# BoringOS Website - Claude Code Instructions

## What This Is

Marketing website for BoringOS, a Linux distribution for normal people. Built on Fedora/Universal Blue/BlueBuild.

## Core Principle

**Show. Don't explain.**

Every feature = screenshot + one sentence. No paragraphs of explanation. Apple-style marketing.

## Voice Rules

- Declarative, not descriptive: "This is how you browse the internet." not "You can browse the internet..."
- One sentence per idea
- Name specific apps (Firefox, not "a browser")
- No jargon ever (no "Wayland", no "Flatpak", no "atomic updates")
- No Linux community language ("freedom", "open source", "customizable")

## Content Formula

```
1. "This is how you [do thing]." — Headline
2. [Screenshot] — Show the screen
3. One sentence. — What happens
4. Move on. — No elaboration
```

## File Structure

```
/public
  index.html          # Main landing page
  mockingbird.html    # Features page (current release)
  what-is-this.html   # Beginner explainer
  
/assets
  /screenshots        # All UI screenshots (required for every feature)
  
/docs
  brand-guidelines.md # Voice, tone, messaging rules
  build-manifest.md   # Technical specs (apps, Flatpak IDs, etc.)
```

## Deployment

- Host: Vercel
- Type: Static site
- Build: None required (plain HTML/CSS)
- Deploy: `vercel --prod` or push to main branch

## Screenshot Requirements

Every "This is how you..." section needs a real screenshot. Placeholders are marked with `[Screenshot: description]` in the HTML.

Required shots:
1. Clean desktop (dock, wallpaper, nothing open)
2. Firefox with webpage
3. Thunderbird inbox
4. LibreOffice Writer with document
5. LibreOffice Calc with data
6. Photo viewer with image
7. Video player
8. Music player
9. Files app
10. Software center
11. Chess game
12. GCompris (kids)

## Key Messaging

**Tagline:** "Your computer. Minus the nonsense."

**The pitch:** Same computer. Same files. Same apps. No ads. No tracking. No forced updates. No Microsoft.

**The emotional hit:** "This is what you'll never see" — crossed-out Windows annoyances.

## Technical Foundation (for reference only, never mention in marketing)

- Base: Fedora Silverblue 42/43
- Desktop: GNOME 48/49
- Build: BlueBuild via Universal Blue
- Apps: Flatpak

## Quick Commands

```bash
# Local preview
npx serve public

# Deploy to Vercel
vercel --prod

# Check links
npx linkinator public/index.html
```
