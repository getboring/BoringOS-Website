# BoringOS Build Manifest
## Mockingbird Release

Technical specification for what ships. Marketing language included for reference.

---

## Core Philosophy

**The Hotel Room Standard:** Everything you need. Nothing you don't.

**The 10-Year Test:** Every app should still exist in 10 years.

**The Account Test:** If it requires an account to function, don't include it.

---

## Base System

| Component | Choice | Notes |
|-----------|--------|-------|
| Base image | Fedora Silverblue 43 | When available; 42 initially |
| Desktop | GNOME 49 | When available; 48 initially |
| Build system | BlueBuild | Via Universal Blue |
| Package format | Flatpak (apps), rpm-ostree (system) | |

---

## Included Applications

### Web & Communication

| App | Flatpak ID | Marketing Copy |
|-----|------------|----------------|
| Firefox | org.mozilla.firefox | "Click the browser. Type a website. That's it." |
| Thunderbird | org.mozilla.Thunderbird | "Works with Gmail. Works with Yahoo. Works with Outlook. Works with anything." |

### Office & Documents

| App | Flatpak ID | Marketing Copy |
|-----|------------|----------------|
| LibreOffice Writer | org.libreoffice.LibreOffice | "Opens Word files. Saves Word files. Your boss won't know the difference." |
| LibreOffice Calc | org.libreoffice.LibreOffice | "Opens Excel files. Saves Excel files. Your accountant won't know the difference." |
| LibreOffice Impress | org.libreoffice.LibreOffice | "Opens PowerPoint files. Saves PowerPoint files." |
| Evince | org.gnome.Evince | "Click a PDF. It opens." |
| GNOME Text Editor | org.gnome.TextEditor | "Plain text. No fuss." |
| GNOME Calendar | org.gnome.Calendar | "Your schedule." |

### Media

| App | Flatpak ID | Marketing Copy |
|-----|------------|----------------|
| Loupe | org.gnome.Loupe | "Click a photo. It opens." |
| Shotwell | org.gnome.Shotwell | "All your photos. Organized." |
| Celluloid | io.github.celluloid_player.Celluloid | "Click a video. It plays." |
| Rhythmbox | org.gnome.Rhythmbox3 | "Your MP3s. Your albums. Your playlists." |
| Sound Recorder | org.gnome.SoundRecorder | "Record audio." |

### Graphics

| App | Flatpak ID | Marketing Copy |
|-----|------------|----------------|
| Drawing | com.github.maoschanz.drawing | "Simple image editing. Like Paint." |

### System Utilities

| App | Source | Marketing Copy |
|-----|--------|----------------|
| Files | GNOME Core | "Documents here. Pictures here. Downloads here." |
| Settings | GNOME Core | "Everything in one place." |
| Software | GNOME Core | "Search. Click Install. Done." |
| Disks | GNOME Core | "Manage your drives." |
| System Monitor | GNOME Core | "See what's running." |
| Archive Manager | GNOME Core | "Open zip files." |
| Calculator | GNOME Core | "Math." |
| Screenshot | GNOME Core | "Capture your screen." |
| Fonts | GNOME Core | "Manage fonts." |
| Clocks | GNOME Core | "World clocks. Alarms. Timers." |

### Games (Adult)

| App | Flatpak ID | Marketing Copy |
|-----|------------|----------------|
| GNOME Chess | org.gnome.Chess | "Chess." |
| AisleRiot Solitaire | org.gnome.Aisleriot | "80+ card games." |
| GNOME Mines | org.gnome.Mines | "Minesweeper." |
| GNOME Sudoku | org.gnome.Sudoku | "Sudoku." |
| GNOME Mahjongg | org.gnome.Mahjongg | "Mahjongg." |

All games marketing: "Already installed. No ads. No accounts."

### Games (Kids)

| App | Flatpak ID | Marketing Copy |
|-----|------------|----------------|
| GCompris | org.kde.gcompris | "100+ educational activities. Math. Reading. Puzzles. Art." |
| Tux Paint | org.tuxpaint.Tuxpaint | "Drawing for kids." |
| Frozen Bubble | org.frozen_bubble.frozen-bubble | "Puzzle game." |
| SuperTux | org.supertuxproject.SuperTux | "Platformer adventure." |

All kids games marketing: "No ads. No in-app purchases. No 'ask your parent to subscribe.'"

---

## Explicitly NOT Included

| Category | Examples | Reason | Marketing Copy |
|----------|----------|--------|----------------|
| Streaming apps | Spotify, Netflix | Account-required, subscription-dependent | "Work in browser." |
| Work chat | Slack, Teams, Zoom | Account-required, work-specific | "Your work provides these. Available in App Store." |
| Cloud storage | Dropbox, Google Drive | Account-required | "Available in App Store if you want them." |
| Other browsers | Chrome, Edge, Brave | One browser is enough | "Available in App Store. Firefox does the same thing." |
| Complex editors | GIMP, Inkscape, Kdenlive | Power user tools, high learning curve | "Available in App Store." |
| Gaming platforms | Steam, Lutris | Not our focus, account-required | "Available in App Store." |
| Violent games | Any shooter, combat game | Not universal, not appropriate for all ages | — |

---

## Selection Criteria Checklist

Before adding any app, it must pass ALL of these:

- [ ] Will it exist in 10 years?
- [ ] Does it work without creating an account?
- [ ] Is it appropriate for all ages?
- [ ] Is it the obvious/universal choice (not controversial)?
- [ ] Can I write a one-sentence description of what it does?
- [ ] Can I show a screenshot of someone using it?

---

## Total App Count

~33 applications

- System utilities: 10
- Web & Communication: 2
- Office & Documents: 6
- Media: 5
- Graphics: 1
- Adult Games: 5
- Kids Games: 4

---

## BlueBuild Recipe Structure

```yaml
name: boringos-mockingbird
description: "Your computer. Minus the nonsense."
base-image: ghcr.io/ublue-os/silverblue-main:43
image-version: mockingbird

modules:
  - type: rpm-ostree
    repos:
      - https://packages.fedoraproject.org/...
    install:
      # System-level packages
      
  - type: default-flatpaks
    user:
      install:
        # All Flatpak apps listed above
        
  - type: files
    files:
      # Wallpapers
      # Branding
      # Default settings
      
  - type: script
    scripts:
      # GNOME settings (dconf)
      # Remove unwanted defaults
      # Set up user experience
```

---

## GNOME Configuration

Default settings via dconf:

```ini
[org/gnome/desktop/interface]
color-scheme='default'
enable-animations=true

[org/gnome/shell]
favorite-apps=['org.mozilla.firefox.desktop', 'org.mozilla.Thunderbird.desktop', 'org.libreoffice.LibreOffice-writer.desktop', 'org.gnome.Nautilus.desktop', 'org.gnome.Software.desktop']

[org/gnome/desktop/privacy]
remember-recent-files=true
remove-old-temp-files=true
remove-old-trash-files=true

[org/gnome/software]
download-updates=false
download-updates-notify=false
```

---

## Wallpapers

- Default: Tennessee landscape (Mockingbird theme)
- Alternatives: 5-10 nature/abstract options
- Location: /usr/share/backgrounds/boringos/

---

## Branding Files

- /usr/share/pixmaps/boringos-logo.svg
- /usr/share/icons/hicolor/scalable/apps/boringos.svg
- /etc/os-release (customized)
- Plymouth boot theme (simple, fast)

---

## Testing Checklist

Before release, verify:

- [ ] All apps launch
- [ ] Firefox opens websites
- [ ] Thunderbird can add Gmail account
- [ ] LibreOffice opens .docx, .xlsx, .pptx
- [ ] Photos open in Loupe
- [ ] Videos play in Celluloid
- [ ] Music plays in Rhythmbox
- [ ] PDFs open in Evince
- [ ] Games launch and work
- [ ] GCompris activities load
- [ ] Software can install a Flatpak
- [ ] Printing works (basic USB printer)
- [ ] WiFi connects
- [ ] Bluetooth pairs
- [ ] Audio works (speakers, headphones)
- [ ] Updates work
- [ ] Rollback works
