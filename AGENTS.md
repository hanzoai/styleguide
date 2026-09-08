# styleguide

**Org:** hanzoai · **Ecosystem:** brand-neutral — hanzoai, zooai, luxfi
**Origin:** https://github.com/hanzoai/styleguide.git

The conventions every repo in the estate follows. Seven documents, indexed by
the README: commits, naming, prose, architecture, TypeScript, Go, whitespace.

Public, `MIT OR Apache-2.0` per HIP-0137. The guides are worth more the further
they travel, so anyone — person or agent — can lift a paragraph into their own
repo's instructions.

`llms.txt` is the machine index. This file is `AGENTS.md` and `LLM.md` and
`CLAUDE.md` are links to it, that way round because a symlink fetched over
`raw.githubusercontent.com` serves its target's *path* rather than its contents,
so the name a bot reaches for has to be the real file.

## Everything here is original

The guide previously shipped `js.md`, which reproduced the Airbnb JavaScript
Style Guide — prose, section anchors and examples — with no LICENSE and no
credit, plus MDN prose under a copyleft licence, also uncredited. That content
is gone. Nothing here is derived from a third-party guide, which is what makes
the licence ours to give.

If you add a section, write it. Do not paste one — a pasted paragraph puts a
licence we cannot see over text we are handing to everyone.

## What belongs here

A convention belongs here when it removes a decision somebody would otherwise
make twice, and when it holds across languages and orgs. Anything true of one
repo belongs in that repo's own LLM.md.

Keep each document short enough to read in full. A guide nobody finishes governs
nothing.
