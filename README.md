<!-- ============================================================
     Jorge "Yorch" Peraza — GitHub Profile README
     Staff / Founding Engineer · AI Platform & Developer Tools
============================================================= -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0B1020,50:5B21B6,100:0EA5E9&height=220&section=header&text=Jorge%20Peraza&fontSize=58&fontColor=FFFFFF&fontAlignY=38&desc=Staff%20%2F%20Founding%20Engineer%20%C2%B7%20AI%20Platform%20%26%20Developer%20Tools&descSize=18&descAlignY=58&animation=fadeIn" alt="Jorge Peraza" width="100%" />
</p>

<p align="center">
  <a href="https://github.com/yorchperaza">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=3200&pause=900&color=A78BFA&center=true&vCenter=true&width=760&lines=Building+MonkeysCode+%E2%80%94+an+agentic+coding+IDE;Serving+Capuchin+on+my+own+H100%2FH200+GPU+stack;92.7%25+of+production+requests+served+in-house;Go+%C2%B7+TypeScript+%C2%B7+Python+%C2%B7+PHP+%E2%80%94+20%2B+years+in+production" alt="Typing intro" />
  </a>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/jorgeperaza/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-jorgeperaza-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="https://dev.to/yorchperaza"><img alt="Dev.to" src="https://img.shields.io/badge/Dev.to-yorchperaza-0A0A0A?style=for-the-badge&logo=devdotto&logoColor=white" /></a>
  <img alt="Location" src="https://img.shields.io/badge/Denver,%20CO-1E293B?style=for-the-badge&logo=googlemaps&logoColor=white" />
  <img alt="Profile views" src="https://komarev.com/ghpvc/?username=yorchperaza&style=for-the-badge&color=8B5CF6&label=PROFILE+VIEWS" />
</p>

---

## 🐒 About me

I build **AI products and the infrastructure they run on** — from the agent runtime a developer touches, down to the GPU node serving the model.

Founder & Principal Engineer at **MonkeysCloud**, where I created **MonkeysCode** (an agentic coding IDE) and **Capuchin** (the in‑house coding model behind it). Twenty years of production systems across Python, TypeScript, Go and PHP, with hands‑on depth in **GPU model serving**, **quota & admission control**, and **RL fine‑tuning**. I'm most at home owning an ambiguous product from zero to production — and running it afterward.

<table>
  <tr>
    <td align="center" width="25%"><h2>92.7%</h2><sub>production requests served<br/>on in‑house infra</sub></td>
    <td align="center" width="25%"><h2>~6×</h2><sub>target cost advantage vs.<br/>reseller‑model competitors</sub></td>
    <td align="center" width="25%"><h2>~7,000</h2><sub>concurrent users<br/>per GPU node</sub></td>
    <td align="center" width="25%"><h2>20+</h2><sub>years shipping<br/>production systems</sub></td>
  </tr>
</table>

---

## 🚀 Flagship — MonkeysCode × Capuchin

> An agentic coding IDE competing with Cursor and Claude Code, powered by a model and serving stack I designed, sized and operate.

<table>
  <tr>
    <td width="50%" valign="top">
      <h4>🧠 Product surface</h4>
      <ul>
        <li><b>capuchin-core</b> — shared TypeScript agent runtime: tool‑calling loops, verification layer</li>
        <li><b>mcode CLI</b> — TypeScript / Ink, compiled with Bun</li>
        <li><b>Troop</b> — multi‑agent desktop orchestrator (Electron)</li>
        <li><b>Org API keys</b> — HMAC‑SHA‑256, audited, rate‑limited, for CI/CD & integrations</li>
      </ul>
    </td>
    <td width="50%" valign="top">
      <h4>⚙️ Infrastructure</h4>
      <ul>
        <li><b>GPU serving</b> — committed H100/H200 on GKE with SGLang, cold‑start elimination</li>
        <li><b>Go quota & admission proxy</b> — dual‑pool per‑model quotas, rolling burst + weekly governors, 9 packaging tiers</li>
        <li><b>Cost‑aware routing</b> — two‑mode model (fast completion / budgeted reasoning) with task‑based routing</li>
        <li><b>RL pipeline</b> — GRPO/DPO on real usage trajectories, rewarded by test‑pass & edit‑persistence</li>
      </ul>
    </td>
  </tr>
</table>

```mermaid
flowchart LR
    subgraph Clients
        IDE[MonkeysCode IDE]
        CLI[mcode CLI]
        TROOP[Troop · multi-agent]
    end

    IDE & CLI & TROOP --> CORE[capuchin-core<br/>agent runtime]
    CORE --> PROXY[Go quota &<br/>admission proxy]
    PROXY --> ROUTER{cost-aware<br/>router}
    ROUTER -->|92.7%| CAP[Capuchin<br/>SGLang · H100/H200 · GKE]
    ROUTER -->|7.3%| FRONTIER[Frontier providers]
    CAP -. trajectories .-> RL[RL fine-tuning<br/>GRPO / DPO]
    RL -. new weights .-> CAP

    classDef core fill:#5B21B6,stroke:#A78BFA,color:#fff
    classDef infra fill:#0C4A6E,stroke:#38BDF8,color:#fff
    classDef ext fill:#1E293B,stroke:#64748B,color:#CBD5E1
    class CORE,PROXY,ROUTER core
    class CAP,RL infra
    class FRONTIER,IDE,CLI,TROOP ext
```

---

## 🧩 The MonkeysCloud ecosystem

|     | Project                | What it is                                                                                                              |
| :-: | :--------------------- | :---------------------------------------------------------------------------------------------------------------------- |
| 🐒  | **MonkeysCode**        | Agentic coding IDE, CLI and multi‑agent orchestrator                                                                    |
| 🧠  | **Capuchin**           | In‑house coding model + serving stack — fast & reasoning modes, automatic routing                                       |
| ⚡  | **MonkeysAI**          | Self‑hosted inference platform on open‑weight models (Llama, DeepSeek, large MoE) via vLLM, OpenAI‑compatible endpoints |
| 🛡️  | **MonkeysLegion**      | Modular PHP 8.4 framework — 29+ packages, PHPStan level 9, production‑ready skeleton                                    |
| 🔮  | **MonkeysLegion Apex** | AI orchestration for PHP 8.4+ — provider abstraction, model routing, fallback strategies                                |
| ☁️  | **MonkeysCloud**       | Developer platform — Git APIs, repo automation, provisioning, deploy triggers, CI/CD                                    |
| ✉️  | **MonkeysMail**        | Transactional email infrastructure — Postfix/OpenDKIM, Redis streams, tracking dashboard                                |

---

## 🛠️ Tech stack

<h4 align="center">AI / ML infrastructure</h4>
<p align="center">
  <img src="https://img.shields.io/badge/SGLang-111827?style=flat-square&logoColor=white" />
  <img src="https://img.shields.io/badge/vLLM-111827?style=flat-square" />
  <img src="https://img.shields.io/badge/OpenAI--compatible%20APIs-111827?style=flat-square&logo=openai&logoColor=white" />
  <img src="https://img.shields.io/badge/Agentic%20runtimes-5B21B6?style=flat-square" />
  <img src="https://img.shields.io/badge/Tool%20calling-5B21B6?style=flat-square" />
  <img src="https://img.shields.io/badge/RAG%20%26%20Embeddings-5B21B6?style=flat-square" />
  <img src="https://img.shields.io/badge/Model%20routing-0C4A6E?style=flat-square" />
  <img src="https://img.shields.io/badge/GPU%20scheduling-0C4A6E?style=flat-square&logo=nvidia&logoColor=76B900" />
  <img src="https://img.shields.io/badge/LoRA%20%2F%20QLoRA-0C4A6E?style=flat-square" />
  <img src="https://img.shields.io/badge/RL%20%C2%B7%20GRPO%20%2F%20DPO-0C4A6E?style=flat-square" />
</p>

<h4 align="center">Languages</h4>
<p align="center">
  <img src="https://skillicons.dev/icons?i=py,ts,go,js,php,bash&theme=dark" />
</p>

<h4 align="center">Cloud, infrastructure & data</h4>
<p align="center">
  <img src="https://skillicons.dev/icons?i=gcp,aws,kubernetes,docker,terraform,linux,nginx,postgres,redis,mongodb,elasticsearch&theme=dark" />
</p>

<h4 align="center">Apps & frameworks</h4>
<p align="center">
  <img src="https://skillicons.dev/icons?i=nodejs,bun,react,nextjs,electron,graphql,symfony&theme=dark" />
  <img src="https://img.shields.io/badge/Drupal-0678BE?style=for-the-badge&logo=drupal&logoColor=white" height="48" />
</p>

<details>
  <summary><b>Reliability & security</b></summary>
  <br/>

- **Reliability** — p50/p95/p99 latency discipline, structured logging, metrics, health & startup probes, dashboards, alerting, capacity planning, incident triage, cost attribution
- **Security** — secrets management, access control, service isolation, TLS, zero‑trust patterns, audit trails, SOC 2 & GDPR readiness
- **Currently learning** — Rust 🦀
</details>

---

## 🧭 Experience

| Role                                  | Company                                                     | When           |
| :------------------------------------ | :---------------------------------------------------------- | :------------- |
| **Founder & Principal Engineer**      | MonkeysCloud · Denver, CO                                   | 2019 – present |
| Senior Full‑Stack / Platform Engineer | Tesla                                                       | 2023 – 2024    |
| Senior Symfony Developer, Full Stack  | Cidi Labs                                                   | 2021 – 2023    |
| Senior Software Engineer & Consultant | Enterprise projects · Costa Rica / US (incl. Gorilla Logic) | 2002 – 2021    |

🎓 Computer Software Engineering — ULACIT, Costa Rica

---

## 💬 Talk to me about

`LLM serving` · `GPU capacity planning` · `agentic runtimes` · `quota & admission control` · `RL fine‑tuning` · `modular PHP 8.4 architecture` · `developer platforms`

---

## 📊 GitHub activity

<p align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=yorchperaza&show_icons=true&hide_border=true&include_all_commits=true&count_private=true&bg_color=0D1117&title_color=A78BFA&icon_color=38BDF8&text_color=C9D1D9&ring_color=8B5CF6" alt="GitHub stats" />
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=yorchperaza&layout=compact&hide_border=true&langs_count=8&bg_color=0D1117&title_color=A78BFA&text_color=C9D1D9" alt="Top languages" />
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=yorchperaza&hide_border=true&background=0D1117&ring=8B5CF6&fire=38BDF8&currStreakLabel=A78BFA&sideLabels=C9D1D9&currStreakNum=FFFFFF&sideNums=FFFFFF&dates=64748B" alt="GitHub streak" />
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0EA5E9,50:5B21B6,100:0B1020&height=120&section=footer" width="100%" />
</p>
