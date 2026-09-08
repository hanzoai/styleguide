# Commits

A capitalised imperative summary, fifty characters or less, no trailing period.
"Add the missing peer", never "Added" or "Adds". Most commits are the summary
alone.

A body only when the reason is absent from the diff: blank line, wrapped at 72,
saying WHY. The diff already says what. Never enumerate changed files, never
open with "this commit does the following", never restate the summary.

    Give the registry a heap it can name

    Node sizes old-space from the cgroup, so a 1Gi limit meant ~512MB of heap
    and verdaccio died at 522MB with exit 134. Every install in the repos
    pinning this registry failed during each restart.

`log --oneline`, `shortlog`, `rebase -i`, `reflog` and every forge UI show the
subject alone and truncate it. A message that needs scrolling has failed.

No attribution trailers. No generated-by lines. The committer is the author.

## Branches

Work lands on `main`. A branch is a few hours old, not a few weeks, and it is
deleted at merge. No dates in branch names.
