# Dhia Boudhraa

**Full-Stack Developer · PHP / Laravel · Vue.js / TypeScript**

I'm a full-stack developer based in Neuss, Germany. At EXTERNALISATION.EU, I work on HostStronger, a VPS and web-hosting platform, building customer interfaces and the APIs, background jobs and integrations behind them.

I'm looking for a full-stack development role in Germany. My language levels are German A2, English B2 and French B2. I hold an engineering degree in Computer Science from École Polytechnique de Sousse, with a ZAB Statement of Comparability available.

[LinkedIn](https://www.linkedin.com/in/dhia-boudhraa-243b80201) · [GitHub](https://github.com/BoudhraaDhia7) · [Email](mailto:boudhraad@gmail.com)

## Selected work: HostStronger

[HostStronger](https://hoststronger.com) combines VPS and hosting management with billing, domains, support and website-building workflows.

My work spans both sides of the application:

- **Frontend:** customer and admin interfaces for VPS setup, billing and support with Vue 3, TypeScript and Pinia, within an application with six locale catalogs.
- **Backend:** Laravel REST APIs, request validation, repositories, API resources and OpenAPI documentation.
- **Provisioning:** asynchronous VPS workflows using Proxmox, Laravel jobs and Redis, with task tracking, retries and compensating cleanup for registered steps.
- **Billing:** Stripe checkout and subscription integration, including queued webhook processing across 17 event types and recovery of failed processing attempts.
- **Realtime:** Laravel Reverb updates with HTTP polling fallback, and a browser terminal connected through a Node.js WebSocket-to-SSH bridge and xterm.js.
- **Quality and delivery:** PHPUnit tests and Docker/GitHub Actions workflows alongside frontend and backend feature work.

### How the parts fit together

The Vue application calls Laravel APIs. Laravel stores application state and dispatches background jobs for longer operations. Those jobs coordinate providers such as Proxmox, Dynadot, cPanel and CyberPanel. Reverb and HTTP polling bring operation status back to the interface.

Paid workflows use Stripe events to update local payment and order state before relevant fulfillment work is dispatched. VPS, domain and hosting orders follow their own workflows; not every order creates a VM, registers a domain and provisions a panel.

### Failure handling

External calls use provider-specific retry and timeout policies. Provisioning code can register compensating actions, run them in reverse order and persist failure records for investigation and retry. The webhook worker records attempts and completion separately, with five attempts and increasing retry delays.

These are best-effort recovery mechanisms, not a claim of exactly-once delivery or guaranteed rollback after every failure.

### AI website-builder integration

I integrated SitePro's AI-assisted builder with account, session and publishing workflows. HostStronger passes the customer's prompt to SitePro and coordinates the surrounding hosting workflow. SitePro provides the editor and website-generation engine; I did not build or train that model.

Separate application features call OpenAI for content/translation assistance and Groq for domain-name suggestions.

### Repository scope

A source audit of revision `b376ed1fe` in September 2026 found:

| Measure | Scope |
|---|---|
| 365 OpenAPI operation attributes | Source declarations, not a verified live-route total |
| 33 queued job classes | Classes implementing Laravel's `ShouldQueue` |
| 396 component files and 154 view files | Vue files in their respective frontend directories |
| 15 Pinia store definitions | `defineStore` declarations |
| 6 locale catalogs | English, French, German, Spanish, Italian and Dutch |
| 17 Stripe event mappings | Registered event types, not 17 handler classes |

These figures describe the repository as a whole, not code personally authored in isolation. The application uses Vue, not React. Deployment artifacts include Compose blue-green scripts, a multi-stage Dockerfile and Kubernetes rolling-update manifests; their presence does not establish an uptime figure.

## Public code: Vultr PHP SDK

[Source repository](https://github.com/BoudhraaDhia7/vultr-php-sdk) · [Packagist package](https://packagist.org/packages/boudhraadhia7/vultr-php-sdk)

I adapted and published a Laravel/Symfony-oriented fork of an existing Vultr API client as `boudhraadhia7/vultr-php-sdk`. HostStronger declares it as a dependency.

The package covers Vultr API operations such as instance management and infrastructure catalogs. Its README credits the original upstream implementation. My contribution is the adaptation and packaging, not sole authorship of the original client.

## Core stack

- **Frontend:** Vue 3, TypeScript, JavaScript, Pinia, Tailwind CSS, PrimeVue, Axios
- **Backend:** PHP, Laravel, REST APIs, OpenAPI, Node.js, Express, WebSockets, Laravel Reverb
- **Data:** PostgreSQL, MySQL, Redis, Eloquent ORM
- **Testing and delivery:** PHPUnit, Git, GitHub Actions, Docker, Linux, nginx, Proxmox VE

## Discussing private work

Much of the application code is private. I can discuss the architecture, my contributions and failure-handling decisions in an interview, and share code or demonstrations only where publication is permitted. I do not publish customer data, infrastructure credentials or confidential source.
