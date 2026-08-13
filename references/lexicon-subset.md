# Lexicon DMR — subset transformat (seed)

> **Scop:** perechi `declanșator RO comun → termen moldovenesc` utile pentru rescrierea de text (humanizer) — se caută sensul standard în text și se înlocuiește cu termenul md.
> **Statut:** SEED (~12 termeni confirmați din prefață). Țintă: 200–400 termeni, extrași și reformulați din cele două ediții DMR aflate în arhiva proprie (2003, 2011).
> **Copyright:** selecția, reformularea și scopul sînt contribuție originală (XAOC, 2026). Cuvintele-titlu și sensurile rămîn fapte lexicale; drepturile asupra dicționarului-sursă rămîn ale autorilor originali (V. Stati). Vezi `surse.md`.

## Criteriu de selecție
1. Termenul are valoare stilistică pentru un ton moldovenesc autentic (nu doar arhaism rar).
2. Are un echivalent român clar, folosibil într-o rescriere.
3. Nu e vulgar/argou (acelea stau în `argou-chisinau.md`, opt-in).

## Format
`| declanșator (RO comun) | termen (md) | notă de uzaj | sursă |`

> **Sens de căutare (important):** rescrierea pornește din textul standard, nu din DMR.
> Agentul caută în text cuvântul din coloana **declanșator** (sensul comun, RO standard)
> și, dacă găsește potrivire naturală de sens și registru, îl înlocuiește cu **termenul md**.
> Coloana „termen (md)" NU e punct de plecare — e destinația substituției.

## Subset (seed)
| declanșator (RO comun) | termen (md) | notă de uzaj | sursă |
|---|---|---|---|
| însușire abuzivă, acaparare | prihvatizare | ton polemic; pentru critică socială | DMR ed. II 2011, prefață |
| luare cu forța / pe nedrept | furluare (cu hapca) | registru oral, expresiv | DMR ed. II 2011, prefață |
| nimicit, distrus definitiv | zătrit | intensitate mare; evită în registru neutru | DMR ed. II 2011, prefață |
| înmormântare; (fig.) lichidare | prohodire | figurat: „prohodirea unui cuvînt" | DMR ed. II 2011, prefață |
| a urca cu efort | a aburca | atestat DU 1929, CADE 1931 | DMR ed. II 2011, prefață |
| dregător peste un ținut/cetate | pîrcălab | istoric; context medieval | DMR ed. II 2011, prefață |
| mare dregător militar al Moldovei | portar de Suceava | istoric | DMR ed. II 2011, prefață |
| piftie, aspic | răcituri | culinar; uz moldovenesc curent | DMR ed. II 2011, prefață |
| struguri | poamă | uz moldovenesc curent | DMR ed. II 2011, prefață |
| (om) blond, bălai | balan / bălae / bălăior | descriptiv | DMR ed. II 2011, prefață |
| urcior, vas de lut cu gît îngust | burlui | concret, obiect | DMR ed. II 2011, prefață |
| persistență, continuitate | dăinuire / clăinuire | abstract; ton elevat | DMR ed. II 2011, prefață |

## Acoperire insuficientă (#2 — regulă de fallback, nu de completare forțată)
- Statut actual: **12/200–400 termeni țintă**. Pe orice text care nu atinge exact aceste
  12 sensuri, acoperirea lexicală e ~0 — asta e statutul real, nu o eroare de rulare.
- **Regulă pentru SKILL.md pasul 3:** cînd niciun declanșator din acest tabel nu are
  potrivire în text, agentul **nu inventează** termeni DMR din memorie proprie și **nu
  forțează** cei 12 existenți pe sensuri nepotrivite. (`references/glosar-dmr.md` e doar
  pointer către acest fișier — nu conține termeni separați de verificat.) Rescrierea
  continuă doar prin eliminare de tipare AI + ritm (`corpus-glas.md`) — omenizarea nu
  depinde exclusiv de lexic.
- Extinderea reală a tabelului (spre 200–400) rămîne un workflow separat, pe sursă
  primară (DMR Vol. 1+2), nu o completare ad-hoc în timpul unei rescrieri de text.

## De completat (workflow de extindere reală)
- Sursă: `Dicționar moldovenesc-românesc (Stati) Vol.1 + Vol.2` (în workspace).
- Pas: extrage ~200–400 candidați → reformulează nota de uzaj cu cuvinte proprii →
  marchează pagina-sursă → completează coloana „declanșator" cu sensul RO comun →
  **NU** copia definiția verbatim.
- Validare: fiecare rînd trebuie să aibă declanșator + termen md + notă proprie + sursă.
