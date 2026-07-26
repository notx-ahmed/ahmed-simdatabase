<!-- ═══════════════════════════════════════════════════════════════ -->
<!--                          BANNER                                   -->
<!-- ═══════════════════════════════════════════════════════════════ -->

<div align="center">

<h1>
  🇵🇰 &nbsp;PAK Number&nbsp;<code>→</code>&nbsp;Info Tool
</h1>

<p><em>A sleek, single-file web console for Pakistan mobile-number OSINT lookups.</em></p>

<p>
  <img alt="Made with HTML5"   src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white">
  <img alt="Styled with CSS3"  src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white">
  <img alt="Vanilla JS"        src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black">
  <img alt="No Dependencies"   src="https://img.shields.io/badge/dependencies-0-success?style=for-the-badge">
</p>

<p>
  <img alt="Zero build step" src="https://img.shields.io/badge/build-none-blueviolet?style=flat-square">
  <img alt="Dark / Light"    src="https://img.shields.io/badge/theme-dark%20%2F%20light-0a0f1a?style=flat-square">
  <img alt="Responsive"      src="https://img.shields.io/badge/layout-responsive-00c3ff?style=flat-square">
  <img alt="Maintained"      src="https://img.shields.io/badge/status-active-brightgreen?style=flat-square">
</p>

<sub>⦿ Powered by ┇ <strong>@NOTX_AHMED_</strong></sub>

</div>

---

## 📑 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Preview](#-preview)
- [Quick Start](#-quick-start)
- [Usage](#-usage)
- [Number Formats](#-number-formats)
- [How It Works](#-how-it-works)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Configuration](#-configuration)
- [Roadmap](#-roadmap)
- [Disclaimer](#-disclaimer)
- [Contact](#-contact)

---

## 🔭 Overview

**PAK Number → Info Tool** is a lightweight, self-contained web app that queries a
Pakistan mobile-number lookup API and renders the response as clean, color-coded
JSON. Everything — markup, styling, and logic — lives in a single `index.html`
file, so it runs anywhere a browser does: no server, no build tools, no
`npm install`.

> Drop the file on any static host (or just double-click it) and you're live.

---

## ✨ Features

| | Feature | Description |
|---|---|---|
| 🎨 | **Advanced UI** | Glassmorphism panel, animated grid backdrop, floating orbs, and a gradient sheen title. |
| 🌙 | **Dark / Light theme** | One-click toggle, remembers your choice, and respects your OS preference. |
| 🧮 | **Smart number parsing** | Accepts local (`03…`), international (`92…`), and bare 10-digit formats. |
| 🌈 | **JSON syntax highlighting** | Keys, strings, numbers, and booleans are color-coded for readability. |
| 📋 | **One-click copy** | Copy the formatted JSON result straight to your clipboard. |
| ⚡ | **Instant actions** | Lookup, Clear, and Example buttons plus <kbd>Enter</kbd>-to-search. |
| 📱 | **Fully responsive** | Adapts cleanly from widescreen down to mobile. |
| 🪶 | **Zero dependencies** | Pure HTML/CSS/JS in one file — nothing to install. |

---

## 🖼️ Preview

<div align="center">

<!-- Add a screenshot at assets/preview.png to have it show here -->
<img src="assets/preview.png" alt="App preview" width="720"
     onerror="this.style.display='none'">

<em>Dark mode (default) &nbsp;·&nbsp; Light mode available via the header toggle.</em>

</div>

---

## 🚀 Quick Start

**Option A — just open it**

```bash
git clone https://github.com/notx-ahmed/ahmed-simdatabase.git
cd ahmed-simdatabase
# open index.html in your browser (double-click, or:)
xdg-open index.html   # Linux
open index.html       # macOS
start index.html      # Windows
```

**Option B — serve locally**

```bash
# Python 3
python3 -m http.server 8080
# then visit http://localhost:8080
```

---

## 🕹️ Usage

1. **Enter a number** in the input field (see [supported formats](#-number-formats)).
2. Click **🔍 LOOKUP** — or press <kbd>Enter</kbd>.
3. Read the color-coded JSON in the output panel.
4. Use **📋 COPY JSON** to copy the result, **🗑️ CLEAR** to reset, or
   **📝 EXAMPLE** to auto-fill a sample number.
5. Flip between **dark** and **light** with the theme toggle in the header.

---

## 🔢 Number Formats

The parser normalizes all of the following to the canonical `92XXXXXXXXXX` form:

| Input example    | Interpreted as   | Notes                         |
|------------------|------------------|-------------------------------|
| `923078750447`   | `923078750447`   | Full international format      |
| `03078750447`    | `923078750447`   | Local format, leading `0`      |
| `3078750447`     | `923078750447`   | Bare 10-digit national number  |

Anything that doesn't resolve to a valid 12-digit `92…` number is rejected with
a clear error message.

---

## ⚙️ How It Works

```text
 ┌────────────┐     normalize      ┌──────────────┐     fetch      ┌───────────┐
 │  Raw input │ ─────────────────▶ │ 92XXXXXXXXXX │ ─────────────▶ │  Lookup   │
 └────────────┘                    └──────────────┘                │    API    │
                                                                   └─────┬─────┘
                                          render + highlight              │
 ┌──────────────────────────────┐   ◀──────────────────────────────  JSON │
 │  Color-coded JSON in panel    │                                        ▼
 └──────────────────────────────┘
```

1. **Normalize** — strip non-digits and coerce to the `92…` international form.
2. **Validate** — ensure a well-formed 12-digit number before any request.
3. **Fetch** — call the configured lookup endpoint with the normalized number.
4. **Clean & render** — tidy the payload, tag the credit, and pretty-print it
   with syntax highlighting.

---

## 🧰 Tech Stack

- **HTML5** — semantic single-file markup
- **CSS3** — custom properties (theming), gradients, backdrop-filter, keyframe animations
- **Vanilla JavaScript** — `fetch`, `localStorage`, clipboard API — **no frameworks**

---

## 🗂️ Project Structure

```text
ahmed-simdatabase/
├── index.html   # The entire app — markup, styles, and logic
└── README.md    # You are here
```

---

## 🔧 Configuration

The lookup endpoint is defined near the top of the script in `index.html`:

```js
const BASE_URL = "https://api-server-virid-two.vercel.app/number=";
```

Point `BASE_URL` at any compatible endpoint that accepts an appended number and
returns JSON.

---

## 🗺️ Roadmap

- [ ] Lookup history with quick re-run
- [ ] Export result as `.json` file
- [ ] Bulk lookup from a pasted list
- [ ] Optional API-key field in the UI
- [ ] Shareable deep links

---

## ⚠️ Disclaimer

This tool is provided for **educational and authorized use only**. You are
responsible for ensuring your queries comply with all applicable laws and with
the terms of service of any data provider. The maintainers assume no liability
for misuse.

---

## 📬 Contact

- **Telegram:** [@devil_inside5](https://t.me/devil_inside5)
- **Instagram:** [@notx_ahmed_](https://instagram.com/notx_ahmed_)
- **GitHub:** [notx-ahmed](https://github.com/notx-ahmed)

<div align="center">
<sub>Built with 🩵 &nbsp;·&nbsp; ⦿ Powered by ┇ <strong>@NOTX_AHMED_</strong></sub>
</div>
