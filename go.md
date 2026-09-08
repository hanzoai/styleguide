# Go

**SQLite is `github.com/hanzoai/sqlite`, and a consumer never imports an
engine.** Not `mattn/go-sqlite3`, not `modernc.org/sqlite`. Two packages
registering the same driver name panic at `init`, before `main`, with a stack
that names neither offender.

**Pragmas ride `OpenPragma` or `PragmaDSN`, never a hand-written DSN.** The two
backends spell pragmas differently and each silently ignores the other's
spelling, so a hand-written profile is right on one build and evaporates on the
other with no error.

**The ORM is `hanzoai/orm`.** Not gorm.

**Prefer a typed op to a raw handler.** One registration yields the route, the
OpenAPI operation, the MCP tool, the CLI command and the SDK method. An untyped
route yields a route and nothing else — no schema, no prose, no tool, no method.

**Identity is never an input field.** Read the validated principal from the
context. A tenant taken from a request body is a cross-tenant read the caller
asserted for itself.

**An absence is not an answer.** Distinguish "the peer does not exist here" from
"the peer failed": the first may fall back, the second is an outage. A failure
rendered as an empty result is the hardest class of bug to see.
