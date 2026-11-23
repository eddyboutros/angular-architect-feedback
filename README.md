# Angular Architect — Feedback & Support

The public issue tracker and support hub for **[Angular Architect](https://plugins.jetbrains.com/plugin/31306-angular-architect)**, an IntelliJ IDEA / WebStorm plugin that maps your Angular components, services, stores, routes, and modules as connected systems — then generates, inspects, navigates, and wires them for you, with a Kubernetes panel for running what you build.

Angular Architect is **freemium since 2.0.0**: most of the plugin is free, and a set of **Pro** features needs a license from JetBrains Marketplace. See [Free and Pro](#free-and-pro) below.

The **plugin source lives in a separate private repository**. This repo exists so users — free and Pro alike — have a public place to:

- 🐛 **File bug reports** — [New bug report →](https://github.com/eddyboutros/angular-architect-feedback/issues/new?template=bug_report.yml)
- ✨ **Request features** — [New feature request →](https://github.com/eddyboutros/angular-architect-feedback/issues/new?template=feature_request.yml)
- ⚠️ **Report false positives** in the inspections — [Report a false positive →](https://github.com/eddyboutros/angular-architect-feedback/issues/new?template=false_positive.yml)
- 💬 **Ask questions and share feedback** in [Discussions](https://github.com/eddyboutros/angular-architect-feedback/discussions)
- ❤️ **Support the project** — see [Support the project](#-support-the-project) below

---

## What is Angular Architect?

A single IntelliJ plugin, version-aware from **Angular 12 to 22** and **TypeScript 4 to 7**: it emits `@Input()` vs `input()`, class-based vs functional guards, `*ngIf` vs `@if`, `HttpClientModule` vs `provideHttpClient()`, experimental vs stable zoneless — whatever fits the versions it detects in your `package.json`.

**64 inspections • 19 generators • 6 intentions • 33+ refactoring detectors • 5 SOLID analysers • 53 live templates • 31 tool-window panels**

Install from JetBrains Marketplace, or search "Angular Architect" in **Settings → Plugins**. Requires **IntelliJ IDEA Ultimate or WebStorm 2025.2+** (the bundled JavaScript and TypeScript plugin).

---

## Free and Pro

Without a license, Pro tabs stay in place with an activation link, and everything else works as usual.

### Free for everyone

- **Generate** — components, feature modules, NgRx stores and action flows, guards, pipes, directives, interceptors, resolvers, CRUD services, reactive and signal forms, interface-from-JSON, feature clone, Extract Component, GraphQL+NgRx features, Standalone Migration, and Angular Material schematics through your project's own CLI.
- **Inspect** — 63 of the 64 inspections: architecture boundaries, circular dependencies, template binding errors, signal misuse, accessibility, dead routes, unused NgRx, deep imports, deprecated APIs (Angular's and third-party libraries'), the RxJS operator advisor, the control-flow / standalone / signal migration assistants, and Angular's style guide (20 on). Plus 33+ refactoring detectors, 5 SOLID analysers, 12 code-review rules, and 6 Alt+Enter intentions.
- **Analyse** — Project Health per feature, Performance grade per component, OSV security advisories, license scan, dependency freshness, code duplication, unused dependencies, code-ownership analytics, and gutter coverage markers.
- **Navigate & visualise** — Feature Graph, Go to Related File, gutter icons, blast-radius and ripple widgets in the status bar, NgRx Flow Tracer, architecture diagram, Signals graph, component and HTTP-API catalogs, route and DI trees, communication map, command palette, and Generate Deep Link.
- **Automate** — the pre-commit Quality Gate and an API mock generator built from your services.

### Pro (license required)

- **Kubernetes panel** — a dashboard for the app you are working on, through your own `kubectl` and kubeconfig: workloads, pods, logs, events, nodes, Helm releases, a Connections map, plain-language failure diagnosis, Troubleshoot Connection, guarded writes (restart, scale, edit YAML, port-forward, exec), and a Deploy wizard that takes an app from code to a running rollout.
- **Upgrade Readiness** — the `angular.dev` update-guide steps for your exact from→to jump, breaking-changes and `ng update` migration catalogs, runtime-floor blockers, and removed-API detection; with **migration hints** in the editor gutter and the **Migration Insights** tab.
- **Error Analysis** — paste browser-console output: NG error codes decoded, the root cause located in your own source, minified frames resolved through your source maps.
- **Unit Test generation** — a runnable `.spec.ts` for the selected file, matched to your runner (Vitest / Jest / Karma) and Angular major.
- **MCP server for AI agents** — the plugin's analysis as read-only tools for MCP-compatible agents; loopback only, off until you start it.
- **OpenAPI / Swagger Studio** — scaffold a typed feature from a spec, re-sync on drift, a live API Explorer, and a mock server.
- **Provenance X-Ray** — trace where a value comes from, hop by hop across files.
- **Impact Analysis dialog** — every direct and indirect consumer of a file, ranked by risk. The status-bar widgets that summarise it stay free.
- **AI Prompt export and Copy Architecture Context** — 22 scan types as structured markdown ready to paste into any AI assistant.
- **Dev-server launcher** — your build, dev server, and backend helpers as one configurable sequence.

### Getting a license

Buy a license from the **Pricing** tab of the [Marketplace listing](https://plugins.jetbrains.com/plugin/31306-angular-architect), then activate it from **Help → Register** in the IDE or from the prompt a Pro feature shows. A free trial can be started from the same place.

Current prices are on the Pricing tab — they are not repeated here so this page can't go stale.

### License, billing, and refund questions

Purchases are sold and processed by **JetBrains Marketplace**, not by me — I can't see your payment details, issue invoices, or process refunds. For anything about a purchase, an invoice, a refund, or a license that won't activate on the JetBrains side, contact [JetBrains sales support](https://sales.jetbrains.com/hc/en-gb).

File an issue **here** when the plugin itself misbehaves around licensing — for example, a Pro feature that stays locked after **Help → Register** shows an active license, or a free feature that asks for one.

---

## Privacy

No telemetry, no analytics, no account. The only automatic network requests are the dependency checks (OSV advisories and the license scan, sending only package names and versions from `package.json`) and a daily rule-pack update; both can be turned off under **Settings → Tools → Angular Architect → Rule Packs**, and offline mode stops all of them. Details: [privacy policy](https://plugins.jetbrains.com/plugin/31306-angular-architect/privacy-policy).

---

## Filing a good bug report

Before filing, please check:

1. You're on the latest plugin version. Update via **Settings → Plugins → Updates**.
2. Your IDE is **IntelliJ IDEA Ultimate or WebStorm 2025.2 (build 252) or later** — earlier builds are not supported.
3. There's no existing issue for the same problem — search [Issues](https://github.com/eddyboutros/angular-architect-feedback/issues?q=is%3Aissue) first.

Then pick a template — the forms guide you through the details that make a bug reproducible without a back-and-forth. The bug template asks whether you're on the free tier, a trial, or a paid license, because a locked Pro tab and a broken one look alike from a screenshot.

**False positives** (an inspection flagging something that isn't actually a problem) have their own template because they need slightly different information: the specific rule that fired, the code that triggered it, and why the rule is wrong for that code. If you're not sure whether you're seeing a false positive or a real problem, use the false-positive template — an inspection flagging real code but with misleading advice still qualifies.

**Kubernetes reports:** please remove cluster names, hostnames, tokens, and Secret values from logs and screenshots before posting. Issues here are public.

---

## ❤️ Support the project

The simplest way to support Angular Architect now is to **buy a Pro license** if the Pro features are useful to you. The free tier stays free.

Behind both tiers there's a set of GitHub Actions that refreshes the bundled Angular metadata, schematic-surface, compat-matrix, deprecated-packages, and update-guide catalogs — so upgrade advice stays current at release time, not just at install time. Each patch that Angular ships triggers a PR that gets reviewed, verified, and folded into the next plugin release. Then there's bug triage from the Marketplace reviews, false-positive reports here, and the ongoing work of tracking the Angular team's roadmap so the plugin's version gating stays honest.

You can also help by:

- **Rating the plugin** on [JetBrains Marketplace](https://plugins.jetbrains.com/plugin/31306-angular-architect/reviews) — a five-star review with a sentence about what worked for you is worth more than you'd think.
- **Filing a good bug or feature request here** — well-scoped issues are how the plugin gets better.
- **Telling one other Angular developer about it** — every install helps the plugin move up in Marketplace search.
- **Donating** — if you use only the free tier and want to give something back, see **[DONATE.md](./DONATE.md)**. A donation is a gift; it does not unlock Pro features.

Thank you. Every license, star, review, issue, and donation is appreciated.

---

## Recently shipped

- **2.2.x** (November 2026) — the Kubernetes Deploy wizard, including deploying something built already (a JAR, a WAR, an Angular build, an image); Helm chart install, upgrade, and rollback; the Connections map and Troubleshoot Connection; Angular CLI `ng update` migrations in Upgrade Readiness; notes on every generator and suggestion when an API is not yet stable in your Angular version; Angular's own best practices in AI Prompt export.
- **2.1.0** (October 2026) — the Kubernetes dashboard as an editor tab, Helm releases, GitOps-aware change warnings, workload timelines.
- **2.0.0** (October 2026) — Free and Pro.

If you want to see something next, [file a feature request](https://github.com/eddyboutros/angular-architect-feedback/issues/new?template=feature_request.yml).

---

## Security

If you find a security issue, please **do not file a public issue**. See [SECURITY.md](./SECURITY.md) for private disclosure.

---

## About this repository

This repository is **not** the Angular Architect plugin — it's a public feedback hub. There is no plugin source, build output, or distributable software here.

- **Plugin licensing** — Angular Architect is proprietary; the license, EULA, and third-party notices live at **[github.com/eddyboutros/angular-architect-legal](https://github.com/eddyboutros/angular-architect-legal)**. Please read those terms before using the plugin.
- **This repo's contents** — © 2026 Eddy Boutros, all rights reserved. Readable freely; not for redistribution or reuse without permission. See [NOTICE.md](./NOTICE.md).
