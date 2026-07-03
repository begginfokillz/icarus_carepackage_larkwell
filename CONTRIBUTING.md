# Contributing

Thanks for helping out with the Larkwell Care Package mod!

## Reporting a bug or requesting content

Open an [issue](../../issues/new/choose) and pick a template:

- **Bug report** — something isn't working
- **Broke after a game update** — an Icarus weekly update broke it
- **Content / feature request** — ideas for new care packages or items
- **Question / help** — anything else

The more detail (mod version, game week, other mods installed, screenshots), the faster it gets sorted.

## Packaging the mod (for updates)

This mod ships in the current `.EXMODZ` format for [JimK72's Icarus Mod Manager](https://github.com/Jimk72/Icarus_Software). An `.EXMODZ` is just a renamed `.zip` with this layout:

```
Extracted Mods/
    LarkwellCarePackage.EXMOD          (manifest: name, author, version, description...)
LarkwellCarePackage/
    Banner.png
    README.md
    Readme (LarkwellCarePackage_P.pak).txt
    LarkwellCarePackage_P.pak          (the mod itself)
```

To update each week:

1. Build the new `LarkwellCarePackage_P.pak` — one word, `_P.pak` on the end, **no space**.
2. Drop it into the `LarkwellCarePackage/` folder, replacing the old one.
3. Bump `version` in **both** `Extracted Mods/LarkwellCarePackage.EXMOD` and `modinfo.json`.
4. Zip the `Extracted Mods` and `LarkwellCarePackage` folders (they must sit at the **root** of the zip, not inside a wrapper folder) and rename the `.zip` to `LarkwellCarePackage.EXMODZ`.
5. Import + merge via the Mod Manager to test it, then commit.

Only the pak and the version number change week to week — everything else you copy forward.
