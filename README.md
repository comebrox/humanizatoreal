<div align="center">

# 🪶 Omenizator

**A Moldovan-language text humanizer** — strips AI writing patterns and rewrites with authentic vocabulary (DMR / Vasile Stati).

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.2.0-blue.svg)](CHANGELOG.md)
[![Skill](https://img.shields.io/badge/type-Claude%20Code%20%2F%20OpenCode-purple.svg)](SKILL.md)
[![Lexicon](https://img.shields.io/badge/lexicon-curated%20subset-orange.svg)](references/lexicon-subset.md)

</div>

---

## What it does

Takes text that "smells like AI" and returns it human: no fluff, explicit subject, Moldovan tone, and real sources.

| Before (AI) | After (humanized) |
|---|---|
| "It is important to note that the solution offers a range of benefits." | "The solution brings three concrete wins." |
| "Within this process, we will proceed to analyze..." | "Let's analyze, one by one." |

---

## Installation

```bash
git clone https://github.com/comebrox/humanizatoreal.git
# drop the skill into your agent's skills directory
```

## Usage

```bash
/omenizator                 # literary mode (default, DMR vocabulary)
/omenizator --argou         # add Chișinău street register (opt-in)
```

Procedure: **read + voice sample → detect patterns → rewrite with DMR vocabulary → verify** (zero fluff, explicit subject, real sources).

---

## Modes

| Mode | Default | Source | Sensitive content |
|---|---|---|---|
| **Literary** | ✅ Yes | DMR / Stati | — |
| **Street** (`--argou`) | ❌ Opt-in | internet compilation | ⚠ entries excluded by default |

---

## Repository structure

<details>
<summary>Show full structure</summary>

```
humanizatoreal/
├─ SKILL.md              # instructions + YAML frontmatter
├─ README.md
├─ LICENSE               # MIT
├─ NOTICE
├─ AUTHORS
├─ CITATION.cff
├─ CHANGELOG.md
├─ CONTRIBUTING.md
├─ references/
│  ├─ tipare.md          # 29 AI patterns
│  ├─ glosar-dmr.md      # confirmed preface terms
│  ├─ lexicon-subset.md  # curated, transformed subset (+ source refs)
│  ├─ argou-chisinau.md  # street mode, opt-in
│  ├─ corpus-glas.md     # Neculce / Creangă pointers (no verbatim copy)
│  └─ surse.md
└─ examples/
   ├─ exemplu-dmr.md
   ├─ exemplu-administrativ.md
   └─ exemplu-tehnic.md
```

</details>

---

## References

- [AI patterns (1–29)](references/tipare.md)
- [DMR glossary](references/glosar-dmr.md) · [Curated subset](references/lexicon-subset.md)
- [Voice corpus](references/corpus-glas.md) · [Sources](references/surse.md)

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) — how to add a pattern, a term, or an example.

## Author & originality

**Omenizator** is an original concept by **XAOC** (2026) — a Moldovan-language humanizer combining AI-pattern removal with the DMR / Vasile Stati lexicon. No prior equivalent was found at the time of creation.

- Author: XAOC · iam@xaoc.bio
- Repository: https://github.com/comebrox/humanizatoreal

If you use or build on this idea, please cite it (see [CITATION.cff](CITATION.cff)).

## Licensing

- **Code** (`SKILL.md` logic, scripts): MIT — see [LICENSE](LICENSE)
- **Reference data & docs** (`references/`, README): CC BY-SA 4.0
- Third-party lexicon sources retain their own rights — see [references/surse.md](references/surse.md)
