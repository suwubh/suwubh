<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=26&duration=3000&pause=1000&color=58A6FF&center=true&vCenter=true&width=700&lines=Hey%2C+I'm+Subhankar+%F0%9F%91%8B;Full-Stack+Developer+%40+BIT+Mesra;Real-Time+Systems+%E2%80%A2+AI+Tooling+%E2%80%A2+Scalable+Backends;Open+to+Remote+Work+%26+Freelance" alt="Typing SVG" />
</div>

<div align="center">

[![Portfolio](https://img.shields.io/badge/Portfolio-my--portfolio--suwubh.vercel.app-58A6FF?style=flat-square&logo=vercel&logoColor=white)](https://my-portfolio-suwubh.vercel.app)
[![Email](https://img.shields.io/badge/Email-subhankarsatpathy69%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:subhankarsatpathy69@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-subhankar--satpathy-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/subhankar-satpathy)

[![LeetCode](https://img.shields.io/badge/LeetCode-Knight%201769-FFA116?style=flat-square&logo=leetcode&logoColor=black)](https://leetcode.com/suwubh)
[![Codeforces](https://img.shields.io/badge/Codeforces-Specialist%201459-1F8ACB?style=flat-square&logo=codeforces&logoColor=white)](https://codeforces.com/profile/suwubh)
[![CodeChef](https://img.shields.io/badge/CodeChef-3%E2%98%85%201669-5B4638?style=flat-square&logo=codechef&logoColor=white)](https://codechef.com/users/suwubh)

</div>

---

## Who I Am

I'm a **pre-final year ECE student at BIT Mesra** (graduating 2027) who builds production-grade full-stack systems — not just side projects. My focus is on the hard stuff: real-time collaboration, distributed state, AI integration, and systems that hold up under load.

I've built platforms that handle **110+ concurrent users with sub-120ms latency**, run usability studies that resulted in a **60% reduction in task completion time**, and shipped test suites with **91% code coverage** — all before finishing my degree.

I'm actively looking for **remote engineering roles, internships, and freelance work** where I can build things that matter.

- 🔭 Currently building: Chess4Nerds mobile + deeper AI integration in Scriblio
- 🧠 Exploring: Advanced CRDT implementations, distributed systems internals
- 🏆 Achievements: SIH 2025 Finalist · HackQuest 2025 Winner · NTSE Scholar · KVPY Fellow
- 🎯 IEEE Technical Lead @ BIT Mesra — led a 5-person team, reviewed 20+ PRs, shipped 3 club projects
- ♟️ Chess.com top 1% globally (1750 Elo) — pattern recognition is my thing

---

## 🛠️ What I Work With

| Layer | Tools |
|---|---|
| **Languages** | TypeScript, JavaScript (ES6+), C++, Java, SQL |
| **Frontend** | React.js, Next.js, Tailwind CSS, SSR, WebRTC |
| **Backend** | Node.js, Express.js, WebSockets, REST APIs, JWT, OAuth |
| **AI / LLM** | OpenAI API, Groq API, pgvector, sentence-transformers |
| **Databases** | PostgreSQL, MongoDB, Redis, Prisma |
| **DevOps** | Docker, GitHub Actions, AWS (S3, EC2), Vercel, Turborepo, Jest, k6 |
| **CS Core** | DSA, OOP, DBMS, OS, Computer Networks, System Design |

---

## 🚀 Featured Projects

### [Scriblio](https://github.com/suwubh/Scriblio) — AI-Powered Collaborative Whiteboard
> *TypeScript · React · Yjs (CRDT) · WebRTC · WebSockets · Redis · OpenAI/Groq · Docker · k6*

The interesting engineering problem here: how do you keep a shared canvas consistent across peers when the network is unreliable? I solved it with **Yjs CRDTs for eventual consistency** and a **hybrid WebRTC + WebSocket fallback** so writes are never blocked by connectivity.

**Numbers that matter:**
- Load-tested the signaling server with k6: **25 concurrent clients, ~9,800 messages over 60s, 107ms median RTT, 0 connection errors** on the live cloud deployment
- Built a natural-language AI command palette (Cmd+K) using OpenAI/Groq — in a **22-participant usability study**, median diagram creation time dropped from **95s → 38s (60% faster)**, with 82% of users preferring the AI flow and a **4.3/5 "would use again" score**
- 4-service Docker Compose architecture: React client · WebSocket signaling · AI command service · Redis presence layer

---

### [Chess4Nerds](https://github.com/suwubh/Chess4Nerds) — Real-Time Multiplayer Chess Platform
> *TypeScript · React · Node.js · WebSockets · Redis · PostgreSQL · Prisma · Turborepo · GitHub Actions*

Building a chess platform sounds simple until you have to handle concurrent games at scale, reconnections without state loss, and a matchmaking system that's actually fair.

**Numbers that matter:**
- **110+ concurrent matches at 305 moves/sec**, p95 move propagation **112ms** under k6 load (220 VUs, 60s, single Node WS replica)
- Server-authoritative move validation via chess.js, async write-behind to Postgres, and DB-backed game rejoin on reconnect
- Redis pub/sub relay layer for horizontal WS scaling; GitHub Actions CI on every PR
- **From-scratch minimax + alpha-beta AI opponent** with MVV-LVA move ordering and piece-square-table evaluation — configurable easy/medium/hard via search depth 2/3/4
- Elo-band matchmaking (±100, widens with wait time)

---

### [ReadHaven](https://github.com/suwubh/ReadHaven) — Social Book Discovery Platform · [Live Demo](https://read-haven-sandy.vercel.app)
> *Next.js 16 · TypeScript · PostgreSQL + pgvector · Prisma · NextAuth · Jest · GitHub Actions · Vercel*

The feature I'm proudest of here isn't the social feed — it's the vector-similarity recommendation engine. Book embeddings via **all-MiniLM-L6-v2 (384-dim)**, indexed with **pgvector ivfflat for cosine distance**, powering both semantic search and "More Like This" on every book page.

**By the numbers:**
- **7K+ book catalog** seeded from Open Library with ISBN deduplication
- Jest test suite: **132 tests across 19 suites**, **91% line / 88% statement coverage** on auth and API handlers
- GitHub Actions CI/CD with ephemeral pgvector/pgvector:pg16 service containers
- **Lighthouse: 100 SEO / 90 Accessibility**

---

### [PiggyTrack](https://github.com/suwubh/PiggyTrack) — Personal Finance Dashboard · [Live Demo](https://piggytrack-vbyp.onrender.com)
> *React · Node.js · Express · MongoDB · JWT*

Full-stack finance tracker with RESTful APIs, JWT auth, interactive spending charts, and one-click Excel export. A cleaner, more focused project — good example of doing a simple thing really well.

---

## 📊 GitHub Stats

<div align="center">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=suwubh&show_icons=true&theme=github_dark&include_all_commits=true&count_private=true&hide_border=true&bg_color=0D1117" />
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=suwubh&layout=compact&theme=github_dark&hide_border=true&bg_color=0D1117" />
</div>

<div align="center">
  <img src="https://streak-stats.demolab.com?user=suwubh&theme=github-dark-blue&hide_border=true&background=0D1117" />
</div>

<div align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=suwubh&theme=github-compact&hide_border=true&bg_color=0D1117&color=58A6FF&line=58A6FF&point=FFFFFF" />
</div>

---

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/suwubh/suwubh/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/suwubh/suwubh/output/github-snake.svg" />
  <img alt="Snake eating my contributions" src="https://raw.githubusercontent.com/suwubh/suwubh/output/github-snake.svg" />
</picture>

---

## 🏆 Trophies

<div align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=suwubh&theme=algolia&no-frame=true&no-bg=true&row=1&column=7" />
</div>

---

## Let's Work Together

I'm open to **remote internships, full-time roles, and freelance projects** — especially anything involving real-time systems, AI tooling, or complex backend architecture. If you're building something interesting and need someone who ships production-ready code, let's talk.

<div align="center">

**[subhankarsatpathy69@gmail.com](mailto:subhankarsatpathy69@gmail.com)** · **[LinkedIn](https://linkedin.com/in/subhankar-satpathy)** · **[Portfolio](https://my-portfolio-suwubh.vercel.app)**

</div>

---

<div align="center">
  <img src="https://komarev.com/ghpvc/?username=suwubh&color=58A6FF&style=flat-square&label=Profile+Views" />
</div>
