# TTML Lyrics Database

A collection of TTML lyric files that I've personally synchronized.

## About

I create and synchronize lyrics using **TtmlMaker**, my private Android application fully vibe-coded with Claude, taking inspiration from [amll-tool](https://github.com/amll-dev/amll-ttml-tool) and [Better Lyrics Composer](https://github.com/better-lyrics/composer).

TtmlMaker mostly follows Better Lyrics' TTML formatting conventions.

## Repository Structure

```text
ttml-lyrics-db/
├── ttmlmaker/
│   ├── project/
│   │   └── ISRC.ttmlproj.json
│   └── ISRC.ttml
├── composer/
│   └── ISRC.ttml
├── LICENSE
└── README.md
```

## Directories

### `ttmlmaker/project/`

Contains the original TtmlMaker project files, named using the track's ISRC:

`ISRC.ttmlproj.json`

These files preserve the project data for future editing.

### `ttmlmaker/`

Contains TTML files exported directly from TtmlMaker.

Each file is named using the track's ISRC:

`ISRC.ttml`

### `composer/`

Contains TTML files exported from Better Lyrics Composer.

The TTML files exported from TtmlMaker are imported into Better Lyrics Composer and processed to produce Better Lyrics-compatible TTML. Each file retains the same ISRC-based naming convention:

`ISRC.ttml`

## File Naming

Files use the **ISRC (International Standard Recording Code)** of the corresponding recording as their filename identifier.

| Location | Filename | Description |
|---|---|---|
| `ttmlmaker/project/` | `ISRC.ttmlproj.json` | Original TtmlMaker project |
| `ttmlmaker/` | `ISRC.ttml` | TTML exported directly from TtmlMaker |
| `composer/` | `ISRC.ttml` | Better Lyrics-compatible TTML |

Replace `ISRC` with the actual recording's ISRC.

## License

Files in `ttmlmaker/` and `composer/` are subject to the terms in [`LICENSE`](LICENSE).

The synchronization credit is stored in TTML metadata as a key-value pair with the key `syncedBy`. If a file contains this field (or equivalent), you must preserve its value and keep the credit associated with the lyrics.

If you convert a TTML file to another format, retain the `syncedBy` credit in an equivalent metadata field or, if the format cannot store it, in accompanying documentation. Do not remove or discard the credit during conversion.

This repository's licence applies only to rights I can license in my own contributions, including the synchronization work where legally protectable. **I do not claim ownership of the underlying lyrics.** The lyrics remain subject to the rights of their respective copyright holders. You are responsible for obtaining any additional permissions or licences required to use, reproduce, distribute, adapt, or otherwise exploit the underlying lyrics. Permission under this repository's licence does not replace permission from the original rights holders.
