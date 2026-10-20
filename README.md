# kit-prelude-lang

`handl-kit-prelude-lang` — the canonical **eval-path `Language` as data**
(the ADR-0044 §6 end state, eval fragment set).

Embeds the authored YAML fragment files (`tokens`, `grammar`, `eval`,
`types`, `ast`, `caps`, `options`, `lexer_rules`, `transforms`, `globals`)
and merges them into a `handl_language::Language` via
`language_from_yaml()` — enough to lex, parse, desugar, and eval `.hnl`.

Tooling fragments (`lints.yaml`, `lsp.yaml`) and the kit-composition
manifests (`data/kits/*`) live upstream in
[`kit-data-prelude`](https://github.com/handl-lang/kit-data-prelude), which
composes this crate and layers them on top to produce the full canonical
`Language` plus the `DataKit` assembly machinery.

Sibling-repo deps are git dependencies (`branch = "main"`); the `[patch]`
tables in the workspace `Cargo.toml` resolve them from sibling checkouts
for local development.
