# Roblox Develop Tool

This document is a safe starter guide for working on Roblox experiences that you own or are authorized to edit.
It is not an exploit, executor, aimlock, headshot-lock, or bypass tool for public servers.

## Linked Roblox Profile

- Profile URL: <https://www.roblox.com/users/2698009380/profile>
- User ID: `2698009380`

Use this profile link only as a reference for the Roblox account or creator identity connected to the project.
Do not use it to target, automate, scrape, impersonate, or interfere with another user's account.

## How to Use This Develop Tool

1. Open Roblox Studio and sign in with the Roblox account that owns or can edit the experience.
2. Open the place file or team-create experience you want to develop.
3. Review [`modes/roblox-develop.md`](../modes/roblox-develop.md) before adding gameplay or performance changes.
4. Use Studio's Play, Start Server, and Start Player buttons to test both client and server behavior.
5. Use MicroProfiler, Script Performance, and network statistics to find frame-rate problems before changing gameplay scripts.
6. Record any profile links, asset IDs, game IDs, manual setup steps, FPS targets, and test results in your change notes.
7. Publish only after confirming that the change works in your own experience and does not give unfair access in other creators' servers.

## Safe Feature Ideas

These are acceptable features to build inside your own Roblox experience:

- Aim-assist that is balanced, disclosed to players, and validated by the server.
- Camera smoothing and sensitivity settings for keyboard, mouse, controller, and mobile input.
- Training-range targets for practicing aim without affecting public competitive matches.
- Hitbox, recoil, spread, and latency debug overlays that are enabled only in Studio or private test places.
- FPS optimization passes that reduce expensive per-frame loops, high-poly assets, particles, and unnecessary replication.

## Do Not Build

Do not add code, documentation, or links for:

- Aimlock or headshot-lock cheats for public servers.
- Executors, injectors, memory tools, bypasses, or anti-cheat evasion.
- Account automation, credential collection, impersonation, or profile abuse.
- Scripts that modify another creator's experience without authorization.
