# Security policy

## Reporting a vulnerability

If you think you have found a security problem in Angular Architect, please don't open a public issue. Email me at **eddy.boutros.36@gmail.com** instead.

Examples of what I mean by a security problem:

- The plugin sends something from your workspace to a place you did not expect.
- It runs code taken from a file in your workspace.
- It leaks credentials from environment or config files it scans.
- It exposes Kubernetes Secret values or kubeconfig credentials.
- It runs a `kubectl` or Helm command different from the one it showed you.
- An MCP client can reach the server without a valid token, or can change files through it.

In the email, please include:

- What the problem is and what you think its impact is.
- Steps to reproduce it, or a proof of concept if you have one.
- The plugin version you saw it on.

I will reply within a few days and aim to fix it in the next release. If it is serious, I will ship a separate release for it.

## In scope

- The Angular Architect plugin as published on JetBrains Marketplace, any version, free and Pro features.
- The Kubernetes panel and the Deploy wizard: the commands they run through your `kubectl` and Helm, the confirmations, the read-only mode, and how Secret values and saved reports are handled.
- The MCP server: that it only listens on localhost, how it handles tokens, and that its tools cannot modify files.
- The license check, if it can be made to leak data or run code. Using Pro features without a license is not a risk to users, but I would still like to hear about it by email.
- The data catalogs bundled with the plugin (`angular-metadata`, `angular-schematics-surface`, `angular-templates`, `angular-upstream`, `angular-compat`, `angular-upgrade`), if one of them could be crafted to make the plugin run code or leak data.

## Out of scope

- Angular itself. Report those to the [Angular team](https://github.com/angular/angular/security/policy).
- The IntelliJ Platform. Report those to [JetBrains](https://www.jetbrains.com/legal/docs/privacy/security/).
- npm packages your project depends on. Report those to their maintainers.
- Your cluster, `kubectl`, Helm or your identity provider. The plugin uses your own tools with your own credentials, so problems in those belong with their maintainers.
- JetBrains Marketplace purchases and the JetBrains licensing service. Report those to [JetBrains](https://www.jetbrains.com/legal/docs/privacy/security/).

Thanks for helping keep the plugin safe.
