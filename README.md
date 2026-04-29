# Humanizer Moldovenesc

O iscusință pentru Claude Code și OpenCode care îndepărtează semnele de scriere AI din text și îl adaptează la limba moldovenească autentică. Bazat pe ghidul Wikipedia „Signs of AI writing" și pe Dicționarul moldovenesc-român de Vasile Stati (ed. a II-a, 2011).

## Instalare

### Claude Code

Clonează de-a dreptul în mapa de iscusințe:

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/comebrox/humanizatoreal.git  ~/.claude/skills/omenizator
```

Sau copiază manual fișierul de pricepere dacă ai deja repo-ul tras:

```bash
mkdir -p ~/.claude/skills/omenizator
cp SKILL.md ~/.claude/skills/omenizator/
```

### OpenCode

Clonează de-a dreptul în mapa OpenCode:

```bash
mkdir -p ~/.config/opencode/skills
git clone https://github.com/comebrox/humanizatoreal.git  ~/.config/opencode/skills/omenizator
```

Sau copiază manual:

```bash
mkdir -p ~/.config/opencode/skills/omenizator
cp SKILL.md ~/.config/opencode/skills/omenizator/
```

> **Notă:** OpenCode caută și în `~/.claude/skills/`, deci o singură clonare în `~/.claude/skills/omenizator/` ajunge pentru amîndouă uneltele.

## Întrebuințare

### Claude Code

```
/omenizator

[lipește textul tău aici]
```

### OpenCode

```
/omenizator

[lipește textul tău aici]
```

Sau spune-i modelului de-a dreptul, în oricare unealtă:

```
Te rog omenește textul ista: [textul tău]
```

### Potrivirea glasului moldovenesc

Ca să prindă felul tău de a scrie sau stilul lui Vasile Stati, dă-i o mostră:

```
/omenizator

Iată o mostră din scrisul meu (sau din Stati) pentru potrivirea glasului:
[lipește 2-3 paragrafe]

Acuma omenește textul ista:
[lipește textul de IA]
```

Iscusința va analiza ritmul, alegerea cuvintelor, tonul (patos, polemic, erudit) și le va reproduce în rescriere, folosind termeni din DMR: „prihvatizare", „furluare", „dăinuire", „clăinuire", „moldovenisme", „pîrcălab", „a aburca", „portar de Suceava", „zătrit", „prohodire".

## Privire de ansamblu

Iscusința face două lucruri:

1. **Scoate tiparele de IA** – cele 29 de tipare din lista de mai jos (umflarea importanței, vocabular generic, pasiv, liste cu emoji, concluzii goale etc.)
2. **Adaugă suflet moldovenesc** – ton patimas, opinii clare, termeni specifici din DMR, referințe la Creangă, Eminescu, Sadoveanu, Ureche, Costin; apărarea individualității limbii moldovenești.

Se sprijină pe:
- Ghidul Wikipedia „Signs of AI writing" (WikiProject AI Cleanup)
- Prefața și lexicul Dicționarului moldovenesc-român de Vasile Stati (Chișinău, 2011)

### Gîndul de bază

> „Modelele mari de limbă ghicesc statistic ce cuvînt urmează. De aceea trag spre răspunsul cel mai probabil, care se potrivește la cît mai multe cazuri."

Și din Stati:

> „Dicționarul moldovenesc-românesc nimic nu inventează. Dicționarul moldovenesc-românesc numai reamintește și reconfirmă."

Așa lucrează și iscusința: scoate artificialul și reamintește adevărul moldovenesc.

## 29 de tipare prinse (cu exemple Înainte/După)

### Tipare de conținut

| # | Tiparul | Înainte | După |
|---|---------|---------|------|
| 1 | **Umflarea însemnătății** | „marcînd un moment pivotal în evoluția..." | „a fost înființat în 1989 ca să strîngă statistici regionale" |
| 2 | **Lăudăroșenie cu nume mari** | „citat în NYT, BBC, FT și The Hindu" | „Într-un interviu din 2024 la NYT, ea a spus..." |
| 3 | **Analize superficiale cu -ind** | „subliniind... reflectînd... evidențiind..." | Scoate sau dezvoltă cu surse concrete (Ureche, Costin, Iordan, Călinescu) |
| 4 | **Limbaj de reclamă / turistic** | „cuibărit în pitoreasca regiune" | „e un tîrg în regiunea Gonder" / „Țara Moldovei", „pîrcălab de Neamț" |
| 5 | **Trimiteri vagi** | „Experții cred că joacă un rol crucial" | „După cum a constatat I. Iordan..." |
| 6 | **Șablonul cu greutăți** | „În pofida provocărilor... continuă să prospere" | Spune concret ce greutăți sînt + patos: „Lichidarea lingvisticii moldovenești a lăsat limba fără pavăză..." |

### Tipare de limbă

| # | Tiparul | Înainte | După |
|---|---------|---------|------|
| 7 | **Vocabular de IA (românesc standard)** | „deosebit de important", „fundamental", „pilon", „mărturie vie", „peisaj lingvistic", „testament al istoriei" | Termeni din DMR: „dăinuire seculare", „clăinuirii multiseculare", „moldovenisme", „prihvatizare", „furluare cu hapca", „zătrit", „prohodire" |
| 8 | **Ocolirea lui „a fi"** | „servește drept... prezintă... constituie o" | „este... are... sînt" |
| 9 | **Paralelisme negative** | „Nu-i doar X, e Y", „..., fără ghiceli" | Spune direct ce vrei |
| 10 | **Regula de trei** | „inovație, inspirație și insight-uri" | Enumerări naturale: „Creangă, Eminescu, Sadoveanu" |
| 11 | **Învîrtirea sinonimelor** | „protagonist... personaj principal... figura centrală... eroul" | Repetă cuvîntul cel mai limpede („Eminescu", „moldovenii") |
| 12 | **Intervale false** | „de la Big Bang pînă la materia întunecată" | Liste concrete: „de la actele din 1384–1503 la dicționarele de azi" |
| 13 | **Pasiv și fraze fără subiect** | „Nu e nevoie de fișier de configurare" | Numește cine face: „Nu ai nevoie de...", „Sistemul păstrează..." |

### Tipare de stil

| # | Tiparul | Înainte | După |
|---|---------|---------|------|
| 14 | **Liniuța em (—) în exces** | „instituțiile — nu oamenii — dar asta continuă —" | Preferă virgula, punctul, parantezele |
| 15 | **Aldine peste tot** | „**OKR-uri**, **KPI-uri**" | „OKR-uri, KPI-uri" |
| 16 | **Liste cu titlu în rînd** | „**Performanță:** Performanța a crescut" | Fă propoziție curgătoare |
| 17 | **Titluri Cu Majuscule** | „Negocieri Strategice Și Parteneriate" | „Negocieri strategice și parteneriate" |
| 18 | **Emojiuri** | „🚀 Faza de lansare: 💡 Idee cheie:" | Scoate emojiurile |
| 19 | **Ghilimele crețe** | `a zis „proiectul"` | Folosește ghilimele drepte cînd se cere |
| 26 | **Perechi cu cratimă** | „inter-funcțional, bazat-pe-date" | Lasă fără cratimă perechile obișnuite („multiseculare", „național-lingvistic") |
| 27 | **Poze de autoritate** | „În esență, ce contează e..." | Spune direct: „Așa stau lucrurile." |
| 28 | **Anunțuri de intrare** | „Hai să vedem", „Iată ce trebuie să știi" | Începe cu conținutul: „Drept surse principale..." |
| 29 | **Titluri rupte** | „## Performanță" + „Viteza contează." | Lasă titlul să lucreze singur |

### Tipare de comunicare

| # | Tiparul | Înainte | După |
|---|---------|---------|------|
| 20 | **Resturi de chatbot** | „Sper că te ajută! Spune-mi dacă..." | Scoate de tot. Începe direct ca Stati: „Fraților români, cețiți și nu judecarați necetind înainte." |
| 21 | **Scuze de limită** | „Deși detaliile sînt limitate în sursele disponibile..." | Găsește surse sau șterge |
| 22 | **Ton lingușitor** | „Întrebare grozavă! Ai perfectă dreptate!" | Răspunde de-a dreptul |

### Umplutură și fereală

| # | Tiparul | Înainte | După |
|---|---------|---------|------|
| 23 | **Vorbe de umplutură** | „În scopul de a", „Din cauza faptului că" | „Ca să", „Fiindcă" |
| 24 | **Fereală în exces** | „ar putea posibil eventual" | „poate" |
| 25 | **Încheieri generice** | „Viitorul arată luminos pentru limba moldovenească" | Fapte concrete + patos: „DMR II introduce peste 1 000 de moldovenisme..." |

## Exemplu întreg

**Înainte (AI-sounding, românesc standard):**

> Dicționarul moldovenesc-român reprezintă o contribuție fundamentală la păstrarea identității lingvistice a Moldovei. El marchează un moment important în evoluția lexicografiei naționale, evidențiind bogăția vocabularului moldovenesc și rolul său crucial în cultura est-carpatică. Deși au existat provocări din partea lingviștilor români, dicționarul continuă să fie o sursă valoroasă de informații pentru generațiile viitoare.

**După (omenesc, cu suflet moldovenesc):**

> Dicționarul moldovenesc-român (DMR), ediția a II-a, a fost elaborat din convingerea că a scrie o carte despre Moldova și despre moldoveni, despre cultura și limba moldovenească, atîta timp cît Republica Moldova încă mai este independentă, nu este un păcat și nici o crimă.
>
> El reamintește și reconfirmă bogăția și diversitatea vocabularului contemporan viu uzual la moldoveni – de la „a aburca" pînă la „pîrcălab" și „portar de Suceava". Valahii, azi români, au prihvatizat cîteva mii de cuvinte moldovenești, declarîndu-le „românești" sau „reg.". DMR II introduce peste 1 000 de moldovenisme noi în circuitul lexicografic.
>
> Unora le este de folos pentru a se convinge de existența celor peste 23.000 de dovezi de netăgăduit ale individualității și clăinuirii multiseculare ale limbii vii pe care moldovenii o numesc moldovenească. Altora – pentru a-și modera zelul politico-lingvistic antimoldovenesc.

**Ce s-a schimbat:**
- Eliminat fluff AI: „contribuție fundamentală", „marchează un moment important", „rol crucial", „sursă valoroasă"
- Adăugat patos și opinie directă din prefața DMR
- Introdus termeni autentici: „prihvatizat", „moldovenisme", „clăinuirii multiseculare", „limba vie pe care moldovenii o numesc moldovenească"
- Referințe concrete: „a aburca", „pîrcălab", „portar de Suceava"
- Ton: apărător, polemic, erudit – exact ca Vasile Stati

## Trimiteri

- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) — sursa primară pentru tiparele AI
- [WikiProject AI Cleanup](https://en.wikipedia.org/wiki/Wikipedia:WikiProject_AI_Cleanup)
- [Dicționarul moldovenesc-român de Vasile Stati, ed. a II-a, Chișinău, 2011](https://example.com) — sursa pentru vocabular moldovenesc autentic

## Istoricul versiunilor

- **1.0.0** — Prima ediție: combină curățarea de tipare AI cu adaptarea la limba moldovenească autentică (stil Vasile Stati, termeni din DMR: „prihvatizare", „furluare", „dăinuire", „clăinuire", „moldovenisme", „pîrcălab", „a aburca", „portar", „zătrit", „prohodire")

## Licență

MIT