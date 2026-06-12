# Humanizer Moldovenesc

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](CHANGELOG.md)
[![Built for](https://img.shields.io/badge/skill-Claude%20Code%20%7C%20OpenCode-7c3aed.svg)](#instalare)

Un skill (`/omenizator`) pentru Claude Code și OpenCode care îndepărtează
semnele de scriere AI dintr-un text și îl adaptează la limba moldovenească
autentică. Bazat pe ghidul Wikipedia „Signs of AI writing" și pe Dicționarul
moldovenesc-român de Vasile Stati (ed. a II-a, 2011).

## Ce face

1. **Scoate tiparele de IA** — cele 29 de tipare (umflarea importanței,
   vocabular generic, pasiv, liste cu emoji, concluzii goale etc.).
2. **Adaugă suflet moldovenesc** — ton clar, opinii directe, lexic din DMR.

Lista completă a tiparelor: [`references/tipare.md`](references/tipare.md).
Lexicul moldovenesc: [`references/glosar-dmr.md`](references/glosar-dmr.md).

## Structura repo

```
humanizatoreal/
├─ SKILL.md              # instrucțiunile skill-ului (slab, cu frontmatter)
├─ README.md
├─ LICENSE               # MIT
├─ CHANGELOG.md
├─ CONTRIBUTING.md
├─ .gitignore
├─ references/
│  ├─ tipare.md          # cele 29 de tipare AI
│  ├─ glosar-dmr.md      # lexic moldovenesc (Stati)
│  ├─ surse.md           # bibliografie
└─ examples/
   ├─ exemplu-dmr.md
   ├─ exemplu-administrativ.md
   └─ exemplu-tehnic.md
```

## Instalare

### Claude Code

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/comebrox/humanizatoreal.git ~/.claude/skills/omenizator
```

### OpenCode

```bash
mkdir -p ~/.config/opencode/skills
git clone https://github.com/comebrox/humanizatoreal.git ~/.config/opencode/skills/omenizator
```

> OpenCode caută și în `~/.claude/skills/`, deci o singură clonare acolo ajunge
> pentru amîndouă uneltele.

## Întrebuințare

```
/omenizator

[lipește textul tău aici]
```

Sau, în oricare unealtă:

```
Te rog omenește textul ista: [textul tău]
```

### Potrivirea glasului

Ca să prindă felul tău de a scrie (sau stilul lui Stati), dă-i o mostră:

```
/omenizator

Iată o mostră din scrisul meu pentru potrivirea glasului:
[lipește 2-3 paragrafe]

Acuma omenește textul ista:
[lipește textul de IA]
```

## Exemple

Vezi rescrieri întregi Înainte/După în [`examples/`](examples/):

- [`exemplu-dmr.md`](examples/exemplu-dmr.md) — text enciclopedic.
- [`exemplu-administrativ.md`](examples/exemplu-administrativ.md) — raport intern.
- [`exemplu-tehnic.md`](examples/exemplu-tehnic.md) — documentație.

## Surse

Vezi [`references/surse.md`](references/surse.md). Pe scurt:

- Wikipedia: „Signs of AI writing" (WikiProject AI Cleanup).
- Vasile Stati, *Dicționar moldovenesc-român*, ed. a II-a, Chișinău, 2011.

## Licență

[MIT](LICENSE)
