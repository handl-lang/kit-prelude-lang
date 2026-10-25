# kit-prelude-lang

The canonical eval-path `Language` as data — the ADR-0044 §6 end state.

## What it is

This crate embeds the authored YAML fragment files that *are* the language:
`tokens`, `grammar`, `eval`, `ast`, `globals`, `capabilities` and friends. There is
no Rust grammar and no Rust evaluator here — loading the crate yields a
`Language` value the engines interpret.

## Modules
- `data/*.yaml` — the authored fragments: `ast`, `eval`, `globals`, `capabilities`, `caps`, tokens/grammar
- crate root — `include_str!`s the fragments and exposes the assembled `Language`


## Start here

- **Reference** — [public API](/kit-prelude-lang/reference/)
- **How-to** — [task recipes](/kit-prelude-lang/how-to/)
- **Explanation** — [design and rationale](/kit-prelude-lang/explanation/)

No tutorials: this repo is a building block used from Rust. End-to-end
walkthroughs live with the product that composes it — see the
[Handl platform](/handl/).
