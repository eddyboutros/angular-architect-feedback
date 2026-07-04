# Security policy

## Reporting a vulnerability

If you believe you've found a security issue in **Angular Architect** — a way for the plugin to leak your workspace to an unintended destination, execute arbitrary code from a workspace file, exfiltrate credentials from environment / config files it scans, or similar — please **do not open a public issue**.

Instead, email me directly at **eddy.boutros.36@gmail.com** with:

- A description of the issue and the impact you believe it has.
- Steps to reproduce (or a proof-of-concept if you have one).
- Which plugin version you observed the issue on.

I'll acknowledge receipt within a few days and aim to ship a fix in the next plugin release. If the issue is severe enough to warrant an out-of-band release, I'll cut one.

## What's in scope

- The IntelliJ plugin distributed on JetBrains Marketplace as **Angular Architect** (any version).
- The bundled data catalogs shipped inside the plugin (`angular-metadata`, `angular-schematics-surface`, `angular-templates`, `angular-upstream`, `angular-compat`, `angular-upgrade`) — specifically, whether any of them could be crafted to cause the plugin to execute code or leak data.

## What's out of scope

- The Angular framework itself — please report those to the [Angular team](https://github.com/angular/angular/security/policy).
- The IntelliJ Platform SDK — please report those to [JetBrains](https://www.jetbrains.com/legal/docs/privacy/security/).
- Third-party npm packages your project depends on — please report those upstream.

Thanks for helping keep the plugin safe.
