# admin-stil.md — Strat administrativ moldovenesc (NU din DMR)

> Separat de DMR. Nu e lexic rural/istoric, ci uz real birocratic din Moldova 2020-2026.
> Se aplică DOAR în mod tehnic-curat când utilizatorul cere explicit `stil=admin`.
> Scop: să sune a instituție din Chișinău, nu a traducere București.

## Principiu
Nu introducem cuvinte de tip Creangă pe texte SIA. Doar reformulăm ticsuri administrative greoaie în forme mai directe, folosite în comunicatele reale din MD.

## Glosar administrativ (RO birocratic greoi → MD administrativ viu)

| declanșator (RO birocratic) | reformulare (MD admin) | notă |
|---|---|---|
| plasarea unei actualizări | punerea în producție / lansarea actualizării | "plasarea" e calchiat |
| funcționalului aferent | funcționalitatea care ține de... / partea care se ocupă de... | "aferent" abuzat |
| vă informăm | vă anunțăm | mai direct, uz MD |
| întru executarea | pentru executarea / ca să executăm | arhaic |
| întru asigurarea | ca să asigurăm / pentru a asigura | arhaic |
| se va purcede la | vom trece la / începem | pasiv inutil |
| se va efectua | vom face / se face | pasiv |
| în vederea | pentru / ca să | fluff AI + birocratic |
| în scopul de a | ca să / pentru a | fluff |
| de către | de — sau subiect explicit | pasiv: "de către bancă" → "banca" |
| aferent / aferentă | care ține de / legat de | evitat |
| derularea / desfășurarea | — (șterge) / organizarea | "derularea procesului" → "procesul" |
| survenirea | apariția | |
| parvenirea | primirea | |
| demers | solicitare / adresare | "demers" abuzat în MD birocratic |
| invocăm | menționăm / spunem | |
| prezenta notificare | notificarea asta / notificarea de față | |
| în contextul | în legătura cu / legat de | |
| cu referire la | referitor la / despre | |
| vizavi de | despre / în legătură cu | rusism birocratic |
| la moment | acum / în prezent | rusism: "на данный момент" |
| de la bun început | din start / de la început | |
| pe parcursul | în timpul / cât | |
| în comun cu | împreună cu | |
| de comun acord | am căzut de acord / am agreat | |
| a fost efectuată actualizarea | am actualizat / am pus în producție | subiect explicit |
| funcționalitate de emitere certificat | emiterea certificatelor / cum se emit certificatele | substantivizare excesivă |

## Exemple transformare

**Înainte (birocratic + AI):**
> În vederea asigurării funcționalului aferent emiterii certificatelor, se va purcede la plasarea unei actualizări în SIA CCDE.

**După (tehnic-curat + admin MD):**
> Ca să asigure emiterea certificatelor, echipa pune în producție o actualizare în SIA CCDE.

**Înainte:**
> Vă informăm că funcționalitatea aferentă tipului resident_type va fi disponibilă.

**După:**
> Vă anunțăm că partea care ține de resident_type va fi disponibilă.

## Reguli aplicare
1. Aplică DOAR după `detect_technical_register() == True`
2. Niciodată nu amesteca cu DMR (nu pune `păpușoi` în text despre IBAN)
3. Păstrează termenii tehnici exacți: JSON, IBAN, SIA, CCDE, resident_type, endpoint — nu-i traduce
4. Scurtează propozițiile >22 cuvinte
5. Subiect explicit: cine face ce (echipa, banca, SIA)

## Când NU aplici
- Text narativ / cotidian / caracter → folosește DMR
- Text tehnic dar utilizatorul NU a cerut `stil=admin` → rămâi pe tehnic-curat simplu (doar curățare AI, fără reformulări admin)
