# 🩺 VitaCore AI — The Health Cockpit of the Future

> AI-powered holistic health platform — **v1.0 MVP**

VitaCore AI is a web-based health platform that gathers your water, medication, sleep, weight, and pain data in a single hub, features a voice-guided interactive AI coach, and processes your data analytically.

⚠️ **Medical Disclaimer:** VitaCore AI is an artificial intelligence assistant and is not a substitute for professional medical advice, diagnosis, or treatment. Please consult your doctor for severe pain.

---

## 📂 Project Structure

| File | Description |
|---|---|
| `index.html` | **Landing Page** — hero, target audience, features, smart system rules, user journey |
| `app.html` | **Interactive MVP Demo** — state-driven health cockpit simulation |
| `.claude/launch.json` | Local preview server configuration |

Both pages are **single-file static HTML**; no build step or installation required.

## 🚀 Getting Started

**Option 1 — Open directly:**
Double-click `index.html`. (Internet connection required; libraries load from CDN.)

**Option 2 — Local server (recommended):**

```bash
npx http-server . -p 4173
# → http://localhost:4173
```

## ✨ Features

### Landing Page (`index.html`)
- Hero section with a live dashboard mockup
- 3 target user personas and the problems being solved
- 6 module cards (cockpit, streak, pain map, AI coach, document reader, analytics)
- "Action → Reaction" smart system rules and a 9-step user journey
- Contact form (Formspree integration) — name, e-mail, topic, and message delivered straight to the inbox
- Smooth reveal-on-scroll animations, mobile menu

### Interactive Demo (`app.html`)
| Module | Dynamic Behavior |
|---|---|
| 🛡️ **Legal Consent Wall** | The cockpit stays blurred/locked until the disclaimer is accepted |
| 👤 **Profile Input** | Height/weight/age input → live BMI calculation |
| 💧 **Water Tracking** | `+250ml` fills the bar; completing the goal grants +2 streak |
| 💊 **Medication Checklist** | Each checked medication makes the streak flame glow |
| 🔥 **Streak Flame** | Animated point system tied to daily goals |
| 🧠 **Pain Map** | SVG body silhouette, 1-10 slider; **lower back ≥ 7 → flags a caution in the workout coach** (review your prescription with your physiotherapist) |
| 🏋️ **Exercise Coach (prescription player)** | Moves are **not AI-generated** — they come from the user's uploaded prescription (`RECETE`) and are applied **in order**. Per-move duration/reps × sets, set-rest and move-rest countdowns, sequence rail, voice coach, congratulations card + streak on finish. Camera-based form tracking is a placeholder (next phase) |
| 📄 **AI Document Reader** | Drag & drop → scanning animation → sample lab result output |
| 📊 **Analytics** | Weight / medication adherence / pain trend charts + AI weekly summary report |

## 🛠️ Tech Stack

- **React 18** (UMD, CDN) + **Babel Standalone** — state-driven simulation in `app.html`
- **Tailwind CSS** (CDN) — dark theme; emerald/cyan/slate palette
- **lucide / lucide-react** — icon set
- **Inter** — typography

> **Note:** The `window.react = window.React;` line in `app.html` is intentional — the lucide-react UMD bundle looks for the React global in lowercase.

## 🗺️ Roadmap (Post-MVP)

- [ ] PWA: service worker, offline support, smart push notifications
- [ ] Real AI document analysis (OCR + health filter extraction)
- [x] Voice coach via the Web Speech API (`speechSynthesis`, TR-TR)
- [ ] Prescription upload — PDF / JSON parser so users can load their own exercise list
- [ ] Camera-based form tracking (pose estimation, `CameraStage` placeholder is live)
- [ ] User accounts and data persistence
- [ ] DOCX upload support

---

© 2026 VitaCore AI · All rights reserved · **v1.0 MVP**
