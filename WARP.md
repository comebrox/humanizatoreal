# WARP.md

Fișierul ista dă îndrumări pentru WARP (warp.dev) cînd lucrează cu codul din repo-ul ista.

## Ce-i repo-ul ista

Repo-ul ista e o **iscusință pentru Claude Code** făcută numai din Markdown, care face două lucruri deodată:

1. **Scoate tiparele de IA** – cele 29 de tipare din ghidul Wikipedia „Signs of AI writing"
2. **Adaugă suflet moldovenesc** – ton patimas, termeni din DMR („prihvatizare", „furluare", „dăinuire", „clăinuire", „moldovenisme", „pîrcălab", „a aburca", „portar", „zătrit", „prohodire"), stilul lui Vasile Stati

„Runtime-ul" e `SKILL.md`: Claude Code citește frontmatter-ul YAML (metadate + unelte îngăduite) și instrucțiunile care urmează.

`README.md` e pentru oameni: instalare, întrebuințare, tabelul cu cele 29 de tipare și istoricul versiunilor.

## Fișiere cheie (și cum se leagă)

- `LICENSE` — Licența MIT (Copyright 2026 Vasile Stati inspiration & XAOC implementation)
- `SKILL.md`
  - Definiția adevărată a iscusinței „Humanizer Moldovenesc"
  - Începe cu frontmatter YAML (`---` … `---`) cu `name`, `version`, `description`, `license`, `compatibility`, `allowed-tools`
  - După frontmatter vine promptul redactorului: sarcina, calibrarea la vocea moldovenească, personalitate și suflet, cele 29 de tipare adaptate la context moldovenesc, procesul în 9 pași, formatul de ieșire, exemplu complet
- `README.md`
  - Instrucțiuni de instalare (Claude Code, OpenCode) și folosire
  - Tabel rezumativ cu „29 de tipare" (adaptate: vocabular AI românesc → termeni DMR)
  - Exemplu întreg (Înainte/După cu suflet moldovenesc)
  - Trimiteri la Wikipedia și DMR
  - Istoricul versiunilor

Cînd schimbi comportamentul/conținutul, ține `SKILL.md` drept sursă de adevăr și adu `README.md` la zi ca să rămînă în pas.

## Comenzi des folosite

### Pune iscusința în Claude Code

Recomandat (clonează de-a dreptul în mapa de iscusințe):

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/comebrox/humanizatoreal.git  ~/.claude/skills/omenizator
```

Instalare manuală / actualizare (numai fișierul de pricepere):

```bash
mkdir -p ~/.claude/skills/omenizator
cp SKILL.md ~/.claude/skills/omenizator/
```

### Pentru OpenCode

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

## Cum o „rulezi" (Claude Code / OpenCode)

Cheamă iscusința:

```
/omenizator

[lipește textul tău aici]
```

Cu potrivirea glasului:

```
/omenizator

Iată o mostră din scrisul meu (sau din Stati) pentru potrivirea glasului:
[lipește 2-3 paragrafe]

Acuma omenește textul ista:
[lipește textul de IA]
```

Sau de-a dreptul:

```
Te rog omenește textul ista și adaptează-l la limba moldovenească: [textul tău]
```

## Cum faci schimbări fără să strici

### Versionare (ține-le sincron)

- `SKILL.md` are cîmpul `version:` în frontmatter-ul YAML (acum: `1.0.0`)
- `README.md` are secțiunea „Istoricul versiunilor"

Dacă urci versiunea, schimbă în amîndouă locurile.

### Editarea lui `SKILL.md`

- Păstrează formatarea YAML validă și indentarea în frontmatter
- Ține numerotarea tiparelor stabilă (1–29), fiindcă README și exemplele trimit la aceleași numere
- Cînd adaugi termeni noi din DMR, actualizează lista din secțiunea „Alternative moldovenești autentice"
- Dacă schimbi exemplul complet, asigură-te că arată atît scoaterea AI-ismelor, cît și adăugarea de suflet moldovenesc

### Notarea reparațiilor mai subtile

Dacă schimbi promptul ca să prinzi un mod de greșeală care se repetă (de pildă:
- un AI-ism specific românească/moldovenească scăpat
- o schimbare de ton neașteptată (prea neutru, fără patos)
- lipsa unor termeni cheie din DMR cînd contextul cere)

adaugă o notiță scurtă în istoricul din `README.md` despre ce-ai reparat și de ce.

### Sfaturi pentru mentenanță

1. **Testează cu texte reale** – ia un articol Wikipedia sau un text de blog și verifică dacă ies toate AI-ismele
2. **Compară cu prefața DMR** – cînd nu ești sigur cum sună „moldovenește autentic", citește din Stati
3. **Nu exagera cu „moldovenismele"** – pune-le doar cînd contextul se potrivește (texte despre limbă, cultură, istorie, identitate)
4. **Ține contul de public** – unele texte cer doar curățare de AI, altele cer și adaptare moldovenească; iscusința trebuie să facă amîndouă bine
