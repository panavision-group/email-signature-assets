# Panavision Group — email signature assets

This repository hosts image assets embedded in Panavision Group employee
email signatures. Files here are served directly to email clients via
`raw.githubusercontent.com`, so this repo **must remain public** for the
images to load.

## ⚠️ Do not rename, move, or delete files in this repository

Every file path here is hard-coded into live email signatures deployed to
employees through IT's centrally managed signature system. Changing a path
breaks the image in every signed email from that moment on.

| File | Used in | Updated by |
|---|---|---|
| `panalux-latest.png` | Panalux group signature ("Proudly supporting" credits banner) | Automated daily — do not edit by hand |

## How updates arrive

The banner is regenerated once a day by a GitHub Actions pipeline in a
separate **private** repository (`panavision-group/panalux-signature-banner`),
which scrapes the latest Panalux-serviced credits from panavision.com,
renders the poster strip, validates it, and pushes the finished PNG here
only when it has changed. If any step fails, nothing is pushed and the
previous image continues to serve — stale, never broken.

Manual commits to this repository should never be necessary. If the banner
looks wrong, fix it in the private code repository and let the pipeline
publish the result.
