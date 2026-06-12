# Changelog

Toate schimbările notabile ale acestui skill sînt documentate aici.
Format bazat pe [Keep a Changelog](https://keepachangelog.com/),
versionare [SemVer](https://semver.org/).

## [1.2.0] - 2026-06-12

### Schimbat
- `references/lexicon-dmr.md` — REFĂCUT din textul curat al DMR (transcriere
  furnizată de utilizator, nu OCR): ed. I 2003 + ed. a II-a 2011. ~8350
  cuvinte-titlu unice, 9680 sensuri, cu marcajele de sursă din articol
  (La CADE, I. Creangă, TD, DD etc.) păstrate ca atestare.
- `references/surse.md` — lexiconul nu mai e marcat „OCR brut"; sursa = text
  transcris curat al ambelor ediții.
- `SKILL.md` — pasul 3 trimite la lexiconul curat; eliminat caveatul „OCR brut".

### Adăugat
- `references/corpus-glas.md` — mostre de glas moldovenesc autentic (Ion
  Neculce, *O samă de cuvinte*; Ion Creangă, *Amintiri din copilărie*),
  fragmente din domeniul public + mic glosar de glas. Pentru ritm/ton, nu lexic.
- `SKILL.md` — pasul 1 trimite la corpusul de glas.

### Eliminat
- Reziduurile OCR din lexicon (recunoaștere defectuoasă din scan).

## [1.1.0] - 2026-06-11

### Adăugat
- `references/lexicon-dmr.md` — ~1386 de articole-titlu extrase din scanul DMR
  ed. a II-a (2011). OCR brut, marcat „de verificat".
- `references/argou-chisinau.md` — argou urban chișinăuian (mod stradal,
  opt-in); intrări vulgare marcate `⚠` și excluse implicit.
- Secțiune „Moduri" în `SKILL.md`: literar (implicit) vs. stradal (opt-in,
  `--argou`).

### Schimbat
- `references/surse.md` — link DMR real (moldova1359.md / Internet Archive),
  hartă de surse pe categorii (lexicon, corpus de glas, argou); eliminat
  placeholderul `example.com`.
- `references/glosar-dmr.md` — îmbogățit cu termeni confirmați din prefața DMR
  (prihvatizare, furluare, zătrit, prohodire, pîrcălab etc.).
- `SKILL.md` — procedura trimite la noul lexicon și la cele două moduri.

## [1.0.0] - 2026-06-11

### Adăugat
- `SKILL.md` canonic cu frontmatter (name, description, version, license).
- `references/tipare.md` — cele 29 de tipare AI, numerotate 1–29, grupate pe
  categorii (conținut, limbă, stil, comunicare, umplutură, structură).
