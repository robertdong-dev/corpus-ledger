# corpus-ledger — public anchor chain

Public, append-only timestamp anchor for the private `corpus` repository.

**Each line = date + corpus commit hash + entity ID. Three fields, nothing else** —
no filenames, no paths, no commit messages, no semantic columns (anti-scraping:
the chain must reveal *rhythm and volume*, never content).

Verify chain: any line's hash → ask the corpus owner to prove that commit exists
(signed) → signature checks against the fingerprint bound on the anchor page.
Timestamp authority: GitHub server-side receive time (the "second clock").

Line format: `YYYY-MM-DD | <full commit sha> | entity:xiaoyuan-dong`

Rules: signed commits only; never rebase/force-push; one line per corpus push.
