# Dainvo Office language packs

Spelling (Hunspell), hyphenation (Hyphen) and thesaurus (MyThes) data for
Dainvo Office on macOS, Windows and Linux.

You don't need to download anything from here by hand. In Dainvo Office, open
**Review > Languages** (or Tools > Options > Language Settings > Writing Aids >
Download more languages), tick the languages you write in and press Apply.
They are in use straight away, without a restart.

## How it works

- Each release holds a signed `index.json` (and `index.json.sig`) plus the
  packs that are new or changed in that release. Dainvo Office always reads
  the index from the latest release.
- `index.json` is signed with an Ed25519 key, and lists the SHA-256 of every
  pack. Dainvo Office refuses a list that is not correctly signed, an older
  list than one it has already seen, and any pack whose checksum does not
  match.
- Packs are zip files with a `pack.json` and the standard dictionary files.
  They are installed per user, in the Dainvo Office profile folder.

## Sources and licences

The data comes from the LibreOffice
[dictionaries](https://git.libreoffice.org/dictionaries) repository; the
exact commit is in each `index.json`. Every pack keeps its original README,
COPYING and licence files in `licenses/`, and its licence is listed in
`index.json`. Licences differ by language (for example SCOWL, LGPL, GPL, MPL,
BSD-style, WordNet).
