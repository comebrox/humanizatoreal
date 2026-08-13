# Changelog

All notable changes to this project are documented here. Format based on
[Keep a Changelog](https://keepachangelog.com/); versioning follows SemVer.

## [1.3.0] - 2026-08-13
### Changed
- **Direcție lexicon inversată** (`declanșator RO comun → termen md`). Rescrierea
  pornește din textul standard; agentul caută declanșatorul, nu termenul md.
- `references/lexicon-subset.md` rescris: format tabel nou, notă de sens de căutare,
  secțiune „Acoperire insuficientă" cu regulă de fallback obligatorie.
- `references/glosar-dmr.md` redus la pointer canonic către `lexicon-subset.md`
  (elimină dubla sursă de adevăr pentru lexic).
- `SKILL.md` — pasul 3 formalizează căutarea prin declanșator + regula
  „nu inventa / nu forța" cînd niciun declanșator nu se potrivește.
- `README.md` — actualizat pentru a reflecta `glosar-dmr.md` ca pointer, nu sursă.

### Added
- **Prag de densitate lexic DMR** în `SKILL.md`: max. ~1 termen la 150 cuvinte de
  output; text tehnic/administrativ/juridic — lexic DMR aproape absent.
- **Livrabil obligatoriu**: tabel de audit (tipar → remediu → termen DMR folosit)
  cerut la fiecare rulare, nu doar la cerere sau doar în `examples/`.
- Regulă „text deja curat" — dacă nu se găsesc tipare AI, textul rămîne neatins
  în loc de rescriere forțată.
- Protecție explicită pentru conținut intangibil: nume proprii, citate exacte,
  cod, unități de măsură, terminologie tehnică fixă.
- A doua confirmare explicită a utilizatorului pentru activarea intrărilor ⚠
  din registrul stradal — `--argou` singur nu mai e suficient.
- Secțiune „Trigger phrases" și convenție `read_file references/...` în `SKILL.md`.

### Rationale
Direcția veche (md → ro) forța agentul să pornească din DMR, cu acoperire reală ~0
pe orice text în afara celor 12 sensuri seed. Fără prag de densitate și fără tabel
de audit obligatoriu, rescrierile nu erau reproductibile — de-asta era nevoie de
verificare manuală după fiecare rulare. Această versiune tratează ambele cauze:
direcția de căutare corectă (#1/#2) și trasabilitatea/determinismul livrabilului
(#3/#4).

## [1.2.0] - 2026-06-12
### Added
- Author metadata (SKILL.md frontmatter, README, LICENSE, CITATION.cff).
- IP governance: NOTICE, AUTHORS, SPDX headers, dual-license note (code MIT, data/docs CC BY-SA 4.0).
- `references/lexicon-subset.md`: curated, transformed subset of the DMR lexicon with source references.
- English README with centered header and before/after example.
### Changed
- Lexicon strategy: ship a transformed subset + source pointers instead of the full verbatim lexicon (copyright-safe).
- Renamed `references/lexicon-dmr.md` → `references/lexicon-subset.md`.

## [1.0.0] - 2026
### Added
- Initial standardized skill repo: SKILL.md, references/, examples/, governance files.
