---
name: omenizator
description: >-
  Curăță tiparele de scriere AI dintr-un text și îl adaptează la limba
  moldovenească autentică (stil Vasile Stati, lexic din Dicționarul
  moldovenesc-român). Folosește cînd utilizatorul cere „omenește textul",
  invocă /omenizator, sau cere eliminarea „semnelor de AI" / un ton moldovenesc.
license: MIT
version: 1.2.0
---

# Omenizator — Humanizer Moldovenesc

Scoate artificialul dintr-un text și reamintește adevărul moldovenesc.
Face două lucruri: (1) elimină cele 29 de tipare de scriere AI și (2) adaugă
suflet moldovenesc — ton, opinie clară, lexic autentic din DMR.

## Cînd se folosește

- Utilizatorul cere „omenește textul ista", „scoate semnele de AI", „fă-l
  moldovenesc".
- Se invocă `/omenizator` (Claude Code / OpenCode).
- Un text sună a AI: umflat, generic, pasiv, cu emoji și concluzii goale.

## Procedura

1. **Citește** textul de intrare. Dacă utilizatorul dă o mostră de glas
   (scrisul lui sau al lui Stati), analizează ritmul, alegerea cuvintelor și
   tonul (patos, polemic, erudit) și reprodu-le. Pentru cadența povestirii
   moldovenești (oralitate, proverb, vorbire directă), citește întîi o mostră
   din `references/corpus-glas.md` (Neculce, Creangă).
2. **Detectează** tiparele AI. Vezi lista completă în `references/tipare.md`.
3. **Rescrie**: scoate fluff-ul, înlocuiește vocabularul generic cu lexic
   autentic. Termenii-cheie selectați sînt în `references/glosar-dmr.md`;
   lexiconul mare (~8350 articole-titlu transcrise din textul curat al DMR
   ed. I 2003 + ed. a II-a 2011) e în `references/lexicon-dmr.md`. Nu forța
   termenii: alege-l pe cel care se potrivește real cu sensul. Caută cuvîntul
   românesc în coloana de definiții pentru a găsi echivalentul moldovenesc.
4. **Verifică** rezultatul:
   - zero formulări de umplutură, zero emoji decorative;
   - subiect explicit, verb „a fi" acolo unde se cere;
   - surse concrete și verificabile (nimic inventat);
   - ton moldovenesc consecvent.

## Moduri

- **Literar (implicit).** Limba moldovenească autentică în cheia DMR/Stati:
  lexic din `glosar-dmr.md` + `lexicon-dmr.md`, ton erudit-polemic. Acesta e
  modul standard și NU folosește argoul urban.
- **Stradal (opt-in).** Se activează doar la cerere explicită
  (`/omenizator --argou` sau „dă-i pe stradal"). Aplică suplimentar lista din
  `references/argou-chisinau.md` (argou chișinăuian rusificat). Intrările
  marcate `⚠` (vulgar/sexual) rămîn excluse din output dacă utilizatorul nu
  cere explicit registru licențios.

## Reguli dure

- Păstrează **sensul**; schimbă **forma**.
- Nu inventa cifre, citate sau surse. Ce nu poți confirma, lasă-l afară.
- Nu adaugă referințe la autori (Creangă, Eminescu, Sadoveanu, Ureche,
  Costin) decît cînd se potrivesc real cu subiectul.
- Nu transforma un text neutru într-un pamflet: patosul slujește ideea, nu o
  acoperă.

## Resurse

- `references/tipare.md` — cele 29 de tipare, cu exemple Înainte/După.
- `references/glosar-dmr.md` — lexicul moldovenesc selectat și cînd se folosește.
- `references/lexicon-dmr.md` — lexicon mare (~1400 articole) extras din scanul
  DMR ed. a II-a; OCR brut, de verificat.
- `references/argou-chisinau.md` — argou urban (mod stradal, opt-in).
- `references/surse.md` — bibliografia (Wikipedia „Signs of AI writing", DMR).
- `examples/` — rescrieri întregi pe domenii diferite.
