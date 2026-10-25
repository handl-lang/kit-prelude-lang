# Explanation

## Why this crate exists

ADR-0044 ends with the language being *data*, not code: a host loads a
`Language` value, and lexing, parsing, transforming, typechecking and evaluation
are all engines over it. This repo is that end state for the canonical kit —
which is why it is a data crate with almost no Rust in it.

## Where it sits

This crate belongs to the `engine-*` family. Plugins, kits and hosts reach it
through the kit's operation slot, so the engine can be swapped without touching a
language definition.

See the [reference](/kit-prelude-lang/reference/) for the API and the
[how-to guides](/kit-prelude-lang/how-to/) for tasks.
