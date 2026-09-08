# TypeScript and the web

**The component library is `@hanzo/gui`.** It carries no Radix, no Tailwind and
no shadcn — its primitives are `@hanzogui/*` (accordion, alert-dialog, avatar,
button, card, checkbox, collapsible, context-menu, dropdown-menu …), which are
the ports. A new surface takes `@hanzo/gui`; an old one migrates onto it rather
than vendoring a second set.

**Style with the token layer, not utility classes.** Geometry and colour come
from CSS custom properties — `--header`, `--page-gutter`, `--band`, `--chrome`,
`--pane-edge`, `--pane-round` — so two surfaces share a rhythm instead of each
inventing one. Inline `style` over a token beats a class that hides one.

**Declare a version once.** Workspace dependencies use the catalog protocol
(`"catalog:"`) with the version in `pnpm-workspace.yaml`. A version literal in a
package manifest is a second place for it to drift.

**A feature is a package, not a form you paste in.** A waitlist is
`@hanzo/waitlist`, telemetry is `@hanzo/event`, the logo is `@hanzo/logo`. A
site renders them and owns none of their transport.

**Never fake a control.** A form that reports success without sending anything
is worse than no form. If the endpoint does not exist, the control does not
ship.
