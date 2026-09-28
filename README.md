# pickify

The public support and privacy site for **Pickify — Randomizer**, served by GitHub Pages
from `docs/` on `main`.

```
https://ivnsjdev.github.io/pickify/            landing page
https://ivnsjdev.github.io/pickify/privacy/    privacy policy — App Store Connect, App Information
https://ivnsjdev.github.io/pickify/support/    support and FAQ — App Store Connect, version page
```

Every URL ends in a trailing slash, because `privacy/index.md` is served at `/privacy/`
and a request without the slash may 404. Both URLs are also compiled into the app, in
`Sources/Core/SupportContact.swift`, where Guideline 5.1.1(i) requires the policy to be
reachable from inside it — so once a build ships carrying one, it must never 404 again.

These pages replace `pickifyappsupport.github.io/pickify-app/`. That site must stay up for
as long as builds pointing at it are installed.

The pages are written from the app's own source, never from a template: every sentence is
a claim about the binary. Re-verify them whenever Pickify gains an SDK, a permission, a
stored key, or a change in purchase terms — see the `app-store-pages` skill.
