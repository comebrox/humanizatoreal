---
name: omenizator
description: >-
  Curăță tiparele de scriere AI dintr-un text și îl adaptează la limba
  moldovenească autentică (stil Vasile Stati, lexic din Dicționarul
  moldovenesc-român). Folosește când utilizatorul cere „omenește textul",
  invocă /omenizator, sau cere eliminarea „semnelor de AI" / un ton moldovenesc.
  Suportă mod literar (implicit) și stradal (--argou).
license: MIT
version: 1.4.0
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
   - păstrează sensul original 100% — nu inventa, nu adăuga fapte noi, nu exagera.
   - ton: direct, concis, fără fluff, fără hedging („ar putea", „în general").
   - ritm natural: propoziții de lungimi variate, ca în glasul moldovenesc autentic (inspirat din Neculce, Creangă, Stati).
4. **Aplică modul** — vezi Moduri mai jos.
5. **Verifică și livrează obligatoriu tabelul de audit** — vezi Livrabil obligatoriu.

**Reguli dure (nu le încălca niciodată):**
- Păstrează sensul intact.
- Nu inventa surse, cifre sau citate.
- Nu atinge nume proprii, citate exacte, cod, unități de măsură sau terminologie tehnică fixă.
- Nu adăuga emoji, bold mecanic, liste simetrice forțate.
- Nu încheia cu „Succes!", „Sper că te ajută" sau platitudini.
- Dacă textul nu are tipare AI detectabile la pasul 2, nu forța rescrierea — raportează „zero tipare găsite" și lasă textul neatins.

## Prag de densitate (lexic DMR)
- Lexicul DMR nu e obligatoriu per output — e o injecție punctuală, nu un strat aplicat uniform.
- Aplică un termen DMR doar dacă înlocuiește natural un cuvînt/sens deja prezent în text (nu adăuga propoziții doar ca să încapă un arhaism).
- Prag orientativ: max. 1 termen DMR la ~150 cuvinte de output. Peste acest raport, oprește injecția lexicală — restul rescrierii se face doar prin eliminare de tipare + ritm (`references/corpus-glas.md`).
- Text tehnic/administrativ/juridic: lexic DMR aproape absent — ritmul și eliminarea fluff-ului fac toată treaba.
- Dacă niciun termen din `lexicon-subset.md` nu are potrivire naturală în text, nu injecta nimic — asta e un rezultat valid, nu un eșec.

## Livrabil obligatoriu
La finalul fiecărei rescrieri, output-ul include un tabel de audit (nu doar textul rescris):

| # tipar | remediu aplicat | termen DMR folosit (dacă e cazul) |
|---|---|---|

- Dacă zero tipare găsite și zero lexic aplicat: rândul e „—", cu mențiune explicită „text deja curat, neatins".
- Acest tabel nu e opțional — e cerut la fiecare rulare a skill-ului, indiferent de lungimea textului.

## Moduri
- **Literar** (implicit): stil erudit, cu rădăcini istorice, lexic DMR / Stati, ton demn și precis.
- **Stradal** (`--argou`): listă suplimentară opt-in (`references/argou-chisinau.md`). Intrările ⚠ (vulgare/sexuale) sînt excluse implicit; se activează doar la a doua confirmare explicită a utilizatorului.

## Referințe (încărcare la cerere)
- tipare complete → `read_file references/tipare.md`
- lexiconul DMR (Master Index v3.1.0) → `read_file references/lexicon-subset.md`
- argou chișinăuian (opt-in) → `read_file references/argou-chisinau.md`
- exemple de glas natural → `read_file references/corpus-glas.md`
- surse și metodologie → `read_file references/surse.md`

Skill structurat modular: `SKILL.md` conține procedura; detaliile stau în `references/` pentru încărcare la cerere (eficiență token).

## Trigger phrases
- „omenește textul ăsta"
- „/omenizator"
- „fă-l să sune ca un moldovan adevărat / ca Vasile Stati"
- „elimină semnele de AI din textul următor"
- „rescrie în registru stradal chișinăuian --argou"

După rescriere, poți întreba utilizatorul dacă vrea ajustări (mai literar / mai stradal / mai scurt / mai polemic) — tabelul de audit rămâne obligatoriu indiferent de ajustare.
