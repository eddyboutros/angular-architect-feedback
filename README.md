# Angular Architect — Feedback & Support

The public issue tracker and support hub for **[Angular Architect](https://plugins.jetbrains.com/plugin/31306-angular-architect)**, a free IntelliJ IDEA / WebStorm plugin that gives Angular developers deep architectural insight, migration tooling, and AI-prompt export for every scan the plugin runs.

The **plugin source lives in a separate private repository**. This repo exists so users have a public place to:

- 🐛 **File bug reports** — [New bug report →](https://github.com/eddyboutros/angular-architect-feedback/issues/new?template=bug_report.yml)
- ✨ **Request features** — [New feature request →](https://github.com/eddyboutros/angular-architect-feedback/issues/new?template=feature_request.yml)
- ⚠️ **Report false positives** in the inspections — [Report a false positive →](https://github.com/eddyboutros/angular-architect-feedback/issues/new?template=false_positive.yml)
- 💬 **Ask questions and share feedback** in [Discussions](https://github.com/eddyboutros/angular-architect-feedback/discussions)
- ❤️ **Support the project** — see [Donate](#-support-the-project) below

---

## What is Angular Architect?

A single IntelliJ plugin that:

- Scans your Angular codebase across **22 dimensions** — performance, signals migration, RxJS operator advisor, SOLID principles, deep import paths, standalone / control-flow migration progress, upgrade readiness, accessibility, and more.
- Ships **58+ inspections** with quick-fixes tuned to the Angular major (v12 → v22) and TypeScript major (4.x → 7.x) it detects from your `package.json`.
- Exports every scan as an **AI-optimised prompt** — copy-paste into Claude / ChatGPT / your model of choice and get a prioritised work plan back.
- Bundles a **weekly-refreshed mirror** of `angular.dev/update-guide`, `angular/angular`'s breaking-changes list, the `ng-update` codemods catalog, and the deprecated-packages advisory feed — so upgrade suggestions stay current at release time, not just at install time.
- Version-aware: emits `@Input()` vs `input()`, class-based vs functional guards, `*ngIf` vs `@if`, `HttpClientModule` vs `provideHttpClient()`, experimental vs stable zoneless — whatever fits your project.

Install from JetBrains Marketplace, or search "Angular Architect" in **Settings → Plugins**.

---

## Filing a good bug report

Before filing, please check:

1. You're on the latest plugin version. Update via **Settings → Plugins → Updates**.
2. The IntelliJ version is at least **2025.2 (build 252)** — earlier builds are not supported.
3. There's no existing issue for the same problem — search [Issues](https://github.com/eddyboutros/angular-architect-feedback/issues?q=is%3Aissue) first.

Then pick a template — the forms guide you through the details that make a bug reproducible without a back-and-forth.

**False positives** (an inspection flagging something that isn't actually a problem) have their own template because they need slightly different information: the specific rule that fired, the code that triggered it, and why the rule is wrong for that code. If you're not sure whether you're seeing a false positive or a real problem, use the false-positive template — an inspection flagging real code but with misleading advice still qualifies.

---

## ❤️ Support the project

**Angular Architect is free and always will be.**

Keeping it that way costs real hours every week. There's a set of GitHub Actions that runs every day to refresh the bundled Angular metadata, schematic-surface, compat-matrix, deprecated-packages, and update-guide catalogs — so upgrade advice stays current at release time, not just at install time. Each patch that Angular ships triggers a PR that gets reviewed, verified, and folded into the next plugin release. Then there's bug triage from the Marketplace reviews, false-positive reports here, and the ongoing work of tracking the Angular team's roadmap so the plugin's version gating stays honest.

A few coffees a month keeps me chasing those. If Angular Architect saves you time, consider giving some back.

### Ways to donate

Donations are handled personally, through **Western Union** — see **[DONATE.md](./DONATE.md)** for the simple steps. In short: email me at [eddy.boutros.36@gmail.com](mailto:eddy.boutros.36@gmail.com?subject=Angular%20Architect%20donation) and the transfer details are exchanged privately — nothing sensitive is ever published here.

If you can't donate right now, you can still help enormously by:

- **Rating the plugin** on [JetBrains Marketplace](https://plugins.jetbrains.com/plugin/31306-angular-architect/reviews) — a five-star review with a sentence about what worked for you is worth more than you'd think.
- **Filing a good bug or feature request here** — well-scoped issues are how the plugin gets better.
- **Telling one other Angular developer about it** — every install helps the plugin move up in Marketplace search.

Thank you. Every star, review, issue, and donation is appreciated.

---

## Roadmap teaser (informal)

Currently on my desk (subject to change):

- Kubernetes to be added inside the plugin.

If you want to see something on this list, [file a feature request](https://github.com/eddyboutros/angular-architect-feedback/issues/new?template=feature_request.yml).

---

## Security

If you find a security issue, please **do not file a public issue**. See [SECURITY.md](./SECURITY.md) for private disclosure.

---

## About this repository

This repository is **not** the Angular Architect plugin — it's a public feedback hub. There is no plugin source, build output, or distributable software here.

- **Plugin licensing** — Angular Architect is proprietary; the license, EULA, and third-party notices live at **[github.com/eddyboutros/angular-architect-legal](https://github.com/eddyboutros/angular-architect-legal)**. Please read those terms before using the plugin.
- **This repo's contents** — © 2026 Eddy Boutros, all rights reserved. Readable freely; not for redistribution or reuse without permission. See [NOTICE.md](./NOTICE.md).
