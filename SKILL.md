---
name: omenizator
description: >-
  Curăță tiparele de scriere AI dintr-un text și îl adaptează la limba
  moldovenească autentică (stil Vasile Stati, lexic din Dicționarul
  moldovenesc-român). Folosește când utilizatorul cere „omenește textul",
  invocă /omenizator, sau cere eliminarea „semnelor de AI" / un ton moldovenesc.
  Suportă mod literar (implicit), stradal (--argou) și strat administrativ (stil=admin).
license: MIT
version: 1.4.1
author: XAOC
contact: iam@xaoc.bio
repository: https://github.com/comebrox/humanizatoreal
created: 2026
---

# Omenizator — Humanizer Moldovenesc

**Procedura obligatorie:**

1. **Citește textul de input.** Dacă utilizatorul oferă o mostră proprie de scris sau există context relevant în conversație, ia o mostră de glas din `references/corpus-glas.md` pentru ritm/ton. Dacă nu e disponibilă, mergi mai departe fără — nu o ceri, nu o presupui.
2. **Detectează tiparele de scriere AI** (`references/tipare.md`, 29 semne) — numerotează fiecare tipar găsit.
3. **Rescrie:**
   - elimină tiparele găsite; transformă construcțiile pasive/vagi în active cu subiect explicit („cine face acțiunea?").
   - **Lexic DMR (direcție obligatorie):** caută **declanșatoarele RO comune** din `references/lexicon-subset.md` (Master Index v3.1.0). Dacă găsești potrivire naturală de sens și registru → înlocuiește cu termenul md — **doar** respectând Pragul de densitate de mai jos.
   - dacă **niciun** declanșator nu se potrivește → **nu inventa** termeni DMR și **nu forța** cei existenți pe sensuri nepotrivite. Continuă doar cu eliminarea tiparelor AI + ritm natural.
   - **Strat administrativ (`stil=admin`):** pe texte tehnice/birocratice, dacă utilizatorul cere explicit `stil=admin`, aplică reformulările din `references/admin-stil.md`. Nu amesteca niciodată cu DMR.
   - păstrează sensul original 100% — nu inventa, nu adăuga fapte noi, nu exagera.
   - ton: direct, concis, fără fluff, fără hedging.
   - ritm natural: propoziții de lungimi variate.
4. **Aplică modul** — vezi Moduri mai jos.
5. **Verifică și livrează obligatoriu tabelul de audit**.

**Reguli dure (nu le încălca niciodată):**
- Păstrează sensul intact.
- Nu inventa surse, cifre sau citate.
- Nu atinge nume proprii, citate exacte, cod, unități de măsură sau terminologie tehnică fixă.
- Nu adăuga emoji, bold mecanic, liste simetrice forțate.
- Nu încheia cu „Succes!", „Sper că te ajută" sau platitudini.
- Dacă textul nu are tipare AI detectabile, nu forța rescrierea — raportează „zero tipare găsite" și lasă textul neatins.

## Prag de densitate (lexic DMR)
- Lexicul DMR nu e obligatoriu per output — e o injecție punctuală.
- Prag orientativ: max. 1 termen DMR la ~150 cuvinte de output.
- **Text tehnic/administrativ/juridic:** lexic DMR aproape absent. Omenizarea se face prin ritm + eliminarea fluff-ului. Dacă utilizatorul cere explicit `stil=admin`, se aplică stratul din `references/admin-stil.md` (separat de DMR).
- Dacă niciun termen din `lexicon-subset.md` nu are potrivire naturală, nu injecta nimic — rezultat valid.

## Livrabil obligatoriu
La finalul fiecărei rescrieri, output-ul include un tabel de audit:

| # tipar | remediu aplicat | termen DMR / reformulare admin (dacă e cazul) |
|---|---|---|

- Dacă zero tipare și zero lexic: „text deja curat, neatins".
- Tabelul nu e opțional.

## Moduri
- **Literar** (implicit): stil erudit, lexic DMR / Stati, ton demn.
- **Stradal** (`--argou`): listă opt-in (`references/argou-chisinau.md`). Intrările ⚠ excluse implicit; se activează doar la a doua confirmare explicită.
- **Administrativ** (`stil=admin`): pe texte tehnice, reformulări birocratice din `references/admin-stil.md`. Activare explicită. Nu se amestecă cu DMR.

## Referințe (încărcare la cerere)
- tipare → `read_file references/tipare.md`
- lexicon DMR (Master Index v3.1.0) → `read_file references/lexicon-subset.md`
- strat administrativ → `read_file references/admin-stil.md`
- argou chișinăuian (opt-in) → `read_file references/argou-chisinau.md`
- corpus de glas → `read_file references/corpus-glas.md`
- surse → `read_file references/surse.md`

## Trigger phrases
- „omenește textul ăsta"
- „/omenizator"
- „fă-l să sune ca un moldovan adevărat / ca Vasile Stati"
- „elimină semnele de AI din textul următor"
- „rescrie în registru stradal chișinăuian --argou"
- „stil=admin" / „în stil administrativ moldovenesc"

După rescriere, poți întreba utilizatorul dacă vrea ajustări — tabelul de audit rămâne obligatoriu.
