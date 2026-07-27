<h1 align="center">Le Hoang An &nbsp;·&nbsp; Lucas</h1>

<p align="center">
  <sub>
    <b>SOFTWARE ENGINEERING</b> &nbsp;&nbsp;<b>EVENT-DRIVEN SYSTEMS</b> &nbsp;&nbsp;<b>SYSTEM DESIGN</b>
  </sub>
</p>

<p align="center">
  <i>Fullstack product builder. Mostly backend, mostly distributed systems.</i>
</p>

<p align="center">
  <a href="mailto:lean09062@gmail.com"><img src="https://img.shields.io/badge/Email-0D1117?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://drive.google.com/file/d/1YlzL3PkEEYn0Z7Ca0eY7St0kjd3jB5GA/view?usp=sharing"><img src="https://img.shields.io/badge/Résumé-0D1117?style=flat-square&logo=readdotcv&logoColor=white" alt="Résumé" /></a>
  <a href="https://github.com/lucasngucii?tab=repositories"><img src="https://img.shields.io/badge/Repositories-0D1117?style=flat-square&logo=github&logoColor=white" alt="Repositories" /></a>
</p>

<br />

---

### About

Four years building products end to end — backend architecture, real-time pipelines, and the UI on top of them.

- **Limzy** — backend design for a multi-channel adtech platform handling campaign data in near real-time.
- **Uniscore** — real-time data pipeline for a product serving around 1M users.
- Comfortable with the messy parts: traffic spikes, unreliable upstream data, third-party API failures.

I like joining products early and staying accountable for how they behave in production.

---

### Open Source

A few things I work on outside of client work.

| Project | What it does | Stack |
| :--- | :--- | :--- |
| **[Argus](https://github.com/lucasngucii/Argus)** <br /><sub>v0.1 · alpha</sub> | A local-first gate for AI coding agents. Parses each command into an AST, scores it by severity, and returns allow / ask / deny. Decisions are stored locally so they can be explained and replayed. | `Go` `SQLite` |
| **[face-detection](https://github.com/lucasngucii/face-detection)** | Attention monitoring from a webcam — MTCNN for detection, MediaPipe landmarks, six geometric features, then a classifier. Around 92% accuracy at ~32 FPS. | `Python` `scikit-learn` |
| **[clickhouse-owl](https://github.com/diepnghitinh/clickhouse-owl)** <br /><sub>contributor</sub> | Web admin console for ClickHouse — tabbed SQL editor, natural-language query generation, visual table builder. | `Next.js` `TypeScript` |

---

### End to End

The layers I've owned on production systems, and what I reach for at each.

| Layer | What that means in practice | Tools |
| :--- | :--- | :--- |
| **Product** | Scoping, tradeoffs, deciding what not to build yet | — |
| **Interface** | App architecture, server components, state, design system | `Next.js` `TypeScript` |
| **API** | Service boundaries, contracts, auth, versioning against third-party APIs | `NestJS` `Node.js` |
| **Domain** | DDD modeling, CQRS, transactional consistency, migrations | `PostgreSQL` `Redis` `MongoDB` |
| **Events** | Async workflows, retries, idempotency, outbox and saga patterns | `Kafka` `RabbitMQ` `BullMQ` |
| **Analytics** | Ingestion, read models, search, ML on top of the pipeline | `Go` `ClickHouse` `Elasticsearch` `Python` |
| **Operations** | Deploys, observability, on-call, incident response | `AWS` `Docker Swarm` |

<sub>
Read models are rebuilt from the event log, so a bad projection is a replay rather than an outage.
Services get extracted only where the scale profile actually differs — the rest stays a modular monolith.
</sub>

---

<p align="center">
  <img height="150" src="https://github-readme-stats-eight-theta.vercel.app/api?username=lucasngucii&show_icons=true&hide_border=true&bg_color=00000000&include_all_commits=true&count_private=true&hide_title=true" alt="GitHub statistics" />
  <img height="150" src="https://github-readme-stats-eight-theta.vercel.app/api/top-langs/?username=lucasngucii&layout=compact&langs_count=6&hide_border=true&bg_color=00000000&hide_title=true" alt="Most used languages" />
</p>

<p align="center">
  <sub><a href="mailto:lean09062@gmail.com">lean09062@gmail.com</a></sub>
</p>
