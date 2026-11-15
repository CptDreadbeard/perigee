# ADR-0001: Technology stack

Status: accepted
Date: 2026-11-14

## Context

Perigee is a free, open-source desktop app for spaceflight fans. It runs on a second monitor. It needs an interactive 3D globe and data panels. It runs on macOS, Windows and Linux. It must use few resources when idle. The developer built one small Tauri and Svelte app before. C# is the strongest language of the developer. Rust is new to the developer.

## Decision

Use Tauri 2 as the desktop framework. Use SvelteKit with the static adapter, Svelte 5, TypeScript and Vite for the frontend. Use three.js for the globe. Use Rust for all network access, the SQLite cache and the scheduler. Use pnpm as the package manager.

## Alternatives

- C# with Avalonia. C# is the strongest language of the developer. The globe needs a hand-written renderer in an OpenGL control. This option is the fallback if the WebView fails.
- C# with Godot 4. 3D work is easy. The dashboard UI and the idle power tuning need manual work.
- Rust only, with egui, Slint or iced. The idle cost is lowest. The learning curve is too steep now, because Rust is new to the developer.

## Consequences

Positive:

- three.js provides drag, zoom and click on globe objects.
- The Rust part stays small. The developer can learn it in steps.

Negative:

- A WebView uses more memory than a native user interface.
- A WebView behaves differently on each operating system.
- Linux WebView performance is not verified.

## Review trigger

Milestone M1, the spike, measures the globe in the WebView. If the measurements fail, the project changes to the fallback, C# with Avalonia.
