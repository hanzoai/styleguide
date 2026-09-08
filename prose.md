# Comments and documentation

**A comment says what the code does, positively.** It does not narrate how the
code came to be, what it used to do, which incident produced it, or what someone
got wrong. History belongs in the log, not the source.

Delete on sight:

    // Previously this used X, but that broke in production...
    // NOTE: do not remove, we learned this the hard way
    // FIXME(2026-03-04): temporary until the migration

**No defensive or concealing language.** Comments describe behaviour and cite
the spec. They do not editorialise about what is private, what must never be
revealed, or what a reader should not infer.

**Cite the spec, do not restate it.** Point at the HIP or RFC and describe the
behaviour. A comment that re-derives a design is a second copy that will drift.

**No dates in filenames, branches or headings.** A dated file is stale the week
after it is written.

**Prose to a reader is continuous sentences.** Not bullets, not "first/second/
third", no recapitulation of the question. The headline carries the result. If a
sentence survives deletion, delete it.
