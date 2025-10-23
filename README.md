# 🧭 CoSurf — Privacy-First WebRTC Co-Browsing Engine  
> *Part of the BiasRadar Open Source Initiative*  
> Developed by **Stephen Antony Venansious** (steve@algorethics.ai)  
> Guided by **Prof. Dr. José Berengueres** (jse@ieee.org)

![License](https://img.shields.io/badge/License-Apache--2.0-blue.svg)
![WebRTC](https://img.shields.io/badge/WebRTC-ready-success.svg)
![Made With](https://img.shields.io/badge/Made%20With-Node.js%20%7C%20React%20%7C%20TypeScript-green.svg)
![Contributions Welcome](https://img.shields.io/badge/Contributions-welcome-brightgreen.svg)
![Maintained](https://img.shields.io/badge/Maintained-Yes-success.svg)

---

## 🌍 Overview

**CoSurf** is an open-source, privacy-preserving **WebRTC co-browsing SDK** that allows two or more people to browse the web together — each maintaining **independent sessions, cookies, and logins** — while securely sharing their screens, audio, and annotations in real-time.

Built under the **BiasRadar** umbrella, CoSurf aims to advance **ethical, transparent, and collaborative AI research** by providing a secure, lightweight platform for:
- **Collaborative browsing and annotation**
- **Behavioral and UX research**
- **Digital forensics and AI bias studies**
- **Remote education and usability testing**

---

## 🔥 Key Features

| Capability | Description |
|-------------|-------------|
| 🧩 **Dual Independent Sessions** | Each user uses their own browser instance — no shared cookies, no DOM injection. |
| 🎥 **WebRTC A/V + Screen Share** | Peer-to-peer media streaming with TURN fallback for NAT traversal. |
| 🗒️ **Notes & Annotations** | Real-time synced sticky notes, highlights, and visual markers tied to URLs + timestamps. |
| 🧠 **BiasRadar Integration** | Hooks for digital behavior studies, ethical AI monitoring, and co-analysis pipelines. |
| 🔒 **Privacy-First Architecture** | No DOM scraping, no cookie access; complies with GDPR and platform ToS. |
| 🧾 **Export Session PDF** | Export session summary (URLs, participants, annotations) using Puppeteer or PDFKit. |
| 🌐 **Lightweight Hosting** | Minimal backend footprint — deploy easily on Vercel, Fly.io, or Render. |

---

## 🧰 Tech Stack

| Layer | Technology |
|--------|-------------|
| **Frontend** | React / Next.js + Tailwind |
| **Realtime Engine** | WebRTC (P2P + TURN) + WebSockets |
| **Backend** | Node.js (NestJS or Express) |
| **Auth** | NextAuth / Firebase Auth / OAuth (Google, Apple, Microsoft) |
| **Database** | Supabase / Firebase / PostgreSQL |
| **PDF Export** | Puppeteer / PDFKit |
| **TURN** | Twilio / Vonage / Cloudflare / coturn |

---

## 🧱 Architecture
Each participant’s browser manages its own cookies and sessions natively.  
**CoSurf never reads or modifies cookies** — it relies solely on the browser’s internal state to enable “auto-login” continuity.

---

## 🚀 Quick Start

### 1️⃣ Clone the repo

```bash
git clone https://github.com/biasradar/cosurf.git
cd cosurf
npm install
# or
pnpm install
## 🔒 Security & Compliance

- **Screen-share only:** no DOM proxying or cookie access.  
- **TLS 1.2+ enforced:** on all signaling and media connections.  
- **SID links:** 128-bit entropy, fully revocable and expirable.  
- **GDPR-ready:** minimal data retention, opt-in storage ≤ 30 days.  
- **Visible consent indicators:** during microphone, camera, or screen usage.  

---

## 📜 License

This project is licensed under the **Apache 2.0 License** — see the [`LICENSE`](LICENSE) file for details.

🧑‍💻 Maintainers
Name	Role	Contact
Stephen Antony Venansious	Lead Developer	steve@algorethics.ai

Prof. Dr. José Berengueres	Mentor & Research Advisor	jse@ieee.org
🌟 Acknowledgments

The BiasRadar initiative for promoting ethical AI collaboration.

Prof. Dr. José Berengueres for continuous mentorship in design thinking and human–computer interaction.

The open-source WebRTC community for foundational technologies enabling transparent digital collaboration.

“CoSurf turns digital observation into ethical collaboration — empowering researchers, developers, and educators to explore the web together with respect for privacy and truth.”
