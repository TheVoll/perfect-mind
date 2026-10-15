---
name: perfect-mind
description: The Human-Grade UI Copywriting, Cognitive Ergonomics & Anti-AI-Slop Standard. Enforces quiet precision, eliminates prompt leaking (e.g. naming panels after internal user instructions), bans shouting uppercase titles and unrequested emojis, and guarantees collision-proof responsive spatial layouts.
---

# Perfect Mind Standard

An authoritative design engineering and microcopy standard for AI agents. While `perfect-design` governs pixels, geometry, and color tokens, `perfect-mind` governs the intelligence, voice, cognitive ergonomics, and spatial restraint of user interfaces.

Software crafted under `perfect-mind` feels quiet, confident, understated, and unmistakably designed by a senior human craftsman.

---

## 1. The Core Philosophy: Quiet Precision

AI coding agents suffer from chronic verbal and visual insecurity. When prompted, an LLM defaults to:
1. **Prompt Leaking**: Blindly plastering user prompt keywords or architectural mechanisms into the UI (e.g., naming a modal *"Yatay Yönetim Paneli"* or *"State Container View"* because the user asked for a horizontal layout).
2. **Technical Shouting**: Writing all-caps technical jargon with parenthetical brags (`"VIKO SİSTEM YAPILANDIRMASI & KISAYOL MERKEZİ (ENGINE V2)"` instead of `"Settings"`).
3. **Emoji Contamination**: Decorating buttons and titles with amateur emojis (🚀, ✨, ⚡, 🎨) that make professional software look like student demos.
4. **Spatial Blindness**: Cramming every requested button into one row without responsive breakpoints, causing controls to collide and overlap when panels widen or windows shrink.
5. **Character Encoding Mojibake**: Corrupting Unicode and international diacritics into broken glyphs (`o `, `Ǭ`).

`perfect-mind` establishes non-negotiable architectural boundaries to eradicate this slop permanently.

---

## 2. The 6 Iron Laws of Perfect Mind

### Law 1: The Prompt Isolation Firewall (Zero Leakage)
**The user's prompt is a directive to the engineer, NEVER copy for the user interface.**

- **The Violation**: If the user prompt says *"bana ayarları yatay yönetim paneli şeklinde yap"*, an uncalibrated AI creates a header reading:
  `"Yatay Yönetim Paneli"` or `"VIKO SİSTEM YAPILANDIRMASI"`.
- **The Rule**: Strip all architectural meta-talk, structural adjectives, internal component names, and user prompt tokens before writing any UI label.
- **The Translation Table**:
  | User Prompt / Internal Architecture | Amateur AI Output (Banned) | Perfect-Mind Output (Required) |
  | :--- | :--- | :--- |
  | "ayarları yatay panel yap" | `"Yatay Yönetim Paneli"` | `"Settings"` (sub: `"Preferences & Shortcuts"`) |
  | "sol katmanlar ve asset paneli" | `"SOL SIDEBAR (LAYERS & 800+ ASSETS)"` | `"Left Sidebar"` (sub: `"Layers & Assets"`) |
  | "piksel adımı snap motoru" | `"HAREKET ADIMI & PİKSEL HASSASİYETİ (SNAP ENGINE)"` | `"Snap & Precision"` |
  | "kopyala yapıştır ofset sistemi" | `"SİSTEM PANOSU & YAPIŞTIRMA OFSETİ (CLIPBOARD ENGINE)"` | `"Clipboard Offset"` |
  | "yön oklarıyla hassas hareket" | `"YÖN OKLARIYLA HASSAS HAREKET (ARROW NUDGING)"` | `"Keyboard Nudge"` |
  | "akıllı hizalama kılavuzları" | `"AKILLI SAĞ TIK & HİZALAMA MOTORU"` | `"Smart Alignment & Guides"` |

---

### Law 2: The 1–2 Word Action Standard (The Surgical Verb)
Action triggers, buttons, and navigation tabs must communicate maximum intent with minimum noise.

- **Banned**: Verbose AI sentences, explanatory buttons, marketing hype.
  - ❌ `"Tüm Projeyi JSON ve Kod Olarak Dışa Aktar"`
  - ❌ `"Click here to export your masterpiece"`
  - ❌ `"Yeni Bir Proje Tasarımı Oluştur"`
- **Required**: 1 to 2 words. Let the icon and context provide deference.
  - ✅ `"Export"`
  - ✅ `"New Design"`
  - ✅ `"Save"`
  - ✅ `"Duplicate"`
  - ✅ `"Reset (100%)"`

---

### Law 3: The Shouting & Jargon Ban
- **Banned**: ALL-CAPS titles, parenthetical marketing boasts, and pseudo-engineering buzzwords.
  - ❌ `"CANVAS RENDERING ACCELERATION MATRIX"`
  - ❌ `"BLUEPRINT HUD ULTRA"`
  - ❌ `"COLOR SYSTEM V3 PRO"`
- **Required**: Human Title Case or Sentence case. Calm, modest, functional.
  - ✅ `"Canvas renderer"`
  - ✅ `"Blueprint overlay"`
  - ✅ `"Color swatch"`

---

### Law 4: The Emoji Prohibition
**Zero emojis in production interfaces, tools, and technical applications.**

- Emojis in buttons (`🚀 Export`, `✨ Enhance`, `⚡ Snap`), dialog headers, tabs, and status bars are strictly banned.
- Emojis communicate artificial hype, break layout baselines, vary unpredictably across operating systems, and ruin visual hierarchy.
- **Always use crisp, 1px monochrome vector SVG icons** (SF Symbols, Feather, Lucide, or hand-tuned path vectors) styled with theme tokens (`#FFFFFF`, `Theme.textSecondary`).

---

### Law 5: Spatial Grace & Collision-Proof Responsive Layouts
An interface that breaks or overlaps when resized is an engineering failure.

- **The Spacer Invariant**: Never put multiple fixed-width rows next to each other inside a layout. Always separate Left, Center, and Right groups with elastic spacers:
  ```qml
  Item { Layout.fillWidth: true; Layout.minimumWidth: 4 }
  ```
- **The Text Boundary Invariant**: Any editable title, project name, or user-generated string in a toolbar must have an explicit maximum width and clip/elide behavior:
  ```qml
  Item {
      width: Math.min(180, Math.max(70, parent.width * 0.10))
      clip: true
      TextInput { elide: Text.ElideRight; ... }
  }
  ```
- **The 3-Tier Responsive Breakdown**:
  - **Tier 1 (Core Essentials - Never Hide)**:
    Back button, Brand logo, Project title, Save, Export CTA, Window controls.
  - **Tier 2 (Primary Tools - Hide only under severe constraint < 1024px)**:
    Zoom % controls, Sidebar toggles, Undo/Redo.
  - **Tier 3 (Contextual Badges & Secondary Controls - Gracefully Hide)**:
    Hardware display badge (`visible: root.width >= 1320`), Canvas resolution badge (`visible: root.width >= 1200`), Wallpaper sync toggle (`visible: root.width >= 1180`), Snap dropdown (`visible: root.width >= 1080`).

---

### Law 6: Linguistic Dignity & Character Integrity
- **UTF-8 Sacredness**: Every file must be written and saved strictly as **UTF-8 without BOM**. Never allow `o `, ``, `Ǭ`, or ASCII substitutions into source code.
- **Natural Native Voice**: Write authentic, idiomatic language. If Turkish: write like a native Turkish senior product designer (`"Dışa Aktar"`, `"Ayarlar"`, `"Hizalama"`), not an automated mechanical translator.

---

## 3. Pre-Flight Verification Checklist

Before finalizing any UI code, run this mental audit:

1. [ ] **No Leaked Words**: Did I use words from the user's prompt (like *"yatay"*, *"yönetim paneli"*, *"ekran boyutu"*) in headers or labels? If yes, replace with standard product vocabulary.
2. [ ] **No Shouting**: Are any titles in ALL-CAPS with parenthetical boasting? Convert to clean Title Case.
3. [ ] **No Emojis**: Are there any emojis in buttons, tabs, or dialogs? Replace with vector icons or clean text.
4. [ ] **Collision Test**: If the window width shrinks from 1920px to 1024px, or if a sidebar is dragged from 250px to 450px, do topbar elements overlap? Ensure elastic spacers and responsive breakpoints are active.
5. [ ] **Character Cleanliness**: Are all quotes, Turkish characters (ş, ğ, ü, ö, ç, ı, İ), and symbols rendering as clean UTF-8 without mojibake?
