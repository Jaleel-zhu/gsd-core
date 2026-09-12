---
type: Security
pr: 0
---
**Path containment at every boundary that takes a directory or filename from the command line** — `todo complete` followed a traversal name outside the todos root and moved the file it found there, `check predicate --phase-dir` let a blocking gate return a passing verdict on evidence from a directory the caller chose, and `check decision-coverage-plan` / `check gap-analysis.plan-post` both accepted a phase directory outside the project. All four now validate against their managed root and reject with a usage error before touching the filesystem. (#4327, #4354)
