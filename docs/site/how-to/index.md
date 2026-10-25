# How-to guides

Task recipes. Each assumes sibling checkouts of this repo and of the platform
repos it patches.

## Change the language

Edit the YAML fragment and rerun the crate's tests: the fragments are the source of truth, so a semantic change is a data diff that reviewers can read.

## Add a fragment kind

Add the file under `data/` and include it in the crate root; engines pick new fragment kinds up through `Language`, not through a new Rust API.
