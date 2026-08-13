# Changelog

All notable changes to this project are documented here. Format based on
[Keep a Changelog](https://keepachangelog.com/); versioning follows SemVer.

## [1.4.0] - 2026-08-13
### Changed
- **Lexicon upgraded to Master Index v3.1.0 (Production).**
  - ~280 termeni unici, curățați de duplicate RO=MD și generice inutile.
  - Integrat 100 regionalisme vii (grupuri publice 2024-2026) + selecție de înaltă valoare din extracția DMR 1500.
  - Protocol de matching semantic + densitate (~1/150) + non-forțare păstrat și întărit.
- `references/lexicon-subset.md` rescris integral ca fișier de producție.
- `references/glosar-dmr.md` actualizat ca pointer.

### Added
- Domenii clare: Interacțiune Socială, Acțiune Fizică, Gastronomie/Obiecte distinctive, Stări/Polemic, Regionalisme Vii.
- Regula explicită de densitate și de logare a lacunelor pentru Lotul 4.

### Removed
- Toate perechile identice RO=MD și termenii generici (soare, an, foc, etc.) care nu aduceau valoare stilistică.

### Rationale
v3.0.0 conținea ~190 de rânduri aproape identice (RO=MD). v3.1.0 păstrează doar termenii care cresc autenticitatea reală a textului fără a forța arhaisme inutile.

## [1.3.0] - 2026-08-13
### Changed
- Direcție lexicon inversată (`declanșator RO comun → termen md`).
- `references/lexicon-subset.md` rescris: format tabel, notă de căutare, regulă de fallback.
- `references/glosar-dmr.md` redus la pointer.
- `SKILL.md` — pasul 3 formalizează căutarea prin declanșator + regula „nu inventa / nu forța”.
- Prag de densitate, livrabil audit obligatoriu, protecție conținut intangibil, a doua confirmare pentru ⚠.

## [1.2.0] - 2026-06-12
### Added
- Author metadata, IP governance, lexicon-subset initial, English README.
### Changed
- Lexicon strategy: transformed subset + source pointers (copyright-safe).

## [1.0.0] - 2026
### Added
- Initial standardized skill repo.
