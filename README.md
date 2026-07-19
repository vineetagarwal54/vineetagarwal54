<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0,2,10,20,30&height=180&section=header&text=Vineet%20Agarwal&fontSize=52&fontColor=ffffff&animation=fadeIn&fontAlignY=36&desc=Software%20Engineer%20%7C%20AI%20Infrastructure%20%7C%20Cloud%20Backend&descSize=16&descAlignY=56" />

<a href="https://vineet-agarwal54.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" /></a>
<a href="https://www.linkedin.com/in/vineetagarwal54/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
<a href="mailto:vineetagarwal540@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
<a href="https://vineet-agarwal54.vercel.app/"><img src="https://img.shields.io/badge/Resume-2EA043?style=for-the-badge&logo=readdotcv&logoColor=white" /></a>

<br/>

<img src="https://img.shields.io/badge/Open%20to-Full--Time%20SWE%20%7C%20January%202027-2ea043?style=flat-square" />
<img src="https://img.shields.io/badge/MEng%20Software%20Engineering-University%20of%20Maryland-red?style=flat-square" />
<img src="https://img.shields.io/badge/Location-Washington%20DC%20Metro%20%2F%20Remote-58a6ff?style=flat-square" />

</div>

---

## About

I build backend and AI infrastructure systems, and I have been shipping production software for over three years, two of them full time before graduate school.

Most recently I worked on LLM inference: implementing speculative decoding from scratch, benchmarking vLLM, SGLang, and TensorRT-LLM against a 480B parameter model on Blackwell GPUs, and digging into why theoretical throughput gains disappear once a real serving loop is involved. Before that I spent two years on production web and mobile systems where the interesting problems were latency, query cost, and things breaking at 2am.

The through line is the same either way: understand the data path, find where the time actually goes, then build on top of it.

```
Full-Stack  ──▶  Cloud & Infra  ──▶  LLM Serving  ──▶  Applied AI Systems
     ▲                                                         │
     └──────────── measure it, then make it faster ◀───────────┘
```

**Currently:** Enterprise AI and Platform Intern at ServBeyond Solutions, building a retrieval pipeline over internal documentation that is now live for the team.
**Graduating:** December 2026, MEng Computer Software Engineering, University of Maryland College Park, with a Graduate Certificate in Cloud Engineering.

---

## LLM Inference and Serving

*Machine Learning and Inference Engineering Intern, Runara, April to May 2026*

| Focus | What I did |
| :--- | :--- |
| **Speculative decoding** | Implemented it from scratch across two GPUs in PyTorch and HuggingFace Transformers, using the probabilistic rejection sampling acceptance criterion from the original paper rather than naive argmax matching. Characterized the draft to target cost ratio under which the technique actually pays for itself. |
| **Acceptance rate debugging** | Traced a gap between 92 percent isolated draft agreement and 29 percent real in-loop acceptance down to KV cache and verification input handling, and showed argmax draft selection beats temperature sampling for acceptance. |
| **Framework benchmarking** | Compared vLLM, SGLang, and TensorRT-LLM serving Qwen3 Coder 480B on RTX PRO 6000 Blackwell GPUs, profiling time to first token, tokens per second, VRAM footprint, KV cache growth, and multi-user scaling. |
| **Quantization review** | Caught that the official FP8 checkpoint did not satisfy a 4-bit requirement and escalated it before GPU hours were spent on the wrong artifact. |

`PyTorch` `HuggingFace` `vLLM` `SGLang` `TensorRT-LLM` `KV cache` `FP8 / INT4 / AWQ` `RunPod` `Blackwell`

---

## Selected Projects

<table>
<tr>
<td width="50%" valign="top">

### [Job_Tracker](https://github.com/vineetagarwal54/Job_Tracker)
Desktop application for tracking job applications, built with React and Electron. One click capture from any job board through a browser bookmarklet, deadline tracking, drag and drop reordering, and JSON export and import.

Built it because spreadsheets kept losing my deadlines. Now has stars and forks from other people using it.

`React` `Electron` `JavaScript` `Local-first`

</td>
<td width="50%" valign="top">

### [RepoResearchAI](https://github.com/vineetagarwal54/RepoResearchAI)
Long running codebase analysis system. Specialized AutoGen agents (engineering, product, QA) work over a FAISS indexed repository to produce architecture insights, API documentation, and schema breakdowns.

Sessions are resumable, so analysis survives interruption on large repositories.

`Python` `AutoGen` `LangChain` `FAISS` `Multi-agent`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [CollabDrawAI](https://github.com/vineetagarwal54/CollabDrawAI)
Real time collaborative whiteboard in a Turborepo monorepo: Next.js frontend, Express API, dedicated WebSocket server, shared UI package, PostgreSQL with Prisma.

Room based sessions with live multi-user drawing and conflict-free cursor sync.

`TypeScript` `Next.js` `WebSocket` `PostgreSQL` `Prisma`

</td>
<td width="50%" valign="top">

### [MeetSpace](https://github.com/vineetagarwal54/MeetSpace)
Peer to peer video conferencing over WebRTC. Multi participant calls, screen sharing, in call chat, and recording with pause and resume.

React and TypeScript frontend, Node and Express signaling with Socket.IO and PeerJS.

`WebRTC` `TypeScript` `Socket.IO` `PeerJS` `Node.js`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [AIChatbot](https://github.com/vineetagarwal54/AIChatbot)
Domain specific customer support assistant with a RAG pipeline over business documentation, Redis response caching, and a hybrid backend that falls back from OpenAI to local Hugging Face models when the API is unavailable.

`Python` `FastAPI` `RAG` `Redis` `LangChain`

</td>
<td width="50%" valign="top">

### [google-adk](https://github.com/vineetagarwal54/google-adk)
Sandbox for agentic orchestration patterns with Google ADK: search agents, research and summarization chains, and sequential versus parallel agent execution compared side by side.

`Python` `Google ADK` `Agent orchestration`

</td>
</tr>
</table>

---

## Production Work

**Xelpmoc Design and Tech**, Software Developer, November 2022 to April 2024
Cut a critical query path from 75 seconds to under 10 seconds by restructuring joins, indexing high traffic tables, and layering Redis caching, roughly 4x throughput improvement. Built a WebRTC and Socket.IO interview platform sustaining 100 plus concurrent sessions under 200ms latency. Led architecture updates on a tourism platform that reduced production defects by 40 percent.

**Svipes**, Full Stack Developer, July 2024 to December 2024
Shipped 50 plus cross platform React Native screens with Redux Toolkit. Refactored the video module with asynchronous loading and caching, reducing playback stutter by up to 70 percent and load time by 1.3 seconds.

---

## Stack

**Languages**
<img src="https://skillicons.dev/icons?i=python,typescript,javascript,cpp,go&theme=dark" height="42" />
<img src="https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white" height="28" />

**AI and Inference**
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white" height="28" />
<img src="https://img.shields.io/badge/HuggingFace-FFD21E?style=flat&logo=huggingface&logoColor=black" height="28" />
<img src="https://img.shields.io/badge/vLLM-1C3A3A?style=flat" height="28" />
<img src="https://img.shields.io/badge/SGLang-4B0082?style=flat" height="28" />
<img src="https://img.shields.io/badge/TensorRT--LLM-76B900?style=flat&logo=nvidia&logoColor=white" height="28" />
<img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white" height="28" />
<img src="https://img.shields.io/badge/RAG-111827?style=flat" height="28" />
<img src="https://img.shields.io/badge/AutoGen-0081CB?style=flat&logo=microsoft&logoColor=white" height="28" />

**Backend and Data**
<img src="https://skillicons.dev/icons?i=fastapi,nodejs,express,postgres,mongodb,redis&theme=dark" height="42" />

**Cloud and Infra**
<img src="https://skillicons.dev/icons?i=aws,docker,kubernetes,githubactions,git,linux&theme=dark" height="42" />

**Frontend**
<img src="https://skillicons.dev/icons?i=react,nextjs,tailwind&theme=dark" height="42" />
<img src="https://img.shields.io/badge/React_Native-20232A?style=flat&logo=react&logoColor=61DAFB" height="28" />

---

## Snapshot

<div align="center">

<img height="150" src="https://github-readme-stats.vercel.app/api?username=vineetagarwal54&show_icons=true&count_private=true&hide_border=true&title_color=58A6FF&icon_color=58A6FF&text_color=c9d1d9&bg_color=0d1117" />
<img height="150" src="https://github-readme-stats.vercel.app/api/top-langs/?username=vineetagarwal54&layout=compact&hide_border=true&title_color=58A6FF&text_color=c9d1d9&bg_color=0d1117&langs_count=8" />

</div>

---

## How I work

I like systems that make sense, APIs that do not surprise you, and interfaces that guide instead of confuse. I would rather measure a bottleneck than guess at one, and I try to build things that survive past the first version.

If you are working on inference, backend infrastructure, or applied AI systems and want to build something together, reach out.

<div align="center">

<a href="https://vineet-agarwal54.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" /></a>
<a href="https://www.linkedin.com/in/vineetagarwal54/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
<a href="mailto:vineetagarwal540@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>

<sub><i>Build relentlessly. Ship quietly. Let the work speak.</i></sub>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0,2,10,20,30&height=100&section=footer" />

</div>
