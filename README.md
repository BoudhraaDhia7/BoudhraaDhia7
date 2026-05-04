# Dhia Boudhraa — Full-Stack Engineer

**Backend Architecture · API Orchestration · Infrastructure Automation**

Most engineers touch a system. I own one.

For 3 years I've been building and running a production VPS hosting platform — the kind where a customer clicks "order" and a server exists 90 seconds later, fully provisioned, no one touching a keyboard. I built every layer of that, and I maintain it.

I'm drawn to backend problems that don't have clean solutions — external APIs that fail in unpredictable ways, provisioning flows that need to survive partial failures, billing logic that has to be right every time.

📧 boudhraa@gmail.com
🔗 [linkedin.com/in/dhia-boudhraa](https://linkedin.com/in/dhia-boudhraa-243b80201)
🌍 Based in Tunisia · ZAB-recognized Engineering Degree (German Master's equivalent) · Chancenkarte-eligible

---

## HostStronger — VPS Hosting Platform

> A customer clicks "order". A server exists 90 seconds later.
> No manual steps. No ops team. Just the automation I built.

![Platform order flow](./assets/hs-landing.gif)

Customer places an order → Proxmox spins the VM → Dynadot registers
the domain → Stripe processes the payment → the control panel
configures itself. My code handles the happy path and every failure
in between.

**Live:** [hoststronger.com](https://hoststronger.com)

---

### AI Site Builder

Integrated AI-assisted site creation — customers describe what
they want, the system builds and deploys it.

![AI site builder](./assets/hs-AI.gif)

---

### Provisioning Pipeline

The core of the platform. Orders are processed asynchronously via
Laravel Jobs and Redis queues. Each provisioning step talks to a
different external API — each with its own failure mode.

- **Proxmox VE API** — automated VM creation, configuration, and
  full lifecycle management. Servers spin up without human intervention.
- **Dynadot registrar API** — domain registration, DNS management,
  and transfer handling, all triggered by order events.
- **Retry logic & alerting** — every external call has fallback
  handling. An API failure is a logged, recoverable event — not a
  user-facing crisis.

---

### Billing Engine

- Stripe + PayPal with multi-currency subscription support
- Automated invoicing on every billing cycle
- Webhook state machine handling renewals, failures, and refunds
- PayPal IPN + Stripe webhooks processed asynchronously via queues

---

### Control Panel Automation

No manual server configuration. Ever.

- **cPanel, CyberPanel, SitePro** — provisioned and configured
  automatically when a hosting order completes
- **SSL renewals** — automated, zero-touch
- **WordPress one-click setup** — full LAMP stack configured
  and handed to the customer ready to use
  
---

### Architecture Decisions

| Layer | Approach |
|---|---|
| Job processing | Laravel Jobs + Redis, with retry and dead-letter handling |
| Auth | JWT + refresh token rotation, 2FA via TOTP |
| Service design | Domain-driven service layers, one responsibility per class |
| Infrastructure | Docker + Docker Compose, GCP, Nginx, Linux hardening |
| Frontend | Vue.js (Composition API) + React (Hooks), Tailwind CSS |

---

## Stack

| Layer | Tools |
|---|---|
| Backend | PHP (Laravel, Symfony) · Node.js · TypeScript |
| Frontend | React · Vue 3 · Redux Toolkit · Tailwind CSS |
| Data | MySQL · Redis |
| DevOps | Docker · GCP · Nginx · CI/CD · Linux |
| APIs | Stripe · PayPal · Proxmox VE · Dynadot · SitePro |

---

## On private repos

Most of my production code is in private repositories due to client
confidentiality. I'm happy to walk through architecture decisions,
system design, and specific code samples in a technical interview or call.
