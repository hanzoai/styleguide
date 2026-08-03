# styleguide — ARCHIVED 2026-08-03, do not revive

**Org:** hanzoai  ·  **Ecosystem:** hanzo
**Origin:** https://github.com/hanzoai/styleguide.git
**Status:** archived. Read-only. Do not un-archive and do not make public.

## Why this was archived

`js.md` is the **Airbnb JavaScript Style Guide** — prose, section anchors and
code examples reproduced from https://github.com/airbnb/javascript — with no
LICENSE file and no credit to Airbnb anywhere in the repo.

Airbnb's guide is MIT licensed, `Copyright (c) 2012 Airbnb`. MIT permits the
copying; what it requires is that the copyright notice and permission notice
travel with it. Neither did.

The provenance is not in doubt. Every anchor in our `js.md` appears verbatim in
Airbnb's README — `references--prefer-const`, `references--disallow-var`,
`references--block-scope`, `es6-object-shorthand`, `es6-object-concise`,
`objects--grouped-shorthand` — along with the `atom` / `addValue` example, the
`const`/`let`/`var` rationale text and the "⬆ back to top" navigation.

The tell is in the object-shorthand example. Airbnb's original uses Star Wars
names; ours renamed `lukeSkywalker` → `miyamotoMusashi` and the surrounding
keys to a samurai theme, but left **`anakinSkywalker`** sitting in the "good"
block, referencing a variable our version never declares. It is a copy with a
find-and-replace run over it, and an incomplete one.

`js.md` also lifts MDN prose without credit — "JavaScript has allowed trailing
commas in array literals since the beginning, and later added them to object
literals (ECMAScript 5) and most recently (ECMAScript 2017) to function
parameters" is MDN's sentence. MDN is CC-BY-SA, which requires attribution
*and* share-alike. That is a second uncredited source, and a copyleft one.

## Why archived rather than fixed

Restoring Airbnb's MIT LICENSE and adding a NOTICE was the other option. It was
rejected: the repo had essentially no original value to justify carrying a
permanent third-party attribution obligation. Archiving removes the obligation
instead of complying with it. Nothing was copied into another repo, because
that would have moved the problem rather than solved it.

Mitigating fact, for the record: the repo was **private** throughout. MIT's
notice condition attaches to distribution of copies, and there was no public
distribution. This was an internal-hygiene failure, not a public breach — but
it would have become one the moment the repo was flipped public.

## What was genuinely ours (nothing is lost)

- **The Zen of Hanzo** (`README.md`) — the ten principles: Orthogonality,
  Smallness, Consistency, Composability, Completeness, Dimensionality, Agility,
  Reflect, Clarity, Focus. 100% Hanzo-authored and the only substantial
  original content here. **Already preserved** in `hanzoai/hanzo.app` at
  `src/components/zen/ZenPrinciples.tsx` and `ZenManifesto.tsx`.
- **"We omit semicolons"** (`js.md` §1.1) — a genuine Hanzo house rule, two
  lines. Belongs in a linter config, not a prose document.
- `react.md` — one line preferring hooks over class components. 2019-era advice,
  now simply how React is written.
- `git.md` — empty. A heading and nothing else.

Not carried into `hanzoai/design`: that repo is the *visual* design system —
tokens, color, type, spacing, brand — which is a different concern from code
style. Nothing here belonged there.

## If you want a Hanzo JavaScript style guide

Write one, from scratch, as lint rules rather than prose. A style guide that
cannot be enforced by CI is a document people cite in review and otherwise
ignore. Do not start by pasting someone else's guide.
