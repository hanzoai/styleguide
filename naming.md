# Naming

Naming is the hard part, so spend the effort here rather than on the code that
follows from a good name.

**Name from first principles.** Call the thing what it is. Prefer the academic,
scientific or mathematical term the field already agreed on — ancestor,
idempotent, invariant, fixpoint, projection, closure — over a coinage.

**Avoid compound words.** One word if one word will do. `gateway`, not
`gatewaysvc`. A namespace already qualifies its members, so `quasar.RoundSigner`
says what `LuxRoundSigner` was trying to say, without braiding the brand into
the identifier.

**One concept, one name, everywhere.** A value that is `org` in the database is
`org` on the wire, in the client and in the CLI flag. Two names for one thing is
how they drift into two things.

**A name is not a place.** The address a capability answers at, the package it
lives in and the store it opens are three separate facts. Renaming one does not
rename the others, and a store key is never an address.
