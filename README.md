<div align="center">

# Hi, I'm Harman

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=58A6FF&center=true&vCenter=true&width=600&lines=Backend+Engineer;Distributed+Systems+%26+Cloud+Infrastructure;Applied+GenAI+%C2%B7+Currently+building+Lyra;Contributing+to+Meshery+(CNCF)" alt="Typing intro" />

**Final-year Computing Science student @ University of Alberta**
Google Maps Platform Hackathon 2025 · Jury Award & Fan Favorite

<a href="https://harman-io.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-0A0A0A?style=for-the-badge&logo=googlechrome&logoColor=white" /></a>
<a href="https://www.linkedin.com/in/harmanp01"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
<a href="mailto:harmanbofficial@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>

</div>

---

## About Me

I'm a computer science student who fell in love with the backend side of things. I started out chasing UI work like most people, but I got far more interested in how systems actually talk to each other: **request routing, load handling, caching and the networking layer underneath it all.**

I still build full stack when a project needs it, but hand me a codebase and I'll go to the server and the architecture diagram before I touch the CSS. Lately I've been going deep on **generative AI**: not just calling an API, but understanding how models, retrieval and prompt design fit into a real application.


**Open to:** Summer 2027 SWE internships · Backend, distributed systems & cloud infrastructure roles · Open source · GenAI / LLM projects

---

## Experience

### Open Source Contributor · [Meshery](https://github.com/meshery) (CNCF)
*Currently contributing*

Meshery is a cloud-native manager for designing and operating **Kubernetes** infrastructure and the apps that run on it. After my time on Volcano I moved over to Meshery, and I'm currently getting to know the codebase and picking up issues.

**Stack:** Go · Kubernetes · React · Cloud-Native Infrastructure

### Open Source Contributor · [Volcano-sh](https://github.com/volcano-sh) (CNCF)
*Jan 2026 – 2026*

Volcano is a cloud-native batch scheduler that runs AI/ML and HPC workloads on **Kubernetes**. I joined to learn how real cloud infrastructure works at scale, and I've had multiple **Go** PRs merged on reliability and testing.

**Stack:** Go · Kubernetes · Redis · Distributed Systems · E2E Testing

### Software Developer Intern · La Connexional
*Jan 2026 – Apr 2026*

Worked on the backend of **UNTAPPED**, a production platform used by **500+ people across Alberta**. Built APIs for OAuth sign-in, password reset, profiles, invoicing and idempotent Stripe payments, added event hooks and scheduled reminders, and shipped releases through Docker and CI/CD.

**Stack:** REST APIs · OAuth · Stripe · Docker · CI/CD

---

## Tech Stack

<table>
  <tr>
    <td align="center"><b>Languages</b></td>
    <td><img src="https://skillicons.dev/icons?i=java,cpp,go,python,cs,ts,js" /></td>
  </tr>
  <tr>
    <td align="center"><b>Backend & Data</b></td>
    <td><img src="https://skillicons.dev/icons?i=spring,dotnet,nodejs,postgres,mongodb,redis" /></td>
  </tr>
  <tr>
    <td align="center"><b>Cloud & DevOps</b></td>
    <td><img src="https://skillicons.dev/icons?i=kubernetes,docker,aws,azure,firebase,linux" /></td>
  </tr>
  <tr>
    <td align="center"><b>Frontend</b></td>
    <td><img src="https://skillicons.dev/icons?i=react,nextjs,tailwind" /></td>
  </tr>
</table>

---

## Featured Projects

| Project | What it is | Built with |
|---|---|---|
| **[ArenaNet](https://github.com/harmanD-MAX/ArenaNet)** | Real-time multiplayer game backend | C++20 · Asio · PostgreSQL · Redis |
| **[Lyra](https://github.com/harmanD-MAX/Lyra)** | AI vocal studio *(in progress)* | Python · Diffusion models · Cloudflare |
| **[Blueprint](https://github.com/harmanD-MAX/Blueprint)** | AI repository analyzer | C# · .NET 10 · React · Gemini |
| **[TripWise](https://github.com/harmanD-MAX/TripWise)** | AI travel planner | Java · Spring Boot · Next.js · AWS |
| **[GeoScope](https://github.com/harmanD-MAX/GeoScope)** | Location intelligence platform | Next.js · Google Maps Platform |
| **[Mood Tracker](https://github.com/cmput301-w25/project-team_16)** | Android social app | Java · Android · Firebase |

<sub>Click a project below to see how it works.</sub>

<details>
<summary><b>ArenaNet: Multiplayer Game Backend</b></summary>
<br>

A C++20 backend built to plug straight into Unity or Godot. It handles login, friends, parties, custom lobbies and full matchmaking. Networking runs on **Asio async TCP** with a small custom protocol (4-byte length header + JSON payload).

| | |
|---|---|
| **Stack** | C++20, Asio, PostgreSQL, Redis, C# SDK |
| **Concurrency** | Lobbies, parties and matchmaking queues held in memory with mutex-protected shared state |
| **Matchmaking** | Background thread runs every second, widening the ELO range the longer someone waits |
| **Reliability** | Redis-backed auth tokens, host-only lobby controls, 30-second reconnect grace period |
| **Data** | PostgreSQL for accounts, friends, match history and leaderboards (window functions); Redis for presence and temp tokens |

Started as *"how hard can matchmaking really be"* and turned into one of the bigger things I've built. Solo players, parties and "Any" wildcard opponents all get grouped correctly by match size. I also wrote a Python GUI client to test several "players" at once, plus a C# SDK so it drops straight into a real Unity project.

</details>

<details>
<summary><b>Lyra: AI Vocal Studio (in progress)</b></summary>
<br>

Sing a take over any song and Lyra corrects your pitch and timing, then renders it in **your own trained voice**. Every render exports studio stems and a MIDI file.

| | |
|---|---|
| **Stack** | Python, Firebase Auth, Cloudflare D1, Cloudflare R2 |
| **AI Models** | Seed-VC (diffusion transformer + Whisper + BigVGAN, 44.1 kHz) and RVC v2, with automatic engine selection per voice |
| **Audio Pipeline** | Source separation, pitch and timing correction, stems and MIDI export |
| **Voice Lab** | Record or upload your voice in the browser and train with Quick, Standard or Best presets |
| **Infrastructure** | Lite mode auto-detects low-RAM/low-disk machines (~0.6 GB of models vs ~2.7 GB); runs locally or on Colab/Kaggle |

The hard part isn't calling a model. It's making a multi-model audio pipeline run reliably on very different machines, and keeping each user's songs and voices tied to their Google account.

</details>

<details>
<summary><b>Blueprint: AI Repository Analyzer</b></summary>
<br>

Paste in any GitHub repo URL and get a full architectural breakdown: dependency graphs, technical debt audits, REST endpoint discovery and AI-generated docs.

| | |
|---|---|
| **Stack** | C#, .NET 10, ASP.NET Core, React 19, TypeScript, Gemini, Astra DB, SignalR, Hangfire, Azure |
| **Analysis** | Clones repos with LibGit2Sharp and detects REST endpoints across ASP.NET Core, Spring Boot, Express, Flask and FastAPI |
| **Real-time** | Streams live analysis progress to the browser over SignalR |
| **Background Jobs** | Long-running analyses run through Hangfire so the API stays responsive |
| **Visualization** | Interactive dependency graph (Cytoscape.js) and a built-in Monaco code viewer |

Built because I kept wanting a faster way to understand a codebase before diving in. The technical debt checker flags large files (500+ lines) and leftover TODO/FIXME comments.

</details>

<details>
<summary><b>TripWise: AI Travel Planner</b></summary>
<br>

Give it a budget, destination and travel style, and it builds a full day-by-day itinerary.

| | |
|---|---|
| **Stack** | Java, Spring Boot 3, Spring Security (JWT), Spring AI, Next.js 16, React 19, PostgreSQL (Supabase), Clerk |
| **AI Features** | Gemini generates itineraries, predicts budgets, powers a travel assistant and writes trip intelligence reports |
| **Routing** | Orders each day's stops with a TSP algorithm over the OSRM API |
| **Security** | Clerk auth, JWT-secured Spring Boot APIs, role-based endpoint protection |
| **Infrastructure** | Frontend on AWS Amplify, backend on AWS EC2, media streamed to Amazon S3 |

</details>

<details>
<summary><b>GeoScope: Location Intelligence Platform</b></summary>
<br>

> **Jury Award & Fan Favorite (Finance), Google Maps Platform Hackathon 2025**

Scores commercial locations with a "GeoScore" built from foot traffic, safety, competition and transit access, to help with lending and business decisions.

| | |
|---|---|
| **Stack** | Next.js 14, TypeScript, Google Maps Platform APIs, Three.js, Tailwind CSS |
| **Features** | Location scoring, 3D map visualizations and hourly traffic trends |

</details>

<details>
<summary><b>Mood Tracker: Android Social App</b></summary>
<br>

University team project (CMPUT 301) for tracking emotional well-being, with location-tagged mood logs, a "time machine" history view, maps and a social feed.

| | |
|---|---|
| **Stack** | Java, Android Studio, Firebase, Google Maps API, Spotify API |
| **Features** | Real-time sync, mood history, maps and a friends feed |

</details>

---

<div align="center">

<sub>Thanks for stopping by.</sub>

</div>
