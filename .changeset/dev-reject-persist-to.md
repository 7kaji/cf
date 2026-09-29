---
"cf": patch
---

Reject `--persist-to` on `cf dev` instead of silently ignoring it

`cf dev --persist-to <dir>` previously started the dev server with its default
state directory and no warning. The dev-server delegates do not accept
`--persist-to`, so `cf dev` now fails with `--persist-to is not supported by cf
dev.`, matching the existing `--local` check.
