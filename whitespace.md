# Whitespace

A file that arrives with the wrong indent width shows up as whole-file noise in
a diff, burying the change that was actually made. That is why this page exists
— not taste, but that a reviewer should be able to see what changed.

**What each language is indented with.** Counted across the estate, not chosen
here:

| Language | Indent | Decided by |
|---|---|---|
| Go | tab | `gofmt` |
| Rust | 4 spaces | `rustfmt` |
| Python | 4 spaces | PEP 8 |
| TypeScript, JavaScript, JSX, TSX | 2 spaces | this guide |
| Shell, YAML, JSON | 2 spaces | this guide |
| Makefile | tab | make requires it |

**Where a language has a canonical formatter, it decides and this page only
records what it does.** `gofmt` indents Go with tabs; there is no setting and no
discussion. A guide that disagreed would only be a guide people remember to
ignore. Run the formatter rather than matching it by hand: `gofmt -l` naming a
file is the same information as a review comment, and it arrives first.

**Two spaces and not four for the brace languages**, because they nest deeply —
a component inside a provider inside a router — and four spends the line on the
left margin. Python does not nest that way, reads better with four, and every
Python tool assumes it.

**Editing an existing file, match the file.** A file with two widths in it is
worse than a file with the wrong one: the first is unreadable, the second is
merely not our style. Reformat in a commit of its own — a change of substance
hidden inside a reindentation cannot be reviewed, which is exactly when a
mistake gets through.

**LF, and a newline at the end of the file.** A missing final newline makes the
last line show as changed the next time anyone touches it.

**No trailing whitespace**, with one exception: inside a Markdown paragraph two
trailing spaces are a line break, so leave those alone.
