<div align="center">

![Header Banner](https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:134e4a,100:0e7490&height=250&section=header&text=Harman%&fontSize=60&fontColor=c9d1d9&animation=fadeIn&fontAlignY=38&desc=Backend%20%7C%20Distributed%20Systems%20%7C%20Gen%20AI%20%7C%20Full%20Stack&descAlignY=55&descSize=18)

![Student](https://img.shields.io/badge/Computer%20Science-Student-1e293b?style=for-the-badge&logo=googlescholar&logoColor=2dd4bf)
![Location](https://img.shields.io/badge/Location-Edmonton,%20Canada-0f172a?style=for-the-badge&logo=googlemaps&logoColor=38bdf8)

<br/>

<a href="https://www.instagram.com/harmn.in/?hl=en"><img src="https://img.shields.io/badge/Instagram-164e63?style=for-the-badge&logo=instagram&logoColor=38bdf8"/></a>
<a href="https://linkedin.com/in/harmanp1"><img src="https://img.shields.io/badge/LinkedIn-0e7490?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="mailto:harmanofficial@protonmail.com"><img src="https://img.shields.io/badge/Email-155e75?style=for-the-badge&logo=protonmail&logoColor=white"/></a>
<a href="https://leetcode.com/u/aQDiQitVpg/"><img src="https://img.shields.io/badge/LeetCode-0e7490?style=for-the-badge&logo=leetcode&logoColor=white"/></a>

</div>

---

## About Me

I'm a computer science student who ended up falling in love with the backend side of things. Most people start out chasing UI work, and I did too for a while, but somewhere along the way I got a lot more interested in how systems actually talk to each other — request routing, load handling, caching, the networking layer underneath it all. That's where I spend most of my time now.

I still build full stack when a project needs it, but if you hand me a codebase, I'll gravitate toward the server and the architecture diagram before I touch the CSS. Lately I've also been spending a lot of time exploring generative AI — not just calling an API and calling it a day, but actually understanding how retrieval, embeddings, and prompt design fit into a real application.

I don't have industry experience yet — I'm still a student — but I learn by building, breaking things, and rebuilding them properly the second time around.

**Open To:**
- Backend Engineering Internships
- Distributed Systems / Networking focused roles
- Open Source Collaboration
- Gen AI / LLM application projects
- Full Stack opportunities where backend is the core

---

## Tech Stack

**Languages**
<p>
<img src="https://skillicons.dev/icons?i=python,java,cpp,js,ts,go" />
</p>

**Frontend**
<p>
<img src="https://skillicons.dev/icons?i=react,nextjs,html,css,redux,tailwind" />
</p>

**Backend & Databases**
<p>
<img src="https://skillicons.dev/icons?i=nodejs,express,django,spring,dotnet,postgres,mongodb,redis,cassandra" />
</p>

**Cloud, DevOps & Tooling**
<p>
<img src="https://skillicons.dev/icons?i=aws,azure,docker,kubernetes,git,linux,nginx,postman" />
</p>

---

## Featured Projects

<details>
<summary><b>🔹 ArenaNet — Multiplayer Game Backend</b></summary>

A C++20 backend I built so it could plug straight into something like Unity or Godot — handles login, friends, parties, custom lobbies, and full matchmaking. Networking runs on Asio for async TCP, with a small custom protocol (4-byte length header + JSON payload) between client and server.

| Aspect | Details |
|---|---|
| Stack | C++20, Asio, PostgreSQL, Redis, C# SDK |
| Scale | Lobbies, parties, and matchmaking queues all managed in-memory with mutex-protected state |
| Performance | Background matchmaking thread runs every second, widening the ELO range the longer someone waits |
| Security | Auth tokens via Redis, host-only lobby controls, 30-second reconnect grace period if you disconnect |
| Impact | Handles dynamic match sizing — solo players, parties, and "Any" wildcard opponents all get grouped correctly based on total match size |
| Repository | [View on GitHub](https://github.com/harmanD-MAX/ArenaNet) |

Started out as "how hard can matchmaking really be" and turned into one of the bigger things I've built. PostgreSQL stores the permanent stuff — accounts, friends, match history, and leaderboard ranks (using Postgres window functions). Redis handles the fast, short-lived stuff — who's online right now and temp auth tokens. I also wrote a little Python GUI client so I could test 2-3 "players" at once without booting up Unity every time, plus a C# SDK so it drops straight into an actual Unity project.

</details>

<details>
<summary><b>🔹 Blueprint — AI Repository Analyzer</b></summary>

A full-stack tool where you paste in any GitHub repo URL and get back a full architectural breakdown — dependency graphs, technical debt audits, API endpoint discovery, and AI-generated docs, all in one go.

| Aspect | Details |
|---|---|
| Stack | React 19 + TypeScript, .NET 10 (C#), Google Gemini AI, Astra DB (Cassandra), SignalR, Hangfire |
| Scale | Clones and parses the whole repo, storing file trees, metadata, and AI insights in Astra DB |
| Performance | Heavy analysis runs in the background via Hangfire so the UI doesn't freeze up, with live progress pushed over SignalR |
| Security | GitHub OAuth login, JWT-secured endpoints, session persists via Redux + localStorage |
| Impact | Auto-detects REST endpoints across ASP.NET Core, Spring Boot, Express, Flask, and FastAPI, and can spit out ATS-optimized resume bullet points for your own projects |
| Repository | [View on GitHub](https://github.com/harmanD-MAX/Blueprint) |

Basically came from me constantly wanting a faster way to understand a codebase before actually diving into it. It clones the repo with LibGit2Sharp, runs the structure through Gemini, and renders everything as an interactive graph with Cytoscape.js. There's also a Monaco-based code viewer built in, so you can read through the actual files without ever leaving the app. Also has a technical debt checker that flags big files (500+ lines) and any leftover TODO/FIXME comments.

</details>

<details>
<summary><b>🔹 TripWise — AI Travel Planner</b></summary>

A full-stack travel planning app — give it a budget, destination, and travel style, and it builds out a full day-by-day itinerary. Deployed on AWS, frontend on Amplify and backend on EC2.

| Aspect | Details |
|---|---|
| Stack | Next.js 16, React 19, Java Spring Boot 3, Spring AI, PostgreSQL (Supabase), AWS S3/EC2/Amplify |
| Scale | Handles itinerary generation, real-time budget tracking, and media uploads (tickets, reservations, photos) per trip |
| Performance | Route optimization using a TSP algorithm over the OSRM API to cut down travel distance each day |

</details>

## Achievements

<div align="center">

| Recognition | Details |
|---|---|
| 🏆 [Google Maps Platform Award 2025](https://devpost.com/software/geoscope) | Recognized under the Google Maps Platform Awards 2025 for **GeoScope** |

</div>

---

## Contribution Activity

<div align="center">

<img src="https://github-readme-activity-graph.vercel.app/graph?username=harmanD-MAX&theme=react-dark&hide_border=false&border_color=30363d&bg_color=0d1117&color=2dd4bf&line=38bdf8&point=c9d1d9" width="100%" />

</div>

---

<div align="center">


![Footer](https://capsule-render.vercel.app/api?type=waving&color=0:0e7490,50:134e4a,100:0d1117&height=120&section=footer)

</div>




