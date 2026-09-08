# .github

Organisation-level files for [PixelKit-Labs](https://github.com/PixelKit-Labs). Nothing here is
code, and nothing here ships.

| Path | What it does |
| :--- | :--- |
| `profile/README.md` | Renders as the organisation landing page at [github.com/PixelKit-Labs](https://github.com/PixelKit-Labs). This is the only file in this repository anyone reads by accident. |
| `LICENSE` | MIT, matching every other repository in the organisation. |

## Editing the profile

`profile/README.md` is the org page. GitHub renders it from the default branch, so a push is a
publish: there is no preview and no staging.

Two things it should keep saying, because they are the questions that otherwise arrive as issues:

- **A development build is required.** PixelKit cannot run in Expo Go, and that is the single most
  common reason someone gets nowhere.
- **It degrades rather than fails.** 13 of the 32 hooks work on any Android device; the rest report
  `unsupported` where the silicon is absent. Without that sentence the project reads as useful to
  far fewer people than it is.

The banner is referenced from `pixelkit-sdk` at its raw URL rather than copied here, so there is one
image to change rather than two that can disagree.

## What does not belong here

Community health files placed in this repository apply to every repository in the organisation that
does not define its own. `CONTRIBUTING.md`, `SECURITY.md` and the issue templates deliberately live
in [`pixelkit-sdk`](https://github.com/PixelKit-Labs/pixelkit-sdk) instead, because they are specific
to it: its contributing guide is about the parity check and the documentation contract, and its
issue template asks for the device and the `source` value a hook returned. A repository-agnostic
version of either would be too vague to be worth reading.
