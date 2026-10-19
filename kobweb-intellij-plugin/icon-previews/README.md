# Icon previews

Outlines for every icon in Kobweb's `silk-icons-*` modules. The
[Kobweb IntelliJ plugin](https://github.com/varabyte/kobweb-intellij-plugin) downloads them to show icons in the
editor gutter.

* `manifest.json`: format version, the Kobweb commit the icon lists came from, and the source, checksum, and per-style
  icon counts for each set
* `fa.bin`, `mdi.bin`, `ms.bin`, `lucide.bin`: one file per icon set, in the format described in the plugin's
  `shared/icon-previews-format` module

## Updating

These files are generated, so don't edit them by hand. From the plugin repo, run:

```bash
./gradlew :tools:icon-previews-generator:generate    # optionally -PkobwebRef=<branch, tag, or commit>
```

Then copy the files in `tools/icon-previews-generator/build/icon-previews/data` into this folder, replacing the old
ones.

`generate` also writes contact sheets to `tools/icon-previews-generator/build/icon-previews/sheets`. Look them over
before copying.

## Sources and licenses

The outlines are derived from:

* [Font Awesome Free](https://fontawesome.com/license/free): CC BY 4.0 (icons)
* [Material Design Icons and Material Symbols](https://github.com/google/material-design-icons): Apache 2.0
* [Lucide](https://lucide.dev/license): ISC
