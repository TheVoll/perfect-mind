# Perfect Mind

> **The Human-Grade UI Copywriting, Cognitive Ergonomics & Anti-AI-Slop Standard.**  
> Crafted by TheVoll. Inspired by Apple HIG, Linear Method, Dieter Rams, and Figma.

---

## What is Perfect Mind?

While [`perfect-design`](https://github.com/TheVoll/perfect-design) establishes the visual physics, Swiss 8px grids, squircle radii, and calibrated typography tokens, **`perfect-mind`** is the cognitive brain.

It exists to eradicate the most frustrating failure mode of AI coding assistants: **AI Slop in UI copy and spatial architecture.**

AI agents naturally suffer from verbal excess, prompt-leaking, shouting uppercase titles, unrequested emoji spam, and spatial blindness that causes toolbar buttons to collide when windows resize. `perfect-mind` provides the definitive standard to build software that feels quiet, confident, and unmistakably crafted by an experienced human product designer.

---

## The 6 Iron Laws

### 1. The Prompt Isolation Firewall (Zero Leakage)
The user's prompt is an instruction to the engineer, **never** UI copy.
- **AI Slop**: User asks *"make the settings a horizontal management panel"* -> AI titles the modal `"Horizontal Management Panel"` or `"SYSTEM CONFIGURATION & SHORTCUT CENTER"`.
- **Perfect Mind**: The modal is titled `"Settings"` with subtitle `"Preferences & Shortcuts"`.

### 2. The 1–2 Word Action Standard
Actions must be surgical verbs. Let spatial context and vector icons provide deference.
- **AI Slop**: `"Export Entire Project as Code and JSON"`, `"Click here to export your masterpiece"`, `"Create a Brand New Design Project"`.
- **Perfect Mind**: `"Export"`, `"Save"`, `"New Design"`.

### 3. The Shouting & Jargon Ban
Never use all-caps screaming or parenthetical technical boasting in UI titles.
- **AI Slop**: `"LEFT SIDEBAR BEHAVIOR (LAYERS & 800+ ASSETS)"`, `"SYSTEM CLIPBOARD & PASTE OFFSET (CLIPBOARD ENGINE V2)"`, `"ARROW NUDGING MATRIX"`.
- **Perfect Mind**: `"Left Sidebar"`, `"Clipboard Offset"`, `"Arrow Nudge"`.

### 4. The Emoji Prohibition
Zero emojis in production tools, buttons, dialogs, and headers.
- Emojis degrade serious developer tools into looking like toys or AI prototypes.
- Use clean, monochrome 1px vector SVG icons.

### 5. Spatial Grace & Collision-Proof Responsive Layouts
Toolbars and headers must never overlap or collide when sidebars expand or window widths shrink.
- Use elastic spacers (`Layout.fillWidth: true; Layout.minimumWidth: 4`).
- Constrain editable title inputs (`Math.min(160, Math.max(70, width * 0.10))`).
- Use 3-tier responsive degradation: hide secondary hardware badges gracefully when width < 1200px so core tools (Back, Title, Save, Export, Window Controls) never touch.

### 6. Linguistic Dignity & Character Integrity
- Strict UTF-8 without BOM. Zero mojibake or broken character substitutions.
- Write natural, idiomatic human copy--never literal machine translations.

---

## Before & After

| Surface | Robotic AI Slop (Banned) | Perfect Mind Standard (Required) |
| :--- | :--- | :--- |
| **Settings Header** | `"SYSTEM CONFIGURATION & SHORTCUT CENTER"` + `"Horizontal Management Panel"` | `Settings` - `Preferences & Shortcuts` |
| **Settings Tab 1** | `"General & Workspace (All System Settings & Rail Engine)"` | `General` - `Panels, docking & layout` |
| **Export CTA** | `"Instantly Export Entire Project Now"` | `Export` |
| **Section Title** | `"LEFT SIDEBAR BEHAVIOR (LAYERS & 800+ ASSETS)"` | `Left Sidebar` |
| **TopBar Layout** | Fixed rows that crash into each other on small screens | Elastic spacers + responsive tiering (0 collision) |
| **Close Button** | Mangled text glyphs or emoji close symbols | Crisp 1px vector close icon (`Icons.close`) |

---

## Installation & Usage

### As an Antigravity / Gemini Agent Skill
Place `SKILL.md` into your agent's customization directory:
```bash
# Windows
%USERPROFILE%\.gemini\config\skills\perfect-mind\SKILL.md

# macOS / Linux
~/.gemini/config/skills/perfect-mind/SKILL.md
```

### In Cursor / Windsurf / Claude Code
Add to your project rules (`.cursorrules` or `AGENTS.md`):
```markdown
Follow the Perfect Mind standard for all UI microcopy, dialog headers, and responsive toolbars:
- Zero prompt-leaking in titles (never name a panel after the prompt description).
- 1-2 words for action triggers.
- Zero emojis in UI components.
- Responsive tiering on toolbars to eliminate element collision on window resize.
```

---

## License
MIT (c) 2026 TheVoll
