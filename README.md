# 🧭 BiasRadar-WebRTC — Privacy-First WebRTC Co-Browsing Engine  
> *Part of the BiasRadar Open Source Initiative*  
> Developed by **Stephen Antony Venansious** (steve@algorethics.ai)  
> Chief Mentor by **Prof. Dr. José Berengueres** (jse@ieee.org)  
> Co-Founder & Chief Ethical Innovation Officer — **Robert McNamara** (robert@algorethics.ai)  
> **Powered by [Algorethics.ai](https://algorethics.ai)**  

![License](https://img.shields.io/badge/License-Apache--2.0-blue.svg)
![WebRTC](https://img.shields.io/badge/WebRTC-ready-success.svg)
![Made With](https://img.shields.io/badge/Made%20With-Node.js%20%7C%20React%20%7C%20TypeScript-green.svg)
![Contributions Welcome](https://img.shields.io/badge/Contributions-welcome-brightgreen.svg)
![Maintained](https://img.shields.io/badge/Maintained-Yes-success.svg)

---

## 🌍 Overview

**BiasRadar-WebRTC** is an open-source, privacy-preserving **WebRTC co-browsing SDK** that enables two or more users to browse the web together — each maintaining **independent sessions, cookies, and logins** — while securely sharing their screens, audio, and annotations in real time.  

The live deployment of this project is available at **[BiasRadar.ai](https://BiasRadar.ai)** for user access, collaboration, and research demonstrations.

Built under the **BiasRadar** umbrella, BiasRadar-WebRTC advances **ethical, transparent, and collaborative AI research** by providing a secure, lightweight platform for:

- **Collaborative browsing and annotation**
- **Behavioral and UX research**
- **Digital forensics and AI bias detection**
- **Remote education and usability testing**

---

---

## 🧪 Research & Collaboration Platform

**BiasRadar-WebRTC** is actively hosted on **[BiasRadar.ai](https://BiasRadar.ai)** as part of the **BiasRadar Research and Collaboration Platform** — a live ecosystem for ethical AI experiments, co-browsing studies, and transparency-focused development.

Researchers, developers, and organizations can:
- 🔬 **Run live WebRTC co-browsing experiments** to study human–AI interaction.  
- 🧑‍🤝‍🧑 **Collaborate on ethical AI projects** using BiasRadar’s integrated communication, annotation, and co-analysis tools.  
- 📊 **Access dashboards** for monitoring model fairness, data transparency, and compliance analytics.  
- 🧠 **Use BiasRadar’s open APIs** for integrating bias detection, session auditing, and co-learning modules into existing research pipelines.  
- 🧾 **Publish session insights** as verifiable reports or export co-browsing sessions as reproducible case studies.  

**Platform Highlights:**
- Hosted and maintained by **[Algorethics.ai](https://Algorethics.ai)**.  
- Includes sandbox environments for **BiasRadar-WebRTC**, **DiscernAI**, and **Carlo PEaaS**.  
- Offers **multi-user collaboration** features for universities, researchers, and innovation teams.  
- Supports **on-premise deployment** for organizations working with sensitive data.  

> Visit **[https://BiasRadar.ai](https://BiasRadar.ai)** to explore live sessions, collaborate on open research, or join the global community advancing **ethical, transparent, and responsible AI**.

---

## 🌐 Citation and Research Attribution

If you use **BiasRadar-WebRTC** or its hosted platform in your research, please cite:

> Steaphen Antony Venansious, S. A., & Berengueres, J. (2025).  
> *BiasRadar-WebRTC: A Privacy-First WebRTC Co-Browsing Engine for Ethical AI Research.*  
> Algorethics Open Source Initiative, [https://BiasRadar.ai](https://BiasRadar.ai).

---

## 🧩 Related Projects in the BiasRadar Ecosystem

| Project | Description | Link |
|----------|--------------|------|
| **Carlo PEaaS** | Real-time Policy Enforcement-as-a-Service for AI systems | [https://carlopeaas.dev/](https://carlopeaas.dev/) |
| **DiscernAI** | Bias detection and misinformation monitoring engine | [https://carlopeaas.dev/](https://carlopeaas.dev/) |
| **RoboEthix** | Ethical robotics and autonomy compliance toolkit | [algorethics.ai/roboethix](https://algorethics.ai) |
| **Childsafe.dev** | Privacy-first guardian AI for child safety and content moderation | [childsafe.dev](https://childsafe.dev) |

---

> “At **BiasRadar.ai**, innovation meets integrity — empowering researchers and developers to collaborate responsibly in an open, transparent, and ethically aligned ecosystem.”


## 🔥 Key Features

| Capability | Description |
|-------------|-------------|
| 🧩 **Dual Independent Sessions** | Each user operates in their own browser instance — no shared cookies, no DOM injection. |
| 🎥 **WebRTC A/V + Screen Share** | Peer-to-peer streaming with TURN fallback for NAT traversal. |
| 🗒️ **Notes & Annotations** | Real-time synchronized sticky notes, highlights, and visual markers tied to URLs and timestamps. |
| 🧠 **BiasRadar Integration** | Hooks for behavioral analysis, ethical AI monitoring, and multi-session co-analysis pipelines. |
| 🔒 **Privacy-First Architecture** | No DOM scraping, no cookie access; fully GDPR-compliant and ToS-safe. |
| 🧾 **Export Session PDF** | Generate session summaries (URLs, participants, annotations) using Puppeteer or PDFKit. |
| 🌐 **Lightweight Hosting** | Deploy seamlessly on Vercel, Fly.io, or Render with minimal backend overhead. |

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
**BiasRadar-WebRTC never reads or modifies cookies** — it relies entirely on the browser’s internal session management for seamless continuity (e.g., auto-login behavior).

```
┌────────────────────────┐        WSS        ┌────────────────────────┐
│  Browser A (User A)    │<---------------->│   Signaling Server     │
│  Screen + A/V Stream   │ offers/answers   │  (Node.js + ws)        │
└──────────▲─────────────┘                  └──────────▲─────────────┘
│ WebRTC P2P (A/V + Screen + Data)          │
┌──────────▼─────────────┐                  ┌──────────▼─────────────┐
│  Browser B (User B)    │<---------------->│  TURN Server (Fallback)│
│  Screen + A/V Stream   │ STUN/TURN        │ (Cloudflare/Twilio)   │
└────────────────────────┘                  └────────────────────────┘
```

---

## 🚀 Quick Start

### 1️⃣ Clone the repo

```bash
git clone https://github.com/smartkuttan/biasradar-Webrtc-co-browsing/
cd webrtc
```

### 2️⃣ Install dependencies

```bash
npm install
# or
pnpm install
```

### 3️⃣ Configure environment

Create a `.env` file at the root:

```bash
SIGNALING_PORT=8080
SIGNALING_HOST=0.0.0.0
CORS_ORIGIN=https://your-frontend.app
ICE_URLS=stun:stun.l.google.com:19302,turns:turn.yourdomain.com:5349
ICE_USERNAME=turnuser
ICE_CREDENTIAL=turnpassword
SID_TTL_HOURS=24
```

### 4️⃣ Start the signaling server

```bash
npm run signaling
```

### 5️⃣ Launch the demo client

```bash
npm run dev
```

Open two browsers:

* **User A** → click “Start Surfing” → copy invite link.
* **User B** → open link → join session.
* Begin real-time collaborative browsing with A/V and notes.

---

## 🔒 Security & Compliance

* **Screen-share only:** no DOM proxying or cookie access.
* **TLS 1.2+ enforced:** on all signaling and media connections.
* **SID links:** 128-bit entropy, fully revocable and expirable.
* **GDPR-ready:** minimal data retention, opt-in storage ≤ 30 days.
* **Visible consent indicators:** during microphone, camera, or screen usage.

---

## 📜 License

This project is licensed under the **Apache 2.0 License** — see the [`LICENSE`](LICENSE) file for details.

```
Copyright © 2025  
Stephen Antony Venansious  
Mentor and Guide – Prof. Dr. José Berengueres  
```

---

## 🧭 Roadmap (v1.3)

* [ ] Multi-participant sessions (>2 users)
* [ ] Remote pointer and scroll synchronization
* [ ] URL co-pilot mode (push links live)
* [ ] Session recording with consent banners
* [ ] Rich PDF timeline templates
* [ ] Localization / caption support
* [ ] WebSocket cluster scaling on Fly.io

---

## 💡 Academic and Research Use

**BiasRadar-WebRTC** supports:

* Human–AI interaction studies
* Digital bias auditing
* UX collaboration research
* Ethical data collection frameworks

**For research collaborations, contact:**
📧 **Prof. Dr. José Berengueres** — [jse@ieee.org](mailto:jse@ieee.org)
📧 **Stephen Antony Venansious** — [steve@algorethics.ai](mailto:steve@algorethics.ai)

---

## 🤝 Contributing

We welcome pull requests and research contributions!

1. **Fork** the repository
2. **Create a feature branch**

   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Commit your changes**

   ```bash
   git commit -m "Add some amazing feature"
   ```
4. **Push your branch**

   ```bash
   git push origin feature/amazing-feature
   ```
5. **Open a Pull Request**

Ensure all submissions align with **BiasRadar’s Ethical AI Contribution Guidelines** (see `/docs/ETHICS.md`).

---

## 🧑‍💻 Maintainers

| Name                           | Role                                          | Contact                                               |
| ------------------------------ | --------------------------------------------- | ----------------------------------------------------- |
| **Stephen Antony Venansious**  | Lead Developer                                | [steve@algorethics.ai](mailto:steve@algorethics.ai)   |
| **Prof. Dr. José Berengueres** | Mentor & Research Advisor                     | [jse@ieee.org](mailto:jse@ieee.org)                   |
| **Robert McNamara**            | Co-Founder & Chief Ethical Innovation Officer | [robert@algorethics.ai](mailto:robert@algorethics.ai) |

---

## 🌟 Acknowledgments

* The **BiasRadar** initiative for promoting ethical AI collaboration.
* **Prof. Dr. José Berengueres** for mentorship in design thinking and human–computer interaction.
* **Robert McNamara** for leadership in ethical innovation and project vision.
* The **open-source WebRTC community** for foundational technologies enabling transparent digital collaboration.

> “**BiasRadar-WebRTC transforms digital observation into ethical collaboration — empowering researchers, developers, and educators to explore the web together with respect for privacy, transparency, and truth.**”
