# Oragent Updates

Public release manifest for the [Oragent](https://pypi.org/project/oragent/) CLI.

Clients read `manifest.json` from this repository (served via GitHub
Pages) to discover the latest published version on each channel.

## Files

- `manifest.json` — current version per channel.
- `appcast-macos.xml` *(coming soon)* — Sparkle appcast for the macOS app.

## Usage

End users don't interact with this repository directly — the Oragent CLI
queries it in the background and notifies users when a new version is on
PyPI.

Install / upgrade Oragent:

    pipx install oragent          # first time
    pipx upgrade oragent          # later

## Schema

`manifest.json` exposes one record per release channel:

- `version`        — latest published version on PyPI
- `pypi_name`      — package name on PyPI (always `oragent`)
- `min_python`     — minimum Python required
- `released_at`    — UTC ISO 8601 timestamp
- `notes_url`      — link to the GitHub Release notes
- `yanked`         — whether the version is withdrawn

## Reporting issues

Please open issues on the main project repository, not here.
