# Dhia Boudhraa — Software Engineer
**Full-Stack Architecture • API Orchestration • System Automation**

I design and build scalable web systems with a focus on **automation** and **reliability**. My expertise lies in connecting complex backend logic (Laravel/Node.js) with reactive frontends (React/Vue), managed through robust DevOps practices.

🌍 **Relocation:** Based in Tunisia | **ZAB Recognized Engineering Degree** | Ready for Germany (Relocation) or Remote (EU Timezones).

- 📧 **Email:** boudhraad@gmail.com
- 🔗 **LinkedIn:** [dhia-boudhraa](https://linkedin.com/in/dhia-boudhraa-243b80201)

---

## 🏗️ Featured Project: HostStronger (Hosting Automation)

HostStronger is a comprehensive platform designed to automate the lifecycle of domains and cloud hosting. My work centered on building a reliable "Provisioning Pipeline" that handles multiple external service providers.

<img src="./assets/hs-landing.gif" alt="Hosteur landing flow" width="900">

**Core Architectural Contributions:**
- **Service Orchestration:** Integrated Dynadot and Site.pro APIs to automate domain registration, DNS management, and site deployments.
- **Asynchronous Processing:** Built an order-handling engine using **Laravel Jobs and Redis** to process service provisioning tasks in the background, ensuring system stability during external API latency.
- **Billing Architecture:** Engineered a full-cycle subscription system with **Stripe and PayPal**, managing complex webhook states for recurring payments, trials, and multi-currency transactions.
- **Infrastructure:** Containerized the entire stack with **Docker**. Managed GCP environments using CyberPanel to automate SSL renewals and system backups.

**Stack:** Laravel, Vue.js (Composition API), Docker, Redis, Nginx, GCP, Stripe, PayPal.
**Live:** [hoststronger.com](https://hoststronger.com)

<div align="center">
<h3>🚀 AI Builder & WordPress Automation</h3>
<details open>
  <summary>Click to view logic flows</summary>
  <p>
    <img src="./assets/hs-AI.gif" alt="AI site builder" width="420" style="margin:10px;">
    <img src="./assets/hs-wp.gif" alt="WordPress one-click setup" width="420" style="margin:10px;">
  </p>
</details>
</div>

---

## 🚀 Engineering Challenges & Solutions

### 1. BID-TN | Event-Driven Auction Platform 
**The Challenge:** Maintaining a consistent global state for bidders during high-concurrency auction events.

<img src="./assets/BID.gif" alt="Auction main flow" width="900">

- **The Solution:** Implemented an event-driven architecture using **Laravel WebSockets** and **Redis** for real-time data broadcasting.
- **State Management:** Used **Redux Toolkit (RTK Query)** on the frontend to manage server-state caching and ensure UI reactivity across bidding rooms.

<img src="./assets/bid-live.gif" alt="Auction live room" width="600">

---

### 2. LondonWaste | Real-Time Logistics Tracking
**The Challenge:** Coordinating driver locations and task assignments dynamically to reduce manual dispatching overhead.

<div align="center">
  <img src="./assets/WASTE.gif" alt="LondonWaste tracking" width="375">
</div>

- **The Solution:** Integrated **Mapbox API** with a **Socket.IO** backend to provide live driver tracking and dynamic route updates.
- **Logic:** Built a centralized dashboard that handles live state updates, allowing admins to reassign tasks based on driver proximity.

---

### 3. Smart-Learn | Media-Heavy E-Learning
**The Challenge:** Managing large-scale media uploads and structured course content delivery without blocking server performance.

<img src="./assets/SM-LD.gif" alt="Smart-Learn course creator" width="900">

- **The Solution:** Developed an asynchronous multi-step content creator using **Laravel Media APIs** and optimized storage protocols.
- **Architecture:** Architected a modular "Course Engine" that supports various media types (Video/Audio/PDF) with automated progress tracking.

---

## 🛠️ Technical Toolbox

- **Languages/Frameworks:** PHP (Laravel, Symfony), JavaScript/TypeScript (React, Vue 3, Node.js).
- **Frontend Tools:** Redux Toolkit, RTK Query, Tailwind CSS, MUI, PrimeVue.
- **Data & Caching:** MySQL, Redis, PostgreSQL.
- **DevOps & Cloud:** Docker & Docker Compose, Google Cloud (GCP), Nginx, CI/CD, Linux.
- **Third-Party APIs:** Stripe, PayPal, Dynadot, Site.pro, Mapbox, WebSockets.

---

## 📄 Professional Note
A significant portion of my production code is held in private repositories for client confidentiality. However, I am prepared to **walk through my architectural decisions**, system designs, and specific code samples during a technical interview or call.
