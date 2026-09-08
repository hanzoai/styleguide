# Architecture

**One and only one way to do everything.** Two ways is two things to keep in
agreement, and they will disagree. When you find a second way, delete it rather
than documenting which to prefer.

**Decomplect.** Separate what a thing does from when it is allowed, what a value
is from where it lives, policy from mechanism. Braided concerns cannot be tested
or replaced independently.

**Composable, orthogonal, complete.** A primitive is complete on its own and
composes with its siblings without knowing them. Prefer composition to
inheritance and wrapping to extending.

**No backwards compatibility.** No shims, no adapter layers, no `compat`
packages, no `v2` beside `v1`. Move the callers and delete the old path in the
same change. A compatibility surface is a second implementation that nothing
tests.

**Forwards perfection.** Fix the generating primitive, not its hundreds of call
sites. If the same constant is redefined in four files, give it one home first.

## Addresses

`/v1/` and nothing else. Never an `/api/` prefix — the host is already
`api.<domain>`, so `/api/` says it twice. Never a `/v2/`.

A capability answers at its own name: the segment after `/v1/` is the product,
and the package, the CLI verb and the SDK method all read that one name.

## What you do not build

**Never build auth.** No local passwords, no OTP, no reset flows, no session or
token schemes of your own. Identity is Hanzo IAM, embedded natively. One auth,
one gate.

**Never store a secret in source, in an environment default, or in a repo.** No
`process.env.KEY || '<literal>'` — that idiom is how live keys reach public git.
Secrets live in KMS and are read at the moment of use. Hash passwords, always.

**Never run heavy builds on a machine that also serves production.** Builds go
to the cloud build fleet.

## Versions

Bump the patch. `x.y.z` → `x.y.z+1`. A major bump is a decision someone makes on
purpose, never a shortcut around a conflict.

## Tests

Show the tests passing. A claim that something works, without the output, is not
a claim anyone can check. A test that cannot fail is not a test — mutate it once
and watch it go red before trusting it.
