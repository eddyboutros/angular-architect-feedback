# Security policy

## Reporting a vulnerability

If you believe you've found a security issue in **Angular Architect** — a way for the plugin to leak your workspace to an unintended destination, execute arbitrary code from a workspace file, exfiltrate credentials from environment / config files it scans, expose Kubernetes Secret values or kubeconfig credentials, run a `kubectl` or Helm command other than the one it showed you, let an MCP client reach the server without a valid token or modify files through it, or similar — please **do not open a public issue**.

Instead, email me directly at **eddy.boutros.36@gmail.com** with:

- A description of the issue and the impact you believe it has.
- Steps to reproduce (or a proof-of-concept if you have one).
- Which plugin version you observed the issue on.

I'll acknowledge receipt within a few days and aim to ship a fix in the next plugin release. If the issue is severe enough to warrant an out-of-band release, I'll cut one.

## What's in scope

- The IntelliJ plugin distributed on JetBrains Marketplace as **Angular Architect** (any version), free and Pro features alike.
- The **Kubernetes panel** and Deploy wizard — the commands the plugin runs through your `kubectl` / Helm, its confirmations and read-only mode, and how it handles Secret values and saved reports.
- The **MCP server** — its loopback binding, token handling, and the read-only guarantee of its tools.
- The **license check** — a way to make it leak data or run code. (A way to use Pro features without a license is not a vulnerability for users, but I'd still like to hear about it by email.)
- The bundled data catalogs shipped inside the plugin (`angular-metadata`, `angular-schematics-surface`, `angular-templates`, `angular-upstream`, `angular-compat`, `angular-upgrade`) — specifically, whether any of them could be crafted to cause the plugin to execute code or leak data.

## What's out of scope

- The Angular framework itself — please report those to the [Angular team](https://github.com/angular/angular/security/policy).
- The IntelliJ Platform SDK — please report those to [JetBrains](https://www.jetbrains.com/legal/docs/privacy/security/).
- Third-party npm packages your project depends on — please report those upstream.
- Your cluster, `kubectl`, Helm, or your identity provider — the plugin drives your own tools with your own credentials; issues in those belong upstream.
- JetBrains Marketplace purchases and the JetBrains licensing service — please report those to [JetBrains](https://www.jetbrains.com/legal/docs/privacy/security/).

Thanks for helping keep the plugin safe.
