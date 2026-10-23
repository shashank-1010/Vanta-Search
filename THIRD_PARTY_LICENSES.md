# Third-party licenses

This file lists third-party material in this repository and **what the repository's own files say
about its license**. Nothing here was filled in from memory: where the files contain no license text,
the entry says so. Where a statement comes from general knowledge rather than from the files, it is
labelled **(not from the files, verify)**.

This is not legal advice. Items marked **UNVERIFIED** must be checked by a human before this
repository is distributed publicly.

## Summary

| Asset | License found in the files | Commercial use / redistribution | Attribution required | Status |
|---|---|---|---|---|
| Lato fonts (`cover_letters/OpenFonts/fonts/lato/*.ttf`, 10 files) | SIL Open Font License 1.1, stated in each font's embedded metadata (name IDs 0, 13, 14). **Full license text is not in the repository.** | Cannot be confirmed from the files, because the license text is absent. **(not from the files, verify)** OFL 1.1 is generally understood to allow both when the copyright notice and license accompany the fonts and the Reserved Font Name rules are followed. | Embedded notice: "Copyright (c) 2010-2011 by tyPoland Lukasz Dziedzic (http://www.typoland.com/) with Reserved Font Name "Lato"". Keep the font files and their metadata unmodified. | Needs human check: add the full OFL text |
| Raleway fonts (`cover_letters/OpenFonts/fonts/raleway/*.otf`, 9 files) | SIL Open Font License 1.1, stated in each font's embedded metadata. **Full license text is not in the repository.** | As above: cannot be confirmed from the files. **(not from the files, verify)** | Embedded notice: "Copyright (c) 2010 - 2012, Matt McInerney, Pablo Impallari, Rodrigo Fuenzalida with Reserved Font Name "Raleway"". Keep the font files and metadata unmodified. | Needs human check: add the full OFL text |
| `cover_letters/cover.cls` | **None found.** No license file, no copyright or license header. Its only header is `\ProvidesClass{cover}[2024/04/30 Cover letter class]`. | Unknown | Unknown | **UNVERIFIED, do not distribute until checked** |
| `cover_letters/OpenFonts/` directory as a bundle | **None found** (no README, license or authorship file for the bundle itself). The upstream CHANGELOG describes it as "the original font bundle", which suggests it was copied from an external template. | Unknown | Unknown | **UNVERIFIED, do not distribute until checked** |
| moderncv (LaTeX class used by `cv/main_example.tex`) | **Not bundled.** The file only calls `\documentclass{moderncv}`; users install it from their TeX distribution. No license text in the repository. | n/a (not redistributed here) | n/a | Not bundled; license not verified from the files |
| Job-portal CLIs under `.agents/skills/*/cli/` (freehire, jobbank, jobdanmark, jobindex, jobnet, linkedin) | **No license file or header in any of them.** The README's Acknowledgements credit a third party for "the job search CLI skills" (see below). | If these were written by the original author, they fall under the MIT license in [LICENSE](LICENSE). If any code came from the credited third party, its license is unknown. | Unknown for any third-party-derived part | **UNVERIFIED, do not distribute until checked** |
| npm dependencies declared (not bundled) in those CLIs' `package.json`: `@bunli/core` 0.9.1, `@bunli/utils` 0.6.0, `node-html-parser`, `zod`, `typescript`, `@types/bun` | None in the repository (no `node_modules`, no lockfile, no vendored code). | n/a (downloaded by the user at install time) | Determined by each package, not verified here | Not bundled; not verified |
| LinkedIn test fixtures (`.agents/skills/linkedin-search/cli/tests/fixtures/`) | **None.** They hold verbatim LinkedIn page markup and the text of a real job posting, captured by a third-party contributor (see below). | Unknown. This is LinkedIn's and an employer's content, and the capture was made by automated access. | Unknown | **UNVERIFIED, do not distribute until checked** |

## Details

### Fonts (Lato and Raleway)

Read directly from the font files' `name` tables:

- Lato: `Copyright (c) 2010-2011 by tyPoland Lukasz Dziedzic with Reserved Font Name "Lato". Licensed under the SIL Open Font License, Version 1.1.` License URL field: `http://scripts.sil.org/OFL`.
- Raleway: `Copyright (c) 2010 - 2012, Matt McInerney (matt@pixelspread.com), Pablo Impallari (impallari@gmail.com), Rodrigo Fuenzalida (hello@rfuenzalida.com) with Reserved Font Name "Raleway"`; `This Font Software is licensed under the SIL Open Font License, Version 1.1.` License URL field: `http://scripts.sil.org/OFL`.

Gaps: the OFL's full text is not shipped with the fonts. Before public distribution, obtain the
official OFL 1.1 text from SIL and add it next to the fonts, then confirm from that text what the
license requires. Do not rename or modify the font files (the Reserved Font Names matter).

### `cover.cls`

No copyright or license information exists in the file or beside it. Its origin could not be
determined from the repository. If it was written by the original project author it is covered by
[LICENSE](LICENSE); if it was adapted from another template, that template's license applies and is
unknown. Do not distribute until its origin is established.

### Job-portal CLIs and the credited third party

The README Acknowledgements credit Mikkel Krogholm (https://github.com/mikkelkrogsholm/skills) "for
the job search CLI skills". The repository contains no license text for that work and no marking of
which files derive from it. Treat all `.agents/skills/*/cli/` code as unverified until the origin and
license of that repository have been checked.

### LinkedIn fixtures

`search-cards.json` and `detail-orbis-excerpt.html` contain markup and posting text from LinkedIn,
captured by a contributor using the handle "portapulito" via an automated request, and were part of a
pull request to the original project that was closed without being merged. Their license status and
compliance with LinkedIn's terms are unknown. They are kept only because nothing was deleted without
a decision; consider replacing them with synthetic fixtures.

### Other bundled material

- No images, logos or icons are bundled (the original mascot was removed).
- No vendored third-party source code was found in the repository.
- The freehire documentation mentions an MIT-licensed backend repository (`strelov1/freehire`) that
  is **not** bundled; only its public API is called.
