<p align="center"><img src=".github/hero.svg" alt="styleguide" width="880"></p>

# Style Guide

The conventions every repo follows, in one place. Brand-neutral on purpose: the
same guide governs `hanzoai`, `zooai` and `luxfi`, because one set of
conventions across the estate is the point.

- [Commits](git.md) — the message, and what a branch is for
- [Naming](naming.md) — first principles, no compound words, one name per concept
- [Comments and documentation](prose.md) — what code does, not how it got here
- [Architecture](architecture.md) — one way, addresses, what you do not build
- [TypeScript and the web](typescript.md) — `@hanzo/gui`, tokens, packages
- [Go](go.md) — the driver, the ORM, typed ops, identity
- [Whitespace](whitespace.md) — indent width by language, and who decides it

## The short version

One and only one way to do everything. Composable, orthogonal, complete. Name it
what it is. Write as little code as the job needs, and delete what the job no
longer needs. No backwards compatibility, no shims, no second implementation
kept alive to avoid moving callers.

Comments say what the code does. The log holds the history.

Never build auth. Never put a secret in source. Never fake a control.

## Licence

[CC0 1.0 Universal](LICENSE) — dedicated to the public domain. Copy any of
it into your own repo's instructions, adapt it, ship it, no attribution
asked. A convention that costs a licence check to follow does not spread,
and these are worth more the further they travel. `llms.txt` indexes the
guides for machine readers.

## Contributing

Open a PR against `main`. A convention earns its place by removing a decision
someone would otherwise make twice.
