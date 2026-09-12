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

The remote repository URL will be added here after GitHub Pages has been
enabled and the published `index.json` URL has been verified. Do not use a
guessed URL as the production repository endpoint.

## Installation

After the repository URL has been published:

1. Open Blender.
2. Go to **Edit > Preferences > Get Extensions**.
3. Open **Repositories** and choose **Add Remote Repository**.
4. Enter the published `index.json` URL.
5. Find **Panda Tool**, install it, and enable the extension if necessary.

## GitHub Pages setup

Configure GitHub Pages in the repository settings after the initial commit has
been pushed:

- Source: **Deploy from a branch**
- Branch: **main**
- Folder: **/docs**

This repository intentionally does not use a GitHub Actions Pages deployment
workflow at this stage.

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

