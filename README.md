# CodeReviewPrompts
# v1.0.0: Initial Release

Two reusable prompt templates for building and auditing Firebase-based web apps with an AI assistant.

## What's included

### `project-build-prompt.md`: Project Builder
A fill-in-the-blank template for generating a new application from a spec in modern vanilla ES6+ JavaScript.

- Placeholders in `[brackets]` for project name, purpose, target users, core features, data entities, and views
- Sections for authentication, data layer, AI integration, analytics, monetization, and content editing/export
- Optional sections (monetization, editor/export) can be deleted if they don't apply
- Asks for modular ES modules, async/await throughout, isolated environment config, and robust error handling
- Requires complete code with no TODO stubs, plus a setup/usage example

### `firebase-code-review-prompt.md`: Production Code Review & Hardening
A strict, two-phase review prompt for auditing a single file before deployment.

- **Phase 1 (analysis only):** findings report with severity, status (Confirmed / Potential / Requires External Verification), evidence, and a surgical change plan. No code is rewritten.
- **Approval gate:** nothing is changed until you approve specific changes.
- **Phase 2 (implementation):** outputs the complete revised file with only approved changes, followed by a self-audit.
- Covers security, correctness, Firebase integration, resource leaks, performance, accessibility, analytics, and production readiness
- Treats client-side auth checks as non-authoritative and never invents Security Rules, schemas, or files it can't see
- Language-neutral core with a swappable `<LANGUAGE_PROFILE>` block. JavaScript profile included, plus a blank template for other languages.

## Suggested workflow

1. Generate a first draft with the Project Builder.
2. Run each generated file through the Code Review prompt, one file at a time.
3. Approve the changes you want, then use Phase 2 to get the revised file.

## Customization notes

- The review prompt assumes a specific architecture: Firebase Auth, SQL Connect, Storage, and Hosting, with PUBLIC / STUDENT / ADMIN page types, GA4 on all pages, and Google Ads conversion tracking forbidden on ADMIN pages. Edit `<APPLICATION_CONTEXT>` and Step 9 to match your own setup.
- To review another language, copy the blank profile template, fill it in, and swap it for the JavaScript profile. Nothing else needs editing.

## Known limitations

- The review is file-level. Findings that depend on other files, Security Rules, or backend config are flagged as "Requires External Verification" rather than guessed.
- Output quality depends on the model. Long files may need to be reviewed in sections.
- Prompts are provided as-is and should be tested against your own code before relying on the results.
