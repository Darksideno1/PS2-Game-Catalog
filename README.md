# PS2 Game Catalog

**PlayStation 2 Game Library — USER v0.1 BETA**

A portable Windows application for browsing PlayStation 2 games and managing your personal collection. Built with **WPF / .NET 8** and a local **SQLite** database, with a clean English-language interface.

## Download

The USER portable ZIP is distributed through [GitHub Releases](https://github.com/Darksideno1/PS2-Game-Catalog/releases).

**Public release pending:** The first downloadable release is being prepared. Only the USER package will be published in this repository.

**File:** `PLAYSTATION_2_GAME_LIBRARY_USER_v0.1_BETA.zip`  
**System:** Windows 10 / 11, 64-bit  
**Installation:** Portable, self-contained; no separate .NET installation is needed.

## Features

- **Game Catalog:** Search by title and filter by region, language, and release type.
- **Regions & Releases:** View regional editions, disc serials, release information, and supported languages.
- **My Collection:** Track separate **Physical** and **Digital** entries, including multiple copies of a game.
- **Physical Inventory:** Track original case, cover, disc, and manual completeness and condition.
- **Digital Inventory:** Save digital file format, storage size, and collection notes.
- **Dashboard:** View collection information, total digital storage, and missing front covers.
- **Front Covers:** Display optional images from a local folder, matched by PS2 disc serial.
- **Import / Export:** Create SQLite backups, restore data, and import or export collection records.
- **Settings & Help:** Configure media folders, application options, and consult the in-app guide.

## Getting Started

1. Download the **USER** ZIP from [Releases](https://github.com/Darksideno1/PS2-Game-Catalog/releases).
2. Extract the **entire** ZIP into a folder where you have write permission, for example `C:\Games\PS2-Game-Catalog\`.
3. Launch `USER\PlayStation2GameLibrary.exe`.
4. The game catalog is initialized on first launch; your personal collection is stored locally.

**Do not run the application directly from the ZIP.** The USER package contains no ADMIN executable or catalog-maintenance controls.

### Folder Layout

```text
PS2-Game-Catalog/
├── USER/
│   ├── PlayStation2GameLibrary.exe
│   ├── database/
│   └── data/
├── Data/
│   └── catalogue.db       (created on first launch)
├── Config/
└── Media/
    └── Covers/
```

The download also contains a user guide, a source-data validation report, version information, and third-party notices.

## Optional Cover Images

Place your own front-cover files in `Media\Covers\`, or choose another media location in **Settings**.

Use a serial from one of the game's linked regional releases as the filename:

```text
Media/Covers/SLUS-20946.jpg
Media/Covers/SLES-52541.png
```

Formats: **JPG, JPEG, PNG, WebP**. Missing images are handled automatically; covers are not downloaded from the internet or bundled in the public package.

## Backups and Updating

Your collection is saved in `Data\catalogue.db`. **Back up this file before updating or reinstalling.** You can also use the built-in **Import / Export** backup function.

To update an existing portable installation:

1. Make a backup of `Data\catalogue.db`.
2. Preserve your existing **Data**, **Config**, and **Media** folders.
3. Replace the USER application files and bundled source-data files with those from the newer ZIP.

Extracting the software into a new folder starts a separate local collection; it does not synchronize your existing one automatically.

## Beta Status

This is a **beta** release. The Windows build and automated smoke tests have passed, but real-world issues may still appear. Individual game titles, languages, or regional release associations may need corrections.

## Credits and Third-Party Metadata

The bundled catalog uses metadata from [GameDB-PS2](https://github.com/niemasd/GameDB-PS2), with supplemental description and genre information from the [Open PS2 Loader CFG Database](https://github.com/Thecat1080/PS2-OPL-CFG-Database). Consult the included `THIRD_PARTY_METADATA.txt`, `METADATA_SOURCE_LICENSE_GPL-3.0.txt`, and other distribution notices for source information and license terms.

*PlayStation* and *PlayStation 2* are trademarks of Sony Interactive Entertainment. This project is independent and is not affiliated with or endorsed by Sony.

---

**Public distribution: USER only.** The ADMIN program, private project source code, and personal collection database files are not published here.