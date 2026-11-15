# Perigee

Perigee is a free desktop app for people who follow spaceflight.
It shows launches, satellites and space weather on a second monitor.

## Status

Pre-alpha. The project setup is in work. There is no release.

## Planned functions

- A countdown to the next launch.
- A list of the next launches.
- A 3D globe that you can turn and zoom.
- Satellites, ground tracks and launch pads on the globe.
- Details for each object when you click it.
- Space weather data.
- The astronomy picture of the day.

## Principles

- No backend. The app gets data directly from public sources.
- No accounts.
- No telemetry and no analytics.
- All settings and cached data stay on your computer.

## Platforms

macOS, Windows and Linux.

## Data sources

Perigee uses data from these sources. Perigee has no affiliation with them.

| Source                               | Data                                        |
| ------------------------------------ | ------------------------------------------- |
| Launch Library 2 by The Space Devs   | Launches and launch pads                    |
| CelesTrak                            | Orbital elements                            |
| NOAA Space Weather Prediction Center | Space weather                               |
| NASA                                 | Astronomy picture of the day, Earth imagery |

## Build from source

Prerequisites:

- Rust (stable) with `rustfmt` and `clippy`
- Node.js (current LTS) and pnpm
- The Tauri 2 system packages for your operating system. Refer to the
  [Tauri prerequisites](https://v2.tauri.app/start/prerequisites/).

Commands:

```bash
pnpm install
pnpm tauri dev      # start the app in development mode
pnpm tauri build    # make a release build
```

## Technology

- Tauri 2
- Svelte and TypeScript for the user interface
- three.js for the globe
- Rust for network access, the cache and the scheduler

## Licence

You can use this software under one of these licences:

- MIT licence ([LICENSE-MIT](LICENSE-MIT))
- Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE))

Contributions to this repository use the same two licences.
