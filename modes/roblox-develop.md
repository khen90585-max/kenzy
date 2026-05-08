# Roblox Develop Mode

Roblox develop mode is a project profile for building and iterating on Roblox experiences.
Use it when work targets Roblox Studio, Luau scripts, or asset workflows that need quick local iteration before release.

## Goals

- Keep Roblox-specific changes isolated from release configuration.
- Prefer fast feedback loops for Luau scripts, place files, assets, and documentation.
- Document assumptions about Studio-only APIs, server/client boundaries, and asset IDs before shipping.

## Roblox Join Link

Use this Roblox join link when you need to open or test the shared experience:

- <https://www.roblox.com/join/2wv0w>

## Workflow

1. Create feature work in the development branch or workspace.
2. Sync or edit Roblox assets and Luau code locally.
3. Test gameplay changes in Roblox Studio with both client and server simulation enabled.
4. Record any required asset IDs, permissions, or manual Studio steps in the change notes.
5. Promote the change only after Studio testing passes.

## Checklist

- [ ] Luau scripts are formatted consistently.
- [ ] Client and server code paths are tested in Roblox Studio.
- [ ] New assets include source notes and ownership details.
- [ ] Security-sensitive APIs, remotes, and permissions are reviewed.
- [ ] Release notes mention Roblox-specific setup or migration steps.
