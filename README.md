<div align="center">

![Header Banner](https://capsule-render.vercel.app/api?type=blur&height=280&color=gradient&customColorList=6,12,20,24,30&text=Harman&fontSize=44&fontColor=ffffff&animation=fadeIn&desc=Backend%20Engineer%20%7C%20Distributed%20Systems%20%7C%20GenAI%20%7C%20Full%20Stack&descAlignY=70&descSize=20)

</div>


## About Me

I'm a computer science student who ended up falling in love with the backend side of things. Most people start out chasing UI work, and I did too for a while, but somewhere along the way I got a lot more interested in how systems actually talk to each other — request routing, load handling, caching, the networking layer underneath it all. That's where I spend most of my time now.

I still build full stack when a project needs it, but if you hand me a codebase, I'll gravitate toward the server and the architecture diagram before I touch the CSS. Lately I've also been spending a lot of time exploring generative AI — not just calling an API and calling it a day, but actually understanding how retrieval, embeddings, and prompt design fit into a real application.

I don't have industry experience yet — I'm still a student — but I learn by building, breaking things, and rebuilding them properly the second time around.

**Open To:**
- Backend Engineering Internships
- Distributed Systems / Networking focused roles
- Open Source Collaboration
- Gen AI / LLM / Kernel projects
- Full Stack opportunities where backend is the core


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
| Stack | Next.js 16, React 19, Java Spring Boot 3, Spring Security (JWT), Spring AI, PostgreSQL (Supabase), AWS S3, AWS EC2, AWS Amplify, Clerk, Leaflet Maps |
| Scale | Manages AI-generated itineraries, expense tracking, trip templates, media uploads, and multi-day travel plans with cloud-backed persistence |
| Performance | Uses a TSP route optimization algorithm with the OSRM API to minimize travel distance, dynamically renders map layers, and streams uploads directly to Amazon S3 |
| Security | Clerk authentication, JWT-protected Spring Boot APIs, role-based authorization, and secure media storage in Amazon S3 |
| Impact | Automatically generates personalized travel itineraries, predicts trip budgets, optimizes daily routes, stores travel documents, and provides AI-powered trip insights through an interactive assistant |
| Repository | [View on GitHub](https://github.com/harmanD-MAX/TripWise) |

Basically came from me constantly wanting a faster way to understand a codebase before actually diving into it. It clones the repo with LibGit2Sharp, runs the structure through Gemini, and renders everything as an interactive graph with Cytoscape.js. There's also a Monaco-based code viewer built in, so you can read through the actual files without ever leaving the app. Also has a technical debt checker that flags big files (500+ lines) and any leftover TODO/FIXME comments.

</details>

<details>
<summary><b>🔹 TripWise — AI Travel Planner</b></summary>

A full-stack travel planning app — give it a budget, destination, and travel style, and it builds out a full day-by-day itinerary. Deployed on AWS, frontend on Amplify and backend on EC2.

| Aspect | Details |
|---|---|
| Stack | Next.js 16, React 19, Java Spring Boot 3, Spring Security (JWT), Spring AI, PostgreSQL (Supabase), AWS S3, AWS EC2, AWS Amplify, Clerk Authentication |
| Scale | Supports AI itinerary generation, budget planning, trip templates, media uploads, AI assistant, and multi-day trip management with persistent cloud storage |
| Performance | Optimizes daily travel routes using a TSP algorithm with the OSRM API, dynamically updates Leaflet maps, and streams file uploads directly to Amazon S3 |
| AI Features | Google Gemini generates day-by-day itineraries, predicts travel budgets, powers an interactive travel assistant, and produces itinerary intelligence reports |
| Security | Clerk authentication, JWT-secured Spring Boot APIs, role-based endpoint protection, and secure cloud file storage on Amazon S3 |
| Infrastructure | Frontend deployed on AWS Amplify, backend hosted on AWS EC2, PostgreSQL on Supabase, object storage on Amazon S3 |
| Features | Interactive Leaflet maps, live weather, expense tracking, trip templates, route optimization, AI itinerary generation, media uploads, and intelligent trip analysis |
| Repository | [View on GitHub](https://github.com/harmanD-MAX/TripWise) |

</details>





