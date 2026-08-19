<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=1000&color=58A6FF&center=true&vCenter=true&width=500&lines=Hey%2C+I'm+Subhankar+%F0%9F%91%8B;Final-Year+SDE+%40+BIT+Mesra+%2727;Real-Time+Systems+%7C+AI+Tooling;Open+to+Full-Time+SDE+Roles" alt="Typing SVG" />
</div>

<div align="center">

[![Portfolio](https://img.shields.io/badge/Portfolio-my--portfolio--suwubh.vercel.app-58A6FF?style=flat-square&logo=vercel&logoColor=white)](https://my-portfolio-suwubh.vercel.app)
[![Email](https://img.shields.io/badge/Email-subhankarsatpathy69%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:subhankarsatpathy69@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-subhankar--satpathy-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/subhankar-satpathy)

</div>

---

## Who I Am

I'm a final-year ECE student at BIT Mesra (graduating 2027). I spend most of my time building web apps, solving competitive programming problems, and going down rabbit holes about how distributed systems actually work.

Over the past year I've built a few projects I'm genuinely proud of. A real-time collaborative whiteboard where I had to figure out conflict resolution across peers. A multiplayer chess platform that I load-tested until I was happy with the numbers. A social reading app with a vector search engine under the hood. I care a lot about whether the thing I built actually works when people use it.

I'm currently looking for full-time SDE roles starting 2027 — also open to remote work or freelance collaborations if you're building something interesting in the meantime.

- Currently building: Chess4Nerds mobile + more AI features in Scriblio
- Learning: distributed systems internals, advanced CRDT patterns
- Semifinalist, HackOn with Amazon S6 — Top 300 of 100,000+ teams (built Amazon Second Life)
- IEEE Technical Lead at BIT Mesra, led a 5-person team and shipped 3 club projects
- Top 1% on Chess.com (1750 Elo) — I like puzzles :)

---

## What I Work With

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

## Projects

### [Scriblio](https://github.com/suwubh/Scriblio) — Collaborative Whiteboard with AI · [Live Demo](https://scriblio-rose.vercel.app/)
> TypeScript · React · Yjs (CRDT) · WebRTC · WebSockets · Redis · OpenAI/Groq · Docker · k6

The core problem I was trying to solve: how do you keep a shared canvas consistent when multiple people are editing at the same time and the network isn't reliable? I ended up using Yjs CRDTs for conflict resolution and a hybrid WebRTC + WebSocket fallback so edits go through even when P2P drops.

I also added an AI command palette (Cmd+K) so you can describe a diagram in plain English and it gets drawn for you. Ran a small usability study with 22 people and median diagram creation time went from 95s to 38s.

Load tested the WebSocket signaling server with k6: 25 concurrent clients, ~9,800 messages over 60s, 0 connection errors, 107ms median round-trip on the live deployment.

---

### [Chess4Nerds](https://github.com/suwubh/Chess4Nerds) — Multiplayer Chess Platform · [Live Demo](https://chess4-nerds-frontend.vercel.app/)
> TypeScript · React · Node.js · WebSockets · Redis · PostgreSQL · Prisma · Turborepo · GitHub Actions

Chess is a good problem domain for learning real-time systems because so many things can go wrong. A player disconnects mid-game. Two moves arrive out of order. You need to scale to more than one server.

I handled disconnects with DB-backed game state so you can rejoin where you left off. Move validation is server-side so you can't cheat. Redis pub/sub lets game broadcasts cross WebSocket replicas. Under k6 load (220 VUs, 60s) it held 110+ concurrent matches at 305 moves/sec with p95 propagation at 112ms.

Also built a minimax AI opponent from scratch with alpha-beta pruning and MVV-LVA move ordering. Three difficulty levels via search depth 2/3/4.

---

### [ReadHaven](https://github.com/suwubh/ReadHaven) — Social Reading Platform · [Live Demo](https://read-haven-sandy.vercel.app)
> Next.js 16 · TypeScript · PostgreSQL + pgvector · Prisma · NextAuth · Jest · GitHub Actions · Vercel

The part I enjoyed most was the recommendation engine. I embedded 7K+ books using all-MiniLM-L6-v2 (384 dimensions) and indexed them with pgvector's ivfflat index for cosine similarity search. It powers both the /discover semantic search page and "More like this" on every book detail page.

Wrote a proper test suite for this one: 132 tests across 19 suites, 91% line coverage. Lighthouse score: 100 SEO, 90 Accessibility.

---

### [Amazon Second Life](https://github.com/suwubh) — Multimodal Returns & Resale Platform · HackOn with Amazon S6
> Python · FastAPI · Gemini 2.5 Flash · AWS Bedrock (Nova) · DynamoDB · Docker · Lambda

Built during HackOn with Amazon Season 6, where our team placed in the Top 300 out of 100,000+ registrants. The problem: retailers lose huge value on returned items that could easily be resold instead of scrapped. Second Life takes photos/video of a returned item and uses Gemini 2.5 Flash to assess condition and generate a resale listing automatically, with AWS Bedrock Nova as an automatic failover if Gemini is unavailable.

Enforced strict Pydantic JSON-schema validation on every model response so a malformed AI output never breaks the pipeline. Shipped as a Dockerized FastAPI service on Lambda, with DynamoDB for listing storage.

---

### [PiggyTrack](https://github.com/suwubh/PiggyTrack) — Finance Tracker · [Live Demo](https://piggytrack-vbyp.onrender.com)
> React · Node.js · Express · MongoDB · JWT

Personal finance dashboard with spending charts, JWT auth, and Excel export. Simpler than the others but a clean, complete full-stack app.

---

## GitHub Stats

<div align="center">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=suwubh&show_icons=true&theme=github_dark&include_all_commits=true&count_private=true&hide_border=true&bg_color=0D1117&cache_seconds=86400" />
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=suwubh&layout=compact&theme=github_dark&hide_border=true&bg_color=0D1117&cache_seconds=86400" />
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

## Tech Stack

<div align="center">
  <img src="https://skillicons.dev/icons?i=ts,react,nextjs,nodejs,express,postgres,mongodb,redis,docker,git,vercel,tailwind&perline=6" />
</div>

---

## Let's Talk

I'm looking for full-time SDE roles after graduation in 2027 — also open to freelance projects or remote collaboration in the meantime. If you're working on something interesting, feel free to reach out.

<div align="center">

**[subhankarsatpathy69@gmail.com](mailto:subhankarsatpathy69@gmail.com)** · **[LinkedIn](https://linkedin.com/in/subhankar-satpathy)** · **[Portfolio](https://my-portfolio-suwubh.vercel.app)**

</div>

---

<div align="center">
  <img src="https://komarev.com/ghpvc/?username=suwubh&color=58A6FF&style=flat-square&label=Profile+Views" />
</div>
