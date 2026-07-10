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
<img src="https://skillicons.dev/icons?i=aws,azure,docker,kubernetes,git,githubactions,linux,nginx,postman" />
</p>

---

## Featured Projects

<details>
<summary><b>🔹 ArenaNet — Multiplayer Game Backend</b></summary>

A C++20 backend built to plug straight into an engine like Unity or Godot, handling everything from login and friends to parties, custom lobbies, and full matchmaking. Networking runs on Asio for async TCP, with a lightweight custom protocol (4-byte length header + JSON payload) between client and server.

| Aspect | Details |
|---|---|
| Stack | C++20, Asio, PostgreSQL, Redis, C# SDK |
| Scale | Concurrent lobbies, parties, and matchmaking queues managed in-memory with mutex-protected state |
| Performance | Background matchmaking thread runs every second, dynamically widening ELO range on long waits |
| Security | Auth tokens via Redis, host-only lobby controls, 30-second session recovery grace period on disconnect |
| Impact | Deep dive into real-time multiplayer backend design — matchmaking logic, party grouping, and dynamic match sizing (including wildcard "Any" opponent matching) |
| Repository | [View on GitHub](https://github.com/harmanD-MAX/ArenaNet) |

This started as "how hard can matchmaking actually be" and turned into one of the more involved things I've built. PostgreSQL handles the permanent stuff — accounts, friends, match history, leaderboard ranks via window functions — while Redis tracks who's online and holds short-lived tokens. I even shipped a small Python GUI client just so I could test two or three players at once without opening Unity every time, plus a C# SDK so the whole thing drops into a real game project.

</details>

<details>
<summary><b>🔹 Blueprint — AI Repository Analyzer</b></summary>

A full stack tool that takes any GitHub repo URL and gives back a complete architectural breakdown — dependency graphs, technical debt audits, API endpoint discovery, and AI-generated documentation, all in one pass.

| Aspect | Details |
|---|---|
| Stack | React 19 + TypeScript, .NET 10 (C#), Google Gemini AI, Astra DB (Cassandra), SignalR, Hangfire |
| Scale | Clones and parses full repositories, storing metadata, file trees, and AI insights in Astra DB |
| Performance | Heavy analysis offloaded to background jobs via Hangfire so the UI stays responsive; live progress pushed over SignalR WebSockets |
| Security | GitHub OAuth login with JWT-secured endpoints, session persistence via Redux |
| Impact | Auto-detects REST endpoints across ASP.NET Core, Spring Boot, Express, Flask, and FastAPI, and generates ATS-optimized resume-ready feature summaries |
| Repository | [View on GitHub](https://github.com/harmanD-MAX/Blueprint) |

The idea came from constantly wanting a faster way to understand a codebase before diving in. It clones the repo with LibGit2Sharp, runs the structure through Gemini, and renders everything as an interactive graph with Cytoscape.js. There's also a Monaco-based code viewer built in, so you can browse the actual files without leaving the app.

</details>

<details>
<summary><b>🔹 TripWise — AI Travel Planner</b></summary>

A full stack travel planning app that turns a budget, destination, and travel style into a complete day-by-day itinerary, deployed on AWS with the frontend on Amplify and the backend on EC2.

| Aspect | Details |
|---|---|
| Stack | Next.js 16, React 19, Java Spring Boot 3, Spring AI, PostgreSQL (Supabase), AWS S3/EC2/Amplify |
| Scale | Handles itinerary generation, real-time budget tracking, and media uploads (tickets, reservations, photos) per trip |
| Performance | Route optimization powered by a TSP algorithm over the OSRM API to minimize daily travel distance |
| Security | JWT auth via Spring Security, Clerk-based authentication on the frontend |
| Impact | AI budget predictions with local currency detection, an intelligence report that flags itinerary issues, and an in-app AI chat assistant for trip questions |
| Repository | [View on GitHub](https://github.com/harmanD-MAX/TripWise) |

This one was less about the AI call and more about what happens after — taking Gemini's raw itinerary output and actually structuring it into days, activities, and costs that make sense. The map side uses Leaflet with a day-by-day filter and toggleable Satellite/Street/Topographic/Dark layers, and the "Optimize Route" button reorders each day's stops to cut down on backtracking.

</details>

---

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




