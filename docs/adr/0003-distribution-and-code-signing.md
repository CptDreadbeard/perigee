# ADR-0003: Distribution and code signing

Status: accepted
Date: 2026-11-14

## Context

The cost must be as near to zero as possible. The legal name of the developer must not appear in public. The project uses GitHub under the alias CptDreadbeard. Whether SignPath accepts a pseudonymous maintainer is not confirmed.

## Decision

Host the source code, CI and downloads on GitHub. GitHub Actions builds the app for macOS, Windows and Linux. The builds use the free runners for public repositories. Publish releases as GitHub Releases. Release only CI builds. Sign the macOS app with an ad-hoc signature. The plan for Windows is free signing through SignPath Foundation. The publisher shown is "SignPath Foundation". Do not use app stores. Builds before version 0.1 stay local.

## Alternatives

- Apple Developer ID. It costs 99 USD each year. The certificate shows the legal name. An alias is not possible.
- Certum open-source certificate. It costs 69 EUR. The certificate shows the name.
- App stores. They tie the listing to a verified identity.

## Consequences

Positive:
- The cost is zero.
- The design keeps the legal name out of the signing certificates.

Negative:
- macOS users approve the app one time. They open System Settings, then Privacy and Security, then "Open Anyway".
- Without SignPath, Windows shows a SmartScreen warning.
- Whether SignPath accepts a pseudonymous maintainer is not confirmed.

## Review trigger

After release 0.1, if macOS users report problems with the first start, examine the Apple Developer ID option again. Examine this decision again also when SignPath answers.
