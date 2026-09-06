# Sourcery review rules — trial repository

These rules mirror `SOUL.md`. After installing the Sourcery GitHub App, add them in **Review Settings → Review rules** for this repository. Sourcery does not currently expose review-rule configuration through its public API.

## Rule 1 — Infrastructure evidence

**Paths:** `**/*.tf`, `**/*.tfvars`, `examples/**`

> Flag Terraform changes that lack appropriate validation evidence, omit expected IAM/cost/data-governance impact, or make irreversible resource changes without migration or rollback notes. Never request secrets or a live plan containing sensitive identifiers.

## Rule 2 — No concealed verification gaps

**Paths:** `**/*`

> Flag claims that a change is complete or verified when the pull request evidence does not show the relevant command and observed result. Ask the author to mark unverifiable work UNKNOWN/INCOMPLETE.

## Rule 3 — Bot accountability boundary

**Paths:** `**/*`

> Flag bot-authored changes that expand permissions, repository access, infrastructure scope, billing impact, data collection or secret handling without an explicit operator decision in the pull request.

## Rule 4 — Public repository hygiene

**Paths:** `**/*`

> Flag credentials, tokens, private contact details, notification addresses, connection strings, sensitive cloud identifiers or generated state that should not be committed to a public repository.
