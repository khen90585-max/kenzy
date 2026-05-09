# Roblox Develop Mode

Roblox develop mode is a project profile for building and iterating on Roblox experiences.
Use it when work targets Roblox Studio, Luau scripts, or asset workflows that need quick local iteration before release.

## Goals

- Keep Roblox-specific changes isolated from release configuration.
- Prefer fast feedback loops for Luau scripts, place files, assets, and documentation.
- Document assumptions about Studio-only APIs, server/client boundaries, and asset IDs before shipping.
- Build competitive mechanics that are fair, transparent, and testable instead of exploit tools for public servers.

## Safety Boundaries

Roblox development work must stay inside experiences, assets, and scripts that the developer owns or is authorized to modify.
Do not build, document, or distribute executors, aimlocks, headshot locks, wallhacks, bypasses, or other tools meant to cheat in other creators' servers.

Acceptable alternatives include:

- Aim-assist mechanics for your own Roblox experience when they are disclosed and balanced for all players.
- Training-range bots, hitbox visualizers, recoil/spread debuggers, and replay tools that run only in Studio or authorized test places.
- Accessibility options such as sensitivity sliders, controller dead-zone tuning, target highlighting in PvE modes, and camera smoothing.
- Performance profiling and optimization work that improves frame pacing without bypassing Roblox client protections or platform rules.

## Performance Targets

When targeting smooth play around 124 FPS to 144 FPS, treat the target as a performance budget rather than a guarantee because final frame rate depends on device hardware, Roblox client settings, graphics quality, network conditions, and the experience's content.

Recommended checks:

1. Use Roblox Studio's MicroProfiler, Script Performance, and network statistics to find CPU, GPU, memory, and replication bottlenecks.
2. Keep expensive client-side work out of per-frame loops unless it is required for camera, input, or animation responsiveness.
3. Prefer event-driven code over polling, cache repeated lookups, and disconnect unused connections.
4. Stream large worlds, reduce unnecessary parts and constraints, and simplify meshes, textures, particles, shadows, and post-processing where possible.
5. Validate RemoteEvent and RemoteFunction usage so servers send only the data clients need.
6. Test on low-, mid-, and high-end devices before claiming a specific FPS target in release notes.

## Workflow

1. Create feature work in the development branch or workspace.
2. Sync or edit Roblox assets and Luau code locally.
3. Test gameplay changes in Roblox Studio with both client and server simulation enabled.
4. Record any required asset IDs, permissions, performance targets, or manual Studio steps in the change notes.
5. Promote the change only after Studio testing passes and any fairness or security risks are reviewed.

## Checklist

- [ ] Luau scripts are formatted consistently.
- [ ] Client and server code paths are tested in Roblox Studio.
- [ ] New assets include source notes and ownership details.
- [ ] Security-sensitive APIs, remotes, and permissions are reviewed.
- [ ] Competitive mechanics are documented as authorized gameplay features, not exploit tools for third-party servers.
- [ ] FPS-sensitive changes include profiling notes, target hardware, and before/after measurements.
- [ ] Release notes mention Roblox-specific setup or migration steps.
