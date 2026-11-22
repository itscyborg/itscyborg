<div align="center">

# Hey, I'm Niraj Kumar 👋

**Full-Stack Developer · Backend Focused · Prop Firm & Trading Platforms**

I build the backend systems prop firms run on: trading engines, challenge and risk-rule engines, double-entry ledgers and real-time market data, plus the trader dashboards and admin panels on top. Outside trading, I build APIs and real-time apps with Node.js, NestJS, PostgreSQL and Next.js.

[![Profile Views](https://komarev.com/ghpvc/?username=itscyborg&label=Profile%20views&color=0e75b6&style=flat-square)](https://github.com/itscyborg)
[![Portfolio](https://img.shields.io/badge/Portfolio-nirajkumar.dev-f97316?style=flat-square&logo=googlechrome&logoColor=white)](https://nirajkumar.dev)
[![Prop Firm Developer](https://img.shields.io/badge/Prop%20Firm%20Developer-Case%20studies-1a1b27?style=flat-square&logo=googlechrome&logoColor=white)](https://nirajkumar.dev/prop-firm-developer)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Niraj%20Kumar-0A66C2?style=flat-square)](https://www.linkedin.com/in/niraj-k-a03295131/)
[![Gmail](https://img.shields.io/badge/nirajuser@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:nirajuser@gmail.com)
[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20me%20a%20coffee-FFDD00?style=flat-square&logo=buy-me-a-coffee&logoColor=black)](https://www.buymeacoffee.com/@itscyborg)

</div>

---

## 🧠 About Me

- 📈 &nbsp;I specialise in **prop firm and trading platform development**: evaluations, risk rules, ledgers and live market data
- 🔭 &nbsp;Currently leading the backend of a **prop-trading platform**, from the trading engine and ledger to the risk engine and admin backend
- 🧱 &nbsp;I care about **idempotent, lock-safe** code paths for anything that touches money
- 💬 &nbsp;Have also built **real-time messaging clients** with offline-first storage, optimistic sends and live sync
- 🌱 &nbsp;Going deeper into **system design, PostgreSQL internals and event-driven architecture**
- 🤝 &nbsp;Open to **prop firm builds, freelance and full-time** backend or full-stack roles

---

## 📈 Prop Firm & Trading Platforms

### Prop-trading firm platform: backend lead
A simulated prop firm. Traders buy an evaluation, trade perpetual futures on live market data, and get a funded account if they hit the profit target without breaking the risk rules.

- **Trading engine:** market and limit orders, take-profit and stop-loss, reduce-only closes, one-way position netting, funding and liquidation. Orders fill against the real order-book depth within slippage bounds, not at the mid price.
- **Challenge engine:** profit targets, drawdown and daily-loss floors, consistency rules, and automatic progression from evaluation phases to a funded account. Rules are pinned to each account when it's created, so editing a program never changes the rules for traders already in it.
- **Risk detection:** a live pass blocks fills that would add exposure as soon as a floor is touched. A settled pass then confirms breaches from the market archive.
- **Double-entry ledger:** Postgres triggers reject unbalanced or edited journals, and every amount uses exact decimals. A reconciliation job checks every account against the ledger every 15 minutes.
- **Money path:** every fill, fee, funding payment and payout runs as one command in a single transaction, with idempotency keys, per-account advisory locks and a transactional outbox.
- **Real-time:** a market-data ingest process streams order books and trades, and Socket.IO gateways push live P&L, margin and account updates to the trading terminal.
- **Admin backend:** accounts, breaches, a risk desk, KYC review and manual actions.
- **Tests:** race, crash and load suites run against real Postgres and Redis. They check rules such as "a cancel and a fill have exactly one winner".

`NestJS` `PostgreSQL` `Redis` `Socket.IO` `Drizzle ORM` `Next.js` `Prometheus` `PM2`

### Prop firm review & complaint platform: full-stack developer
Traders compare prop firms, file complaints and see how each firm responds. A public trust score reflects the outcomes.

- **Trust score engine:** three weighted pillars (credibility, trading conditions, payouts). Each upheld complaint deducts points, scaled by how much the firm has paid out, and every deduction is recorded so it can be reversed.
- **Complaint system:** a lifecycle with response deadlines, firm replies, moderator decisions and automatic resolution, plus two-level comments.
- **Abuse-resistant feed ranking:** hot and discovery scores. Votes are weighted by the voter's reputation and counted once per user, enforced by database constraints.
- **Role-based admin:** admin, moderator, editor and firm roles checked by shared guards, plus rate limiting, upload validation and an audit-log pipeline (Redis to PostgreSQL).

`Next.js` `MongoDB` `PostgreSQL` `Redis` `Clerk` `Jest`

> Full case studies: **[nirajkumar.dev/prop-firm-developer](https://nirajkumar.dev/prop-firm-developer)**

---

## 🚀 Tech Stack

### Backend
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![Socket.IO](https://img.shields.io/badge/Socket.IO-010101?style=flat-square&logo=socketdotio&logoColor=white)
![WebRTC](https://img.shields.io/badge/WebRTC-333333?style=flat-square&logo=webrtc&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

### Databases & ORMs
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Drizzle](https://img.shields.io/badge/Drizzle-C5F74F?style=flat-square&logo=drizzle&logoColor=black)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)

### Frontend
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Redux](https://img.shields.io/badge/Redux_Toolkit-764ABC?style=flat-square&logo=redux&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

### Tools & DevOps
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![PM2](https://img.shields.io/badge/PM2-2B037A?style=flat-square&logo=pm2&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=firebase&logoColor=black)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)

### Also
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Arduino](https://img.shields.io/badge/Arduino-00979D?style=flat-square&logo=arduino&logoColor=white)

---

## 📌 Open-Source Projects

| Project | What it is |
| --- | --- |
| [**smartCall**](https://github.com/itscyborg/smartCall) | One-to-one voice and video calling over WebRTC: a Next.js client and a Node signalling server on Socket.IO, with call sessions in MongoDB |
| [**oauth**](https://github.com/itscyborg/oauth) | A minimal OAuth 2.0 flow in Node: initiate, callback and token refresh |
| [**youtubeTranscriptSummarizer**](https://github.com/itscyborg/youtubeTranscriptSummarizer) | A Chrome extension that sends a YouTube video's transcript to a Python service and shows a summary |
| [**AirQualityMOnitoringSystem**](https://github.com/itscyborg/AirQualityMOnitoringSystem) | Air-quality monitoring on an ESP8266 with a DHT sensor, an OLED display and Blynk |

> The prop firm platforms and my client work live in private repositories. Case studies are on **[nirajkumar.dev](https://nirajkumar.dev)**.

---

## 📊 GitHub Stats

<div align="center">

<img height="160" src="https://github-readme-stats.vercel.app/api?username=itscyborg&show_icons=true&theme=default&hide_border=true&count_private=true" />
<img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=itscyborg&layout=compact&hide_border=true&theme=default" />

</div>

<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=itscyborg&hide_border=true" />
</div>

---

<div align="center">

*Building a prop firm or trading platform? Let's talk.*

</div>
