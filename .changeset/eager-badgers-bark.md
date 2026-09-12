---
type: Changed
pr: 0
---
**The path-containment predicate is now a single exported seam** — `security.cjs` no longer exports `validatePath`; `assertWithinRoot` (throws), `tryWithinRoot` (returns null) and `requireSafePath` are the only containment exports, and all three return a branded `ContainedPath` so a validated path cannot be silently swapped for an unvalidated one. The per-call-site `{ allowAbsolute: true }` flag is replaced by the named `PathAcceptance` policy, which states what it actually permits: an absolute path outside the root was always rejected and still is. Rejection message text and every command's observable behavior are unchanged. (#4653)
