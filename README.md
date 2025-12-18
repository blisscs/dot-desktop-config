# Dot Desktop Config

This project stores a collection of .desktop files, one for each desktop application. These files define how applications appear in the desktop environment, including icons, names, and launch commands.

## Installation

To use these .desktop files, you need to make them available to your desktop environment. The standard location is `~/.local/share/applications/` for user-specific applications.

### Static Linking

For static linking, you can create hard links to the files in this folder to the applications directory. This ensures that changes in this folder are reflected in the applications directory without duplicating files.

To statically link a .desktop file:

```bash
ln /path/to/this/folder/app.desktop ~/.local/share/applications/app.desktop
```

Replace `/path/to/this/folder` with the actual path to this directory, and `app.desktop` with the name of the file.

After linking, you may need to restart your desktop session or run `update-desktop-database` to refresh the desktop entries.

## Adding New Entries

To add a new .desktop file, place it in this directory. Ensure it follows the XDG Desktop Entry Specification.