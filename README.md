<h1 align="center">Le Hoang An &nbsp;·&nbsp; Lucas</h1>

<p align="center">
  <sub>
    <b>DISTRIBUTED SYSTEMS</b> &nbsp;&nbsp;<b>EVENT-DRIVEN ARCHITECTURE</b> &nbsp;&nbsp;<b>REAL-TIME DATA PIPELINES</b>
  </sub>
</p>

<p align="center">
  <i>Fullstack product builder. I design backends that stay up when the data doesn't cooperate.</i>
</p>

<p align="center">
  <a href="mailto:lean09062@gmail.com"><img src="https://img.shields.io/badge/Email-0D1117?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://drive.google.com/file/d/1YlzL3PkEEYn0Z7Ca0eY7St0kjd3jB5GA/view?usp=sharing"><img src="https://img.shields.io/badge/Résumé-0D1117?style=flat-square&logo=readdotcv&logoColor=white" alt="Résumé" /></a>
  <a href="https://github.com/lucasngucii?tab=repositories"><img src="https://img.shields.io/badge/Repositories-0D1117?style=flat-square&logo=github&logoColor=white" alt="Repositories" /></a>
</p>

<br />

---

<h2 align="center">Open Source</h2>

<p align="center">
  <sub>WHAT I BUILD WHEN NOBODY ASSIGNS IT TO ME</sub>
</p>

<br />

<h3 align="center">
  🛡️ &nbsp;<a href="https://github.com/lucasngucii/Argus">Argus</a>
</h3>

<p align="center">
  <b>A local-first governance gate for AI coding agents.</b><br />
  <sub>Every command an agent tries to run gets parsed, scored, and answered — <code>allow</code> / <code>ask</code> / <code>deny</code>.</sub>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Go-0D1117?style=flat-square&logo=go&logoColor=white" alt="Go" />
  <img src="https://img.shields.io/badge/SQLite-0D1117?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite" />
  <img src="https://img.shields.io/badge/MIT-0D1117?style=flat-square" alt="MIT" />
  <img src="https://img.shields.io/github/stars/lucasngucii/Argus?style=flat-square&color=0D1117&labelColor=0D1117" alt="Stars" />
</p>

```console
$ argus explain 'X=rm; $X -rf /'

  parsed argv     rm -rf /
  obfuscation     variable indirection  →  escalated
  matched rule    rm-recursive-root  (floor)
  severity        high
  verdict         deny
  logged          ~/.argus/argus.db
```

Deny-lists pattern-match a raw string, then throw the answer away. Argus parses the command into a
real AST — so `X=rm; $X -rf /` and `rm$IFS-rf$IFS/` collapse to the same `argv` — grades it on a
four-level severity scale, and writes every decision to a local SQLite store you can query, explain,
and replay against a candidate policy before you adopt it.

> [!IMPORTANT]
> Catastrophic commands are denied in **every** permission mode — including
> `--dangerously-skip-permissions` — and no policy rule or allow-list entry can downgrade them.
> On a parse error the gate escalates rather than letting the command through.

<br />

<table>
<tr>
<td width="50%" valign="top">

<h3>🧠 <a href="https://github.com/lucasngucii/face-detection">face-detection</a></h3>

<p><b>Real-time attention monitoring from a plain webcam.</b> No headset, no eye tracker, no specialized hardware.</p>

<p>MTCNN → MediaPipe landmarks → six geometric features → classifier, benchmarked across Random Forest, SVM, and an MLP.</p>

<p><code>92.1% accuracy</code> &nbsp; <code>~32 FPS</code></p>

<p>
<img src="https://img.shields.io/badge/Python-0D1117?style=flat-square&logo=python&logoColor=white" alt="Python" />
<img src="https://img.shields.io/badge/scikit--learn-0D1117?style=flat-square&logo=scikitlearn&logoColor=white" alt="scikit-learn" />
</p>

</td>
<td width="50%" valign="top">

<h3>🦉 <a href="https://github.com/diepnghitinh/clickhouse-owl">clickhouse-owl</a></h3>

<p><b>An admin console for ClickHouse that doesn't feel like 2011.</b> <sub>— contributor</sub></p>

<p>Tabbed SQL editor with natural-language query generation, <code>EXPLAIN PLAN</code> visualization, and a visual table builder.</p>

<p><code>Next.js 14</code> &nbsp; <code>Monaco</code> &nbsp; <code>Vercel AI SDK</code></p>

<p>
<img src="https://img.shields.io/badge/TypeScript-0D1117?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
<img src="https://img.shields.io/badge/ClickHouse-0D1117?style=flat-square&logo=clickhouse&logoColor=white" alt="ClickHouse" />
</p>

</td>
</tr>
</table>

---

<h2 align="center">At Work</h2>

<br />

- **LinkAdz** — led end-to-end backend design for a multi-channel adtech platform processing high-volume campaign data in near real-time.
- **Uniscore** — architected the real-time data pipeline behind a product serving **1M+ users**.
- Built event-driven systems that hold up under traffic spikes, dirty upstream data, and third-party API failures.

**The shape I keep coming back to** — one path answers the user, the other one does the work.

```
 REQUEST PATH · synchronous, latency is the constraint
 ─────────────────────────────────────────────────────
   browser  ─▶  Next.js  ─▶  NestJS  ─┬─▶  PostgreSQL     source of truth
                                      └─▶  Redis          cache · sessions


 EVENT PATH · asynchronous, durability is the constraint
 ─────────────────────────────────────────────────────
   NestJS  ─▶  Kafka  ─┬─▶  Go ingester  ─▶  ClickHouse   analytics
                       └─▶  BullMQ jobs  ─▶  Elasticsearch  search
```

<sub>
The write side stays boring and consistent. Read models are rebuilt from the event log, so a bad
projection is a replay, not an outage. Services get extracted only where the scale profile actually
differs — everything else stays a modular monolith.<br /><br />
Also: <b>Python</b> (LightGBM / XGBoost) &nbsp;·&nbsp; <b>RabbitMQ</b> &nbsp;·&nbsp; <b>MongoDB</b> &nbsp;·&nbsp; <b>AWS</b> &nbsp;·&nbsp; <b>Docker Swarm</b>
</sub>

---

<p align="center">
  <img height="150" src="https://github-readme-stats-eight-theta.vercel.app/api?username=lucasngucii&show_icons=true&hide_border=true&bg_color=00000000&include_all_commits=true&count_private=true&hide_title=true" alt="GitHub statistics" />
  <img height="150" src="https://github-readme-stats-eight-theta.vercel.app/api/top-langs/?username=lucasngucii&layout=compact&langs_count=6&hide_border=true&bg_color=00000000&hide_title=true" alt="Most used languages" />
</p>

<p align="center">
  <sub><a href="mailto:lean09062@gmail.com">lean09062@gmail.com</a></sub>
</p>
