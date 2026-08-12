+++
title = "Running changelog"
[cascade]
  [cascade.params]
    type = "docs"
+++

This is the bleeding-edge changelog since version 2026.07, for **pre-release 2026.08**.

### Build commands

- queued build cancellation and rejection now apply yardmaps after their existing rectangular checks, allowing the same compatible overlaps as sequential construction. Set `construction.useYardmapsForQueuedBuildOverlap = false` in `gamedata/modrules.lua` to restore the previous rectangle-only queue behavior.
- add `Spring.TestBuildOrderOverlap(queuedBuild, proposedBuild) → boolean overlaps, boolean cancels` to test a queued build against a proposed build. `overlaps` reports any conflict under the queued-build yardmap rules; `cancels` reports that the conflict is also inside the cancellation rectangle. Each build is `{unitDefID, x, y, z, facing}`.
