<h1 align="center">Le Hoang An — Lucas</h1>

<p align="center">
  <sub>
    <b>DISTRIBUTED SYSTEMS</b> &nbsp;·&nbsp;
    <b>EVENT-DRIVEN ARCHITECTURE</b> &nbsp;·&nbsp;
    <b>REAL-TIME DATA PIPELINES</b>
  </sub>
</p>

<p align="center">
  Fullstack product builder. I design backends that stay up when the data doesn't cooperate.
</p>

<p align="center">
  <a href="mailto:lean09062@gmail.com">
    <img src="https://img.shields.io/badge/Email-0D1117?style=flat-square&logo=gmail&logoColor=white" alt="Email" />
  </a>
  <a href="https://drive.google.com/file/d/1YlzL3PkEEYn0Z7Ca0eY7St0kjd3jB5GA/view?usp=sharing">
    <img src="https://img.shields.io/badge/Résumé-0D1117?style=flat-square&logo=readdotcv&logoColor=white" alt="Résumé" />
  </a>
  <a href="https://github.com/lucasngucii?tab=repositories">
    <img src="https://img.shields.io/badge/Repositories-0D1117?style=flat-square&logo=github&logoColor=white" alt="Repositories" />
  </a>
</p>

---

### What I've shipped

- **Limzy** — led end-to-end backend design for a multi-channel adtech platform processing high-volume campaign data in near real-time.
- **Uniscore** — architected the real-time data pipeline behind a product serving **1M+ users**.
- Built event-driven systems that hold up under traffic spikes, dirty upstream data, and third-party API failures.

I like joining products early, owning the technical design, and staying accountable for what it does in production.

---

### How I build

```
 client ──▶ Next.js ──▶ NestJS ──┬──▶ PostgreSQL · Redis
                                 │       write model
                                 │
                                 └──▶ Kafka ──▶ Go · BullMQ
                                                    │
                                     ClickHouse · Elasticsearch
                                             read model
```

<sub>
CQRS &amp; DDD over a modular monolith, extracted into services only where the scale profile actually differs.
Also: <b>Python</b> (LightGBM / XGBoost), <b>RabbitMQ</b>, <b>MongoDB</b>, <b>AWS</b>, <b>Docker Swarm</b>.
</sub>

---

### Open source

**[Argus](https://github.com/lucasngucii/Argus)** &nbsp;<img src="https://img.shields.io/badge/Go-0D1117?style=flat-square&logo=go&logoColor=white" align="center" />
A local-first governance gate for AI coding agents. Every shell command an agent runs is parsed into a real AST, scored by severity, and answered with **allow / ask / deny** — then written to a local SQLite store you can query and replay. Fail-closed, with a catastrophic-command floor that no policy can downgrade.

**[face-detection](https://github.com/lucasngucii/face-detection)** &nbsp;<img src="https://img.shields.io/badge/Python-0D1117?style=flat-square&logo=python&logoColor=white" align="center" />
Real-time attention monitoring from a plain webcam. MTCNN → MediaPipe landmarks → six geometric features → classifier. **92.1% accuracy at ~32 FPS**, no specialized hardware.

**[clickhouse-owl](https://github.com/diepnghitinh/clickhouse-owl)** &nbsp;<img src="https://img.shields.io/badge/TypeScript-0D1117?style=flat-square&logo=typescript&logoColor=white" align="center" /> &nbsp;<sub>contributor</sub>
An admin console for ClickHouse — tabbed SQL editor, natural-language query generation, and a visual table builder.

---

<p align="center">
  <img
    height="150"
    src="https://github-readme-stats-eight-theta.vercel.app/api?username=lucasngucii&show_icons=true&hide_border=true&bg_color=00000000&include_all_commits=true&count_private=true&hide_title=true"
    alt="GitHub statistics"
  />
  <img
    height="150"
    src="https://github-readme-stats-eight-theta.vercel.app/api/top-langs/?username=lucasngucii&layout=compact&langs_count=6&hide_border=true&bg_color=00000000&hide_title=true"
    alt="Most used languages"
  />
</p>
