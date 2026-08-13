<div align="center">

# 🪶 Omenizator

**Humanizer de text în limba moldovenească**  
Elimină tiparele de scriere AI și rescrie cu lexic autentic (DMR / Vasile Stati + regionalisme vii).

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.4.0-blue.svg)](CHANGELOG.md)
[![Lexicon](https://img.shields.io/badge/lexicon-~280%20termeni-orange.svg)](references/lexicon-subset.md)
[![Skill](https://img.shields.io/badge/type-Agent%20Skill-purple.svg)](SKILL.md)

**RO → MD** · **Zero forțare** · **Audit obligatoriu**

</div>

---

## Ce face

Primește un text care „miroase a AI” și îl întoarce uman: fără fluff, cu subiect explicit, ton moldovenesc și surse reale.

| Înainte (AI) | După (omenizat) |
|---|---|
| „Este important de menționat că soluția oferă o serie de beneficii.” | „Soluția aduce trei câștiguri concrete.” |
| „În cadrul acestui proces vom proceda la analiza…” | „Hai să analizăm, pe rând.” |

**Lexicon actual:** Master Index v3.1.0 — ~280 termeni unici (DMR + regionalisme vii), direcție `declanșator RO comun → termen MD`, cu regulă strictă de non-forțare.

---

## Instalare

```bash
git clone https://github.com/comebrox/humanizatoreal.git
# plasează skill-ul în directorul de skills al agentului tău
```

## Utilizare

```bash
/omenizator                 # mod literar (implicit, lexic DMR)
/omenizator --argou         # adaugă registru stradal chișinăuian (opt-in)
```

**Procedură fixă:**  
1. Citește textul (+ mostră de glas, dacă există)  
2. Detectează tiparele AI (29 semne)  
3. Rescrie (elimină tipare + injectează MD doar la potrivire naturală)  
4. Livrează **tabel de audit obligatoriu**

---

## Moduri

| Mod | Implicit | Sursă | Conținut sensibil |
|---|---|---|---|
| **Literar** | ✅ Da | DMR / Stati + regionalisme | — |
| **Stradal** (`--argou`) | ❌ Opt-in | Compilație de internet | Intrările ⚠ excluse implicit |

**Densitate lexicală:** max. ~1 termen MD la 150 cuvinte.  
Pe texte tehnice / administrative densitatea e intenționat aproape zero — omenizarea se face prin ritm și curățarea tiparelor AI.

---

## Structura repo-ului

```
humanizatoreal/
├─ SKILL.md                 # procedura + YAML frontmatter (v1.4.0)
├─ README.md
├─ LICENSE · NOTICE · AUTHORS · CITATION.cff
├─ CHANGELOG.md · CONTRIBUTING.md
├─ references/
│  ├─ tipare.md             # 29 tipare AI
│  ├─ lexicon-subset.md     # Master Index v3.1.0 (canonic)
│  ├─ glosar-dmr.md         # pointer → lexicon-subset.md
│  ├─ argou-chisinau.md     # mod stradal (opt-in)
│  ├─ corpus-glas.md        # mostre de ritm (Neculce / Creangă)
│  └─ surse.md
└─ examples/
   ├─ exemplu-dmr.md
   ├─ exemplu-administrativ.md
   └─ exemplu-tehnic.md
```

---

## Referințe rapide

- [Tipare AI (1–29)](references/tipare.md)
- [Lexicon DMR (RO → MD)](references/lexicon-subset.md)
- [Corpus de glas](references/corpus-glas.md) · [Surse](references/surse.md)
- [Changelog](CHANGELOG.md)

---

## Autor & originalitate

**Omenizator** este un concept original al **XAOC** (2026) — humanizer moldovenesc care combină eliminarea tiparelor AI cu lexicul DMR / Vasile Stati. La momentul creării nu exista un echivalent public.

- Autor: **XAOC** · iam@xaoc.bio  
- Repo: https://github.com/comebrox/humanizatoreal

Dacă folosești sau construiești pe această idee, citează-o (vezi [CITATION.cff](CITATION.cff)).

---

## Licențiere

| Componentă | Licență |
|---|---|
| Cod & logică (`SKILL.md`) | [MIT](LICENSE) |
| Date de referință & documentație (`references/`, README) | CC BY-SA 4.0 |
| Surse lexicale terțe (Stati etc.) | Drepturile rămân ale autorilor originali — vezi [surse.md](references/surse.md) |

---

<div align="center">

**Fă textul să sune a om, nu a model.**

</div>
