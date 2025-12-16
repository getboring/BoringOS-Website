# BoringOS Brand Guidelines v3.0

## The Rule

**Show. Don't explain.**

Every piece of content answers: "What does this look like? What happens when I click?"

Not: "What is this conceptually? Why does it exist?"

---

## Voice

**Declarative.** Not descriptive.

| Don't say | Say |
|-----------|-----|
| "BoringOS is an operating system that provides..." | "This is what you see when you turn it on." |
| "You can browse the internet just like you normally would..." | "Click the browser. Type a website. That's it." |
| "LibreOffice provides Microsoft Office compatibility..." | "Opens Word files. Saves Word files. Your boss won't know the difference." |
| "The system is designed to be user-friendly..." | [Screenshot of the thing being easy] |

**Short.** One idea per sentence.

| Don't say | Say |
|-----------|-----|
| "BoringOS comes with a comprehensive suite of applications that cover all your daily computing needs, from web browsing to document editing to media playback." | "Everything you need. Already installed." |

**Specific.** Name the thing.

| Don't say | Say |
|-----------|-----|
| "A full-featured web browser" | "Firefox" |
| "An office suite" | "LibreOffice" |
| "Media applications" | "Photos. Videos. Music." |

**No jargon.** Ever.

| Don't say | Say |
|-----------|-----|
| "Wayland compositor" | "Smooth graphics" |
| "Atomic updates with rollback" | "Updates you can undo" |
| "Flatpak sandboxing" | "Apps can't mess with each other" |
| "GNOME 49" | [Just show the screenshot] |

---

## Content Formula

Every feature, every page, every section follows this:

1. **"This is how you [do thing]."** — Headline
2. **[Screenshot]** — Show the screen
3. **One sentence.** — What happens when you do it
4. **Move on.** — No elaboration

Example:

> **This is how you write a document.**
> 
> [Screenshot of LibreOffice Writer]
> 
> Opens Word files. Saves Word files. Your boss won't know the difference.

---

## The "Never See" Pattern

The emotional gut punch. Show Windows annoyances, crossed out.

Format:
- ~~"Your PC doesn't meet requirements"~~ ✕
- What BoringOS does instead (one line)

Use sparingly. Maximum 6 items. These are:

1. "Your PC doesn't meet requirements" → Runs on computers Windows rejected
2. Ads in Start menu → No ads anywhere
3. "Restart now to update" → Updates when you want
4. "Sign in with Microsoft" → No account required
5. "Give Edge a chance" → No nagging
6. Virus warnings → Different system, different security

---

## App Philosophy

**The Complete Package.** Like a good hotel room.

A hotel room has everything: TV, coffee maker, iron, hairdryer, alarm clock. You don't need to leave the room to get anything essential.

BoringOS ships complete. Every app you need. No more. No less.

### The 10-Year Test

Every included app must answer: "Will this still exist in 10 years?"

- Firefox: 20+ years ✓
- LibreOffice: 20+ years ✓
- Chess: 1500+ years ✓
- Spotify app: Maybe not ✗

### The Account Test

If it requires an account to function at all, don't include it.

Exception: Email client (Thunderbird) — works with ANY email provider.

### The Controversy Test

If reasonable people disagree about the best option, include the most universal one or none.

- Web browser: Firefox (universal, independent)
- Office suite: LibreOffice (opens everything)
- Photo editor: None (too many opinions — use App Store)

---

## What's Included

When listing apps, group by what people DO, not by category:

| Task | App | Why |
|------|-----|-----|
| Browse the internet | Firefox | Works everywhere |
| Check email | Thunderbird | Works with any provider |
| Write documents | LibreOffice Writer | Opens Word files |
| Make spreadsheets | LibreOffice Calc | Opens Excel files |
| Create presentations | LibreOffice Impress | Opens PowerPoint files |
| View PDFs | Evince | Just works |
| View photos | Loupe + Shotwell | View and organize |
| Watch videos | Celluloid | Plays everything |
| Listen to music | Rhythmbox | Your MP3s, your way |
| Play games | Chess, Solitaire, Sudoku, etc. | No ads, no accounts |
| Kids learn | GCompris | 100+ activities |
| Get more apps | Software | Thousands available |

---

## What's NOT Included (and why)

Be explicit. People want to know.

| Not Included | Why |
|--------------|-----|
| Spotify, Netflix apps | Require accounts. Work fine in browser. |
| Slack, Teams, Zoom | Work apps. Your work provides these. |
| Chrome | Firefox does the same thing. Chrome available in App Store. |
| GIMP | Power user tool. Available in App Store. |
| Steam | Gaming platform. Not our focus. Available in App Store. |

---

## Messaging Hierarchy

1. **Headline:** What you see / What you do
2. **Screenshot:** Proof
3. **One line:** What happens
4. **Never:** Paragraphs of explanation

---

## Taglines

Primary: **"Your computer. Minus the nonsense."**

Alternates:
- "Same computer. Better software."
- "Everything you need. Nothing you don't."
- "Turn it on. Do your stuff. Turn it off."

Never use:
- "Freedom" (means nothing to normal people)
- "Open source" (they don't care)
- "Community" (sounds like a cult)
- "Customizable" (sounds like work)
- "Privacy-focused" (sounds paranoid)

---

## Visual Rules

1. **Screenshots are mandatory.** No feature without a screenshot.
2. **Show real UI.** Not mockups, not illustrations.
3. **Show normal use.** A document with text. An inbox with emails. A photo of a family.
4. **Clean desktop.** Don't show 50 apps open.
5. **No terminals.** Ever. Unless someone specifically asks about command line.

---

## Naming

**Release names:** Tennessee state wildlife

- Mockingbird (current)
- Future: Raccoon, Firefly, Elk, Bobcat, etc.

**Version numbers:** Don't emphasize. People don't care about 1.0 vs 1.1.

---

## Attribution

Always credit the stack. Footer of every page:

> Built with Universal Blue and BlueBuild, based on Fedora.
> Curated by Cody Boring in Tennessee.

---

## The Test

Before publishing anything, ask:

1. **Can I show a screenshot?** If no, rewrite until I can.
2. **Is it one sentence?** If no, cut it.
3. **Would my mom understand it?** If no, simpler words.
4. **Does it answer "what do I click?"** If no, make it concrete.

---

## Examples: Good vs Bad

**Bad:**
> BoringOS provides a streamlined computing experience with carefully curated applications designed to meet the needs of everyday users while maintaining system stability and security.

**Good:**
> This is what you see when you turn it on.
> [Screenshot]
> A desktop. A dock. Your apps. Nothing else.

---

**Bad:**
> Our email client supports IMAP, POP3, and Exchange protocols, allowing you to connect to virtually any email provider.

**Good:**
> Works with Gmail. Works with Yahoo. Works with Outlook. Works with anything.

---

**Bad:**
> BoringOS includes a comprehensive office productivity suite that provides compatibility with Microsoft Office file formats.

**Good:**
> Opens Word files. Saves Word files. Your boss won't know the difference.
