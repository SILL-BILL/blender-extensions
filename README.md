# SILL-BILL Blender Extensions

This repository is the static distribution repository for Blender Extensions
published by SILL-BILL. The contents of `docs/` are intended to be served
directly by GitHub Pages and used as a remote repository in Blender.

Extension development and releases remain in each extension's own repository.
This repository contains only the files needed for distribution.

## Available Extensions

### Panda Tool

- Version: 0.1.0 Preview
- Blender: 4.2+
- Type: Add-on

## Repository URL

```text
https://sill-bill.github.io/blender-extensions/index.json
```

Use this URL when adding the SILL-BILL Blender Extensions repository to
Blender.

## Installation

1. Open Blender.
2. Go to **Edit > Preferences > Get Extensions**.
3. Open **Repositories** and choose **Add Remote Repository**.
4. Enter `https://sill-bill.github.io/blender-extensions/index.json`.
5. Sync the repository.
6. Find **Panda Tool**.
7. Install the extension and enable it if necessary.

## Tested with

- Blender 4.2.23 LTS
- Blender 5.1.1

For Panda Tool v0.1.0, repository synchronization, extension discovery,
installation, enablement, and Create Anchor execution have been verified
through the published GitHub Pages repository.

## GitHub Pages

This repository is published through GitHub Pages using **Deploy from a
branch**:

- Branch: `main`
- Folder: `/docs`

Repository endpoint:

```text
https://sill-bill.github.io/blender-extensions/index.json
```

## Updating the repository manually

Place the original release ZIP in `docs/` without repacking it, then regenerate
the static index with Blender's official CLI:

```powershell
blender --factory-startup --command extension server-generate --repo-dir=docs --html
```

Commit the ZIP and both generated index files only after validating the
package metadata and archive checksum.

## License

Repository infrastructure is licensed under GPL-3.0-only.
Individual extensions retain their respective licenses.
