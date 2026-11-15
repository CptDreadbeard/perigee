# ADR-0005: Upgrade to SvelteKit 3

Status: accepted
Date: 2026-11-15

## Context

The Tauri scaffold installed SvelteKit 2. A Dependabot pull request proposed SvelteKit 3. Its check failed. SvelteKit 3 does not read svelte.config.js. The project had no application code at that time. The migration cost was therefore low.

## Decision

The project now uses SvelteKit 3.2.0 and adapter-static 4. The upgrade was done before the project contained application code. The configuration moved from svelte.config.js into the sveltekit() plugin call in vite.config.js. The project deleted svelte.config.js. The file tsconfig.json now extends "$app/tsconfig". The "$lib" alias is replaced by "#lib" subpath imports with file extensions. An "imports" block in package.json defines them. The adapter keeps the fallback option "index.html", which Tauri needs. The minimum Node version is 22.17.

The migration used the official tool "sv migrate sveltekit-3". Type check, build and lint passed after the migration.

## Alternatives

- Stay on SvelteKit 2 until after milestone M1.

## Consequences

Positive:
- The project uses the current major version.

Negative:
- The Tauri documentation and the scaffold still show the SvelteKit 2 configuration file. Their examples need adaptation.
- Dependabot is limited to minor and patch updates.
- Major updates are done by hand. Each major update needs a decision record.

## Review trigger

A Tauri release changes its SvelteKit integration.
