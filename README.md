# SILL-BILL Blender Extensions

This repository is the static distribution repository for Blender Extensions
published by SILL-BILL. The contents of `docs/` are intended to be served
directly by GitHub Pages and used as a remote repository in Blender.

Extension development and releases remain in each extension's own repository.
This repository contains only the files needed for distribution.

## Available Extensions

### Panda Tool

- Version: 0.8.0
- Blender: 4.2+
- Type: Add-on

### Mixamo Rig Kai

- Version: 0.6.8 Preview
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
6. Find **Panda Tool** or **Mixamo Rig Kai**.
7. Install the extension and enable it if necessary.

## Tested with

- Blender 4.2.23 LTS
- Blender 5.1.1

Panda Tool v0.8.0 adds Convert Names to English for known Bone, Shape Key,
Material and Object names. Its exact-match dictionary supports Japanese,
Simplified Chinese and known English aliases, with 84 / 52 / 31 / 16 mappings.
Unknown names are unchanged, conflicts are skipped, and standard Undo is
supported. Linked Data, Library Overrides and unsafe Bone Driver references
cancel the operation before modification. Existing tools include Remove
Constraints and Panda Apply Modifier. English and Japanese documentation is
available in the source repository. Install or update through GitHub Pages;
v0.7.0 installations can update to v0.8.0 after repository synchronization.

Mixamo Rig Kai v0.6.8 Preview adds the Facial Phase 2 Custom Shape Key
Controller Generator, including target-based slider creation, automatic
Internal IDs, `cs_switch` Knobs, viewport labels, per-mesh Mapping, and safe
Remove / Regenerate persistence.

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
