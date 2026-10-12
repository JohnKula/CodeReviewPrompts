Act as an expert full-stack developer specializing in [primary platform, e.g., Google Cloud / Firebase / AWS / Supabase] and [database type, e.g., relational / NoSQL] architectures. Write clean, modular, modern, production-ready code in vanilla ES6+ JavaScript (plus HTML and CSS where a UI is needed) for [project type, e.g., a single-page web application / Node.js service / browser extension].

---

### Project Overview: [Project Name]
Build [the frontend / backend / full application] for **[Project Name]** ("[tagline or one-line mission]"), a [purpose of project] platform.

The application allows [target users] to:
1. [Core capability #1]
2. [Core capability #2, e.g., AI-assisted content generation]
3. [Core capability #3, e.g., in-browser editing before saving or exporting]
4. [Core capability #4, e.g., purchase and track subscriptions]

---

### Technical Stack & Service Integrations
Your code must initialize and handle client-side operations for the following:

1. **Authentication & Security** — [auth provider]
   - Supported sign-in methods: [e.g., Google Sign-In, email/magic link, SSO]
   - Bot protection: [e.g., reCAPTCHA v3 on sign-up and login]
   - Role-based access: [e.g., MFA enforcement hooks for the ADMIN role]
   - Compliance: [e.g., terms-and-conditions checkbox on registration, cookie consent]

2. **Data Layer** — [database / SDK, e.g., Firebase Data Connect, Firestore, Supabase]
   - Connect via [SDK or client library] queries and mutations.
   - Implement data operations for:
     - **[Entity 1, e.g., User Profiles]:** [key fields]
     - **[Entity 2, e.g., Primary Records]:** [key fields, states, tag/array matching]
     - **[Entity 3, e.g., Workflow Items]:** [lifecycle states, e.g., draft / submitted / complete]
     - **[Entity 4, e.g., Billing]:** [subscriptions, transaction history, promo codes]

3. **AI Integration** — [model/provider, e.g., Gemini via Genkit / Vertex AI, OpenAI, Claude API]
   - Execute [generation task] securely from the client (or via [proxy / cloud function]).
   - Build prompt payloads that merge [static template or source content] with [dynamic user data].
   - Implement exponential backoff, retry handling, and user-friendly error alerts for latency and timeouts.

4. **Analytics** — [e.g., Google Analytics 4]
   - Initialize [tracking snippet], consent-mode banner logic, and [custom events / e-commerce events / page title tracking].

5. **Monetization** (optional) — [e.g., AdSense, Stripe]
   - Include responsive ad placeholders ([config attributes]).
   - Conditionally hide ads for [paying / subscribed] users.

6. **Content Editing & Export** (optional) — [e.g., rich text editor, PDF generation]
   - Provide an editable [WYSIWYG / markdown] container for real-time adjustments.
   - Include client-side hooks for [PDF download / export format] and [auto-submission HTTP POST payloads with mapped fields].

---

### Layout & UI Requirements ([design style, e.g., Metronic-style SaaS dashboard])
- **Design Theme:** [e.g., clean, modern, crisp typography, responsive card grids, modal dialogs, smooth transitions]
- **Core Views/Modals to Render:**
  1. **[View 1, e.g., Public/Auth View]:** [components]
  2. **[View 2, e.g., Main Explorer / Dashboard]:** [filters, sorting, card grid, status badges]
  3. **[View 3, e.g., Workspace]:** [layout, e.g., split view with requirements left, form + editor right; action buttons]
  4. **[View 4, e.g., Tracker]:** [statuses, actions]
  5. **[View 5, e.g., Profile & Settings]:** [tag-based managers, billing modal]
  6. **[View 6, e.g., Ad / Promo Placements]:** [responsive fallback layouts]

---

### JavaScript & Functionality Requirements
- Write clean, modular ES6+ vanilla JavaScript using async/await throughout. Use ES modules ([import/export]) and separate concerns into [e.g., config, auth, data, ai, ui, utils] modules.
- Handle errors robustly for network interruptions, database disconnects, and token/auth verification failures.
- Isolate all environment configuration at the top with descriptive placeholders (e.g., YOUR_API_KEY, YOUR_PROJECT_ID, YOUR_MEASUREMENT_ID, YOUR_CONNECTOR_ID).
- [Optional: browser support target, accessibility standard (e.g., WCAG 2.1 AA), performance constraints, no-build-step requirement, bundler of choice.]

---

### Code Output Rules
1. **Complete Code:** Provide working code in [a single markdown code block / one block per file] with no abbreviated "TODO" comments.
2. **Usage Example Section:** Immediately after the main code, provide a practical setup snippet showing how to [initialize the data connector], [configure mock data, e.g., a sample user profile], and [run a test AI generation call].
