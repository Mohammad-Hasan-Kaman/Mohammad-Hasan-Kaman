# Hi, I'm Mohammad Hasan Kaman 👋

<img align="right" width="150" height="150" alt="Mohammad Hasan Kaman" src="https://mhkaman.com/media/profile/photo.jpg" />

Full-stack developer building **AI applications, developer tooling, and secure systems**.
I ship end-to-end software in **Python**, **C#** and **Django** — from AI-driven clinical
screening pipelines and encrypted desktop messengers to diagnostics for LLM streaming APIs
and production web platforms.

🌐 **Portfolio: [mhkaman.com](https://mhkaman.com)** · **Live product: [kahaai.ir](https://kahaai.ir)** · 📄 **CV: [mhkaman.com/en/cv](https://mhkaman.com/en/cv)**

[![Followers](https://img.shields.io/github/followers/Mohammad-Hasan-Kaman?style=for-the-badge&logo=github&label=Followers&color=0969DA)](https://github.com/Mohammad-Hasan-Kaman?tab=followers)
[![Stars](https://img.shields.io/github/stars/Mohammad-Hasan-Kaman?style=for-the-badge&logo=github&label=Total%20Stars&color=yellow)](https://github.com/Mohammad-Hasan-Kaman?tab=repositories)
[![Forks](https://img.shields.io/github/forks/Mohammad-Hasan-Kaman?style=for-the-badge&logo=github&label=Forks&color=blue)](https://github.com/Mohammad-Hasan-Kaman?tab=repositories)
[![Repos](https://img.shields.io/github/repos/Mohammad-Hasan-Kaman?style=for-the-badge&logo=github&label=Public%20Repos&color=0969DA)](https://github.com/Mohammad-Hasan-Kaman?tab=repositories)

---

## 🧩 Languages

![Python](https://img.shields.io/badge/Python-58.48%25-3776AB?style=for-the-badge&logo=python&logoColor=white) ![HTML](https://img.shields.io/badge/HTML-20.15%25-E34F26?style=for-the-badge&logo=html5&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-10.07%25-F7DF1E?style=for-the-badge&logo=javascript&logoColor=white) ![CSS](https://img.shields.io/badge/CSS-8.82%25-1572B6?style=for-the-badge&logo=css&logoColor=white) ![C%23](https://img.shields.io/badge/C%23-2.45%25-239120?style=for-the-badge&logo=csharp&logoColor=white)

*Byte share across the 12 project repositories, from the GitHub `/languages` API.*

---

## 🚀 Flagship Projects

*Ordered by GitHub stars — most-starred first.*

### 🤖 [kaman-ai-translator](https://github.com/Mohammad-Hasan-Kaman/kaman-ai-translator) · ⭐ 48 · v3.0.0

**Translate whole books, not sentences.** A PyQt6 desktop studio that turns PDF & EPUB
books into fluent academic Persian — and back into English — one page at a time or an
entire book unattended.

- **Whole-book automation** with pause/resume across restarts and app updates; every
  finished page is saved instantly to a per-file job store.
- **Structure-aware** — per-book templates for headings, labels and page furniture;
  headers/footers are detected and stripped before translation.
- **Quality pipeline** — a QC review loop, per-page chunking with context rolling, and
  scanned-page support — a page with no text layer is sent to the model as an
  image and transcribed before translation.
- **RTL export** — HTML output shaped for right-to-left reading, plus EPUB.
- **Privacy by design** — API keys encrypted with Windows DPAPI (labelled base64
  fallback), stored locally; the only network traffic is to the provider you configure.
- **303 offline tests** that run headlessly — the core is deliberately Qt-free.
- Works with **Gemini** or any **OpenAI-compatible** server. Ships as a Windows
  `.exe` in [releases](https://github.com/Mohammad-Hasan-Kaman/kaman-ai-translator/releases)
  (current: **v3.0.0**).

### 🩺 [agent-stream-doctor](https://github.com/Mohammad-Hasan-Kaman/agent-stream-doctor) · ⭐ 5 · v0.2.0

**Diagnose why your LLM stream gave you nothing.** A zero-dependency Python CLI that
reads raw SSE chat-completion captures and tells you exactly what went wrong — instead
of you staring at an empty response box.

- **12 checks, each with an explanation** — `empty-stream`, `reasoning-only-response`,
  `missing-finish-reason`, `malformed-sse-line`, `invalid-json-payload`,
  `data-after-done`, `incomplete-tool-call`, `unparseable-tool-arguments`,
  `empty-content-stream`, `inconsistent-finish-reason`, `role-not-announced` and
  `stream-ended-without-done`.
- **Two ways in** — `record` performs a live streaming call and saves the raw SSE;
  `analyze` diagnoses a capture you already have. Works fully offline.
- **Tolerant parser** — a diagnostic tool that crashes on malformed input is useless, so
  every deviation becomes a finding instead of an exception.
- **Script-friendly** — exit codes `0` healthy / `1` problems found / `2` usage error,
  plus `--json` for CI.
- **Usable as a library** — `from agent_stream_doctor import diagnose`.
- Core is **stdlib only**; `--record` is the single optional dependency.

### 🤖 [ai-counseling-widget](https://github.com/Mohammad-Hasan-Kaman/ai-counseling-widget) · ⭐ 1 · v1.0.0

**An AI intake system for counseling centers — shipped as a Persian RTL chat widget.**
The AI *is* the product: it talks to every visitor, runs the GHQ-28 wellbeing screening,
extracts clinical concepts from what they say, and matches them to the right consultant.

- **AI triage assistant** — computes each next question from the visitor's previous
  answers instead of following a rigid form.
- **GHQ-28 screening** — 28 questions across four subscales, scored and interpreted
  server-side.
- **Consultant matching** — ranks available consultants by gender, branch, age, session
  type, extracted concepts, screening results and live appointment slots, with a
  "why this match" explanation.
- **Self-learning** — success/failure reports re-weight the engine per tenant.
- **Multi-tenant by design** — API keys, admin accounts, allowed domains, flows and
  consultant data are isolated per tenant; one `<script>` tag embeds it.
- **Fully local AI** — no third-party LLM, no per-message cost, no visitor data leaves
  your server.
- FastAPI + SQLite, Persian-first RTL UI, background availability crawler, Excel export.

🌐 Live product: **[kahaai.ir](https://kahaai.ir)**

### 💬 [ai-counseling-bot](https://github.com/Mohammad-Hasan-Kaman/ai-counseling-bot) · ⭐ 1 · v1.0.0

**The same intelligence, as a Bale messenger bot.** Guided intake → GHQ-28 screening →
a self-learning engine ranks the counselors that fit the person's situation, and admins
run everything from inside the chat: statistics, Excel import/export, broadcasts, and
feedback that retrains the matching engine.

- **SpiralMatchEngine** — hard filters (gender, branch, age bounds), then weighted
  scoring across topic fit, concept match and free-appointment count.
- **Concept extraction** — free text mapped to clinical concepts via a synonym
  dictionary with Persian/Arabic variants.
- **Name normalization** — fuzzy counselor-name matching, so user input never has to
  be exact.
- **Availability awareness** — a crawler refreshes open slots every 2 hours so the
  engine prefers counselors who can actually be booked.
- No external API, no cloud LLM, no per-message cost.

---

## 📂 All Projects

*The rest of the portfolio, by category.*

### 🧰 AI & Developer Tools

| Project | What it does |
|---|---|
| **[kaman-ai-chat](https://github.com/Mohammad-Hasan-Kaman/kaman-ai-chat)** · ⭐ 1 | C# WinForms chat assistant (DeepSeek via OpenModel API) with native Windows text-to-speech, embedded send/receive sounds, and an API key resolved at runtime — env var, `app.config` or `%APPDATA%`. Single dependency-free `.exe`. |

### 🔐 Security & Networking

| Project | What it does |
|---|---|
| **[kaman-messenger](https://github.com/Mohammad-Hasan-Kaman/kaman-messenger)** · ⭐ 1 | Real-time encrypted messenger built from scratch: TCP sockets, Fernet (AES) traffic encryption, bcrypt auth, rate limiting, SQLite storage, CustomTkinter GUI. Ships as client + server `.exe`. |

### 🌐 Web Platforms

| Project | What it does |
|---|---|
| **[kaman-portfolio](https://github.com/Mohammad-Hasan-Kaman/kaman-portfolio)** · ⭐ 1 | Trilingual (EN/FA/AR) Django portfolio — every page editable from admin, trilingual PDF CV generator with RTL shaping, privacy-friendly server-side analytics, sitemap/robots/llms.txt built in. **Live at [mhkaman.com](https://mhkaman.com)** |
| **[dr-kaman-site](https://github.com/Mohammad-Hasan-Kaman/dr-kaman-site)** · ⭐ 1 | Multimedia archive for Dr. Mohammad Reza Kaman — audio, video, books, articles. Django + nginx + gunicorn on a Linux VPS. **Live at [drkaman.ir](https://drkaman.ir)** |
| **[planikaa-portal](https://github.com/Mohammad-Hasan-Kaman/planikaa-portal)** · ⭐ 1 | Django educational platform: exam & competition analysis with visual dashboards, an educational blog, a review/feedback system, Jalali (Persian) calendar support and `django-allauth` accounts. |

### 🖥 Desktop Tools & Bots

| Project | What it does |
|---|---|
| **[quran-group-bot](https://github.com/Mohammad-Hasan-Kaman/quran-group-bot)** · ⭐ 1 | Serverless Bale bot that runs a 30-person weekly Quran juz reading circle — Cloudflare Workers + KV, cron-scheduled posts, rotating juz assignment, weekly hadith. |
| **[youtube-downloader](https://github.com/Mohammad-Hasan-Kaman/youtube-downloader)** · ⭐ 1 | Windows YouTube downloader on yt-dlp with a Persian-language dark-mode GUI, three live progress bars, video/audio format selection and browser-cookie support. |
| **[kaman-web-browser](https://github.com/Mohammad-Hasan-Kaman/kaman-web-browser)** · ⭐ 1 | Lightweight multi-tab Windows browser on Microsoft Edge WebView2 (Chromium) with smart URL-vs-search routing. |

---

## ✍️ Writing

*Technical articles on the live portfolio — the reasoning behind the flagship projects.*

| Article | Covers |
|---|---|
| **[📖 Building a Persian-first desktop translator for PDF and EPUB books](https://mhkaman.com/en/articles/building-a-persian-first-desktop-translator-for-pdf-and-epub-books/)** | Why a 300-page book fails in a chat window — chunking, rolling context, and a per-book structure template. |
| **[🧠 Building an AI counseling widget that matches visitors to the right counselor](https://mhkaman.com/en/articles/building-an-ai-counseling-widget-that-matches-visitors-to-counselors/)** | Replacing the form-and-phone funnel with a conversational intake — without a hosted LLM. |
| **[💬 Shipping a counseling bot on Bale](https://mhkaman.com/en/articles/shipping-a-counseling-bot-on-bale-with-ghq-28-screening-and-self-learning-matching/)** | GHQ-28 screening, self-learning matching, and 12 conversation states inside a messenger. |
| **[🩺 Why is my LLM stream empty? A field guide to broken SSE responses](https://mhkaman.com/en/articles/why-is-my-llm-stream-empty/)** | The four failure modes behind empty streaming responses — and the tool that diagnoses them. |

---

## 🧠 Tech Stack

| Area | Technologies |
|---|---|
| **Languages** | Python · C# · JavaScript · HTML · CSS |
| **Backend** | Django · FastAPI · REST APIs · raw TCP sockets · SQLite |
| **Desktop** | PyQt6 · CustomTkinter · WinForms (WebView2) |
| **AI engineering** | OpenAI-compatible APIs · Gemini · DeepSeek · GHQ-28 screening · concept extraction · SSE streaming · tool calling |
| **Ops & Infra** | Cloudflare Workers/KV · nginx + gunicorn on Linux VPS · BIND9 DNS · Docker · Git |

---

## 📊 GitHub Stats

![Stats](https://github-readme-stats.vercel.app/api?username=Mohammad-Hasan-Kaman&show_icons=true&theme=tokyonight)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs?username=Mohammad-Hasan-Kaman&layout=compact&theme=tokyonight)

![Streak](https://streak-stats.demolab.com?user=Mohammad-Hasan-Kaman&theme=tokyonight)

---

## 📌 Currently

- 🧠 Shipping **[kaman-ai-translator](https://github.com/Mohammad-Hasan-Kaman/kaman-ai-translator) v3** — whole-book Persian translation with a QC loop and DPAPI-encrypted keys
- 🩺 Running **[ai-counseling-widget](https://github.com/Mohammad-Hasan-Kaman/ai-counseling-widget)** and **[ai-counseling-bot](https://github.com/Mohammad-Hasan-Kaman/ai-counseling-bot)** in production for counseling centers — live at **[kahaai.ir](https://kahaai.ir)**
- 🩺 Turning real-world LLM-router debugging sessions into **[agent-stream-doctor](https://github.com/Mohammad-Hasan-Kaman/agent-stream-doctor)**
- 🎓 Finishing secondary education (graduation expected mid-2028) while freelancing for international clients
- 🤝 Open to collaborating on Python developer tools, AI agents and open-source projects

---

## 📬 Find me

[![Portfolio](https://img.shields.io/badge/Portfolio-mhkaman.com-0969DA?style=flat&logo=googlechrome&logoColor=white)](https://mhkaman.com)
[![Kahaai](https://img.shields.io/badge/Live%20Product-kahaai.ir-0969DA?style=flat&logo=googlechrome&logoColor=white)](https://kahaai.ir)
[![X/Twitter](https://img.shields.io/badge/X-@kaman_hasan0975-black?style=flat&logo=x)](https://x.com/kaman_hasan0975)
[![Telegram](https://img.shields.io/badge/Telegram-@mohaka0975-26A5E4?style=flat&logo=telegram&logoColor=white)](https://t.me/mohaka0975)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-kaman--programmer-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kaman-programmer)
[![Email](https://img.shields.io/badge/Email-mohammadhasankaman%40gmail.com-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:mohammadhasankaman@gmail.com)

---

## 📄 License

All repositories in this profile are released under the [MIT License](LICENSE).

## 🤝 Contributing

Issues and pull requests are welcome on any repository here — see each project's
`CONTRIBUTING.md` for the specifics.
