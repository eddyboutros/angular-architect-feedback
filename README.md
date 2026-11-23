# Angular Architect: Feedback & Support

This is the public issue tracker for [Angular Architect](https://plugins.jetbrains.com/plugin/31306-angular-architect), a plugin for IntelliJ IDEA and WebStorm. The plugin's source code is in a private repository, so this is where bugs, feature requests and questions go.

- [Report a bug](https://github.com/eddyboutros/angular-architect-feedback/issues/new?template=bug_report.yml)
- [Request a feature](https://github.com/eddyboutros/angular-architect-feedback/issues/new?template=feature_request.yml)
- [Report a false positive](https://github.com/eddyboutros/angular-architect-feedback/issues/new?template=false_positive.yml) from an inspection
- [Ask a question](https://github.com/eddyboutros/angular-architect-feedback/discussions) in Discussions

Since version 2.0.0 the plugin has a free tier and a paid Pro tier. Everyone is welcome here, whichever one you use.

## What is Angular Architect?

Angular Architect reads your Angular project as a set of connected parts: components, services, stores, routes and modules. It uses that picture to generate code, wire files together, find problems, and help you move around a large codebase.

It checks the Angular and TypeScript versions in your `package.json` (Angular 12 to 22, TypeScript 4 to 7) and writes code that fits them. On an older project you get `@Input()`, `*ngIf` and class-based guards. On a newer one you get `input()`, `@if` and functional guards.

It also has a Kubernetes panel, which is a big part of the plugin now. You can look after the app you are working on, frontend or backend, without leaving the IDE. The panel uses your own `kubectl` and kubeconfig, so if your login works in the terminal it works here too, and every view shows the command it ran. With it you can:

- See what is running and what is unhealthy: workloads, pods, services, ingress, config, events, nodes, Helm releases and custom resources. You can connect several contexts at once, and a Connections map shows which workloads call which.
- Find out why a pod is failing. The panel explains exit codes, OOM kills, failed probes, scheduling and mount problems in plain words. You can open up to four logs side by side, and stack frames link back to your source.
- Make changes: restart or undo a rollout, scale, edit YAML with a dry run and a diff, forward ports (and point `ng serve`'s proxy at them), open a shell in a container, and install, upgrade or roll back Helm charts.
- Deploy. A wizard takes an Angular app, or a Java, Node, Python, Go or .NET backend, from source to a running rollout. It can also deploy something you have already built, such as a JAR, a WAR, an Angular build or an image.

Every change asks for confirmation and shows the exact command first. There is a read-only mode that hides all writes. Nothing gets installed in your cluster.

In numbers: 64 inspections, 19 generators, 6 intentions, 33+ refactoring detectors, 5 SOLID analysers, 53 live templates and 31 tool-window panels.

To install it, search for "Angular Architect" in **Settings → Plugins**, or get it from [JetBrains Marketplace](https://plugins.jetbrains.com/plugin/31306-angular-architect). You need IntelliJ IDEA Ultimate or WebStorm, 2025.2 or later.

## Free and Pro

Most of the plugin is free. If you don't have a license, the Pro tabs are still visible and show an activation link. Everything else works as usual.

### Free

- Generators for components, feature modules, NgRx stores and action flows, guards, pipes, directives, interceptors, resolvers, CRUD services, reactive and signal forms, interfaces from JSON, feature clone, Extract Component, GraphQL+NgRx features, Standalone Migration, and Angular Material schematics run through your project's own CLI.
- 63 of the 64 inspections. They cover architecture boundaries, circular dependencies, template binding errors, signal misuse, accessibility, dead routes, unused NgRx code, deep imports, deprecated APIs in Angular and in third-party libraries, RxJS operator advice, the control-flow, standalone and signal migration assistants, and Angular's style guide (from Angular 20).
- The refactoring detectors, the SOLID analysers, 12 code-review rules and the Alt+Enter intentions.
- Project Health per feature, a Performance grade per component, OSV security advisories, a license scan, dependency freshness, duplicated code, unused dependencies, code-ownership stats from git history, and coverage markers in the gutter.
- Navigation and diagrams: Feature Graph, Go to Related File, gutter icons, the blast-radius and ripple widgets in the status bar, NgRx Flow Tracer, the architecture diagram, the Signals graph, component and HTTP API catalogs, route and DI trees, the communication map, the command palette and Generate Deep Link.
- The pre-commit Quality Gate and an API mock generator built from your services.

### Pro

- The Kubernetes panel described above, including the Deploy wizard.
- Upgrade Readiness. It shows the angular.dev update-guide steps for the exact versions you are moving between, the breaking changes, the `ng update` migrations, and anything that blocks the upgrade. Migration hints show the same findings in the editor gutter, and the Migration Insights tab tracks how far each feature has moved to signals, standalone and control flow.
- Error Analysis. Paste what the browser console printed and it explains the NG error codes, points to the cause in your own source, and resolves minified frames through your source maps.
- Unit test generation. It writes a runnable `.spec.ts` for the selected file that matches your test runner (Vitest, Jest or Karma) and your Angular version.
- An MCP server that gives AI agents read-only access to the plugin's analysis. It listens on localhost only and stays off until you start it.
- OpenAPI / Swagger Studio. Scaffold a typed feature from a spec, re-sync when the spec changes, send live requests, and run a mock server.
- Provenance X-Ray, which traces where a value comes from across files.
- The full Impact Analysis dialog, listing everything that depends on a file. The status-bar widgets that summarise it are free.
- AI Prompt export and Copy Architecture Context. They turn 22 kinds of scan into markdown you can paste into an AI assistant.
- The dev-server launcher, which starts your build, dev server and backend helpers in one sequence.

### Getting a license

Prices are on the Pricing tab of the [Marketplace page](https://plugins.jetbrains.com/plugin/31306-angular-architect). After you buy, activate the license in the IDE under **Help → Register**, or from the prompt that a Pro feature shows. You can start a free trial from the same place.

### Billing and refunds

Licenses are sold by JetBrains, not by me. I can't see your payment, send an invoice or issue a refund. For any of that, please contact [JetBrains sales support](https://sales.jetbrains.com/hc/en-gb).

If the plugin gets licensing wrong, that is a bug and it belongs here. For example: a Pro feature stays locked although **Help → Register** shows an active license, or a free feature asks for one.

## Privacy

The plugin has no telemetry, no analytics, and needs no account. It makes two kinds of network request on its own: the dependency checks (security advisories and the license scan, which send only package names and versions from `package.json`) and a daily rule-pack update. You can turn both off under **Settings → Tools → Angular Architect → Rule Packs**, and offline mode stops all of them. The full [privacy policy](https://plugins.jetbrains.com/plugin/31306-angular-architect/privacy-policy) is on Marketplace.

## Before you file a bug

1. Update to the latest plugin version (**Settings → Plugins → Updates**).
2. Check your IDE version. The plugin needs IntelliJ IDEA Ultimate or WebStorm 2025.2 (build 252) or later.
3. Search the [existing issues](https://github.com/eddyboutros/angular-architect-feedback/issues?q=is%3Aissue) in case someone has already reported it.

Then pick a template. The forms ask for the details I need to reproduce the problem. The bug form also asks whether you are on the free tier, a trial or a paid license, because a locked Pro tab and a broken one look the same in a screenshot.

Use the false-positive form when an inspection flags code that is fine, or when its advice is wrong for your case. If you can't tell whether it is a false positive or a real bug, use that form anyway.

If your report involves Kubernetes, please remove cluster names, hostnames, tokens and Secret values from logs and screenshots first. Issues here are public.

## Supporting the project

If the Pro features are useful to you, buying a license is the best way to support the plugin. The free tier stays free.

A lot of the work is keeping up with Angular. GitHub Actions refresh the Angular data bundled with the plugin (API metadata, schematics, the compatibility matrix, deprecated packages and the update guide), and I review each refresh before it goes into a release. The rest is fixing bugs and false positives reported here and on Marketplace.

Other ways to help:

- Leave a review on [JetBrains Marketplace](https://plugins.jetbrains.com/plugin/31306-angular-architect/reviews). A sentence about what you use the plugin for helps other people decide.
- File clear bug reports and feature requests.
- Tell another Angular developer about it.
- Donate. If you only use the free tier and want to give something back, see [DONATE.md](./DONATE.md). A donation is a gift and does not unlock Pro features.

Thank you.

## Recently shipped

- 2.2 (November 2026): the Kubernetes Deploy wizard, including deploying something already built; installing, upgrading and rolling back Helm charts; the Connections map and Troubleshoot Connection; the Angular CLI's `ng update` migrations in Upgrade Readiness; a note on generated code when an API is not yet stable in your Angular version; Angular's own best practices in AI Prompt export.
- 2.1 (October 2026): the Kubernetes dashboard as an editor tab, Helm releases, a warning before changing a workload that Argo CD or Flux manages, and workload timelines.
- 2.0 (October 2026): the Free and Pro tiers.

If there is something you would like next, [file a feature request](https://github.com/eddyboutros/angular-architect-feedback/issues/new?template=feature_request.yml).

## Security

Please don't report security problems in a public issue. [SECURITY.md](./SECURITY.md) explains how to report them privately.

## About this repository

This repository does not contain the plugin. There is no source code, build output or download here.

The plugin is proprietary. Its license, EULA and third-party notices are at [github.com/eddyboutros/angular-architect-legal](https://github.com/eddyboutros/angular-architect-legal). Please read them before using the plugin.

The contents of this repository are © 2026 Eddy Boutros, all rights reserved. You can read them freely, but please don't redistribute or reuse them without permission. See [NOTICE.md](./NOTICE.md).
