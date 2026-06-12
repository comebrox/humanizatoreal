---
name: omenizator
description: >-
  Curăță tiparele de scriere AI dintr-un text și îl adaptează la limba
  moldovenească autentică (stil Vasile Stati, lexic din Dicționarul
  moldovenesc-român). Folosește când utilizatorul cere „omenește textul",
  invocă /omenizator, sau cere eliminarea „semnelor de AI" / un ton moldovenesc.
license: MIT
version: 1.2.0
author: XAOC
contact: iam@xaoc.bio
repository: https://github.com/comebrox/humanizatoreal
created: 2026
---

# Omenizator — Humanizer Moldovenesc

Procedura:
1. citește textul + ia o mostră de glas
2. detectează tiparele AI (`references/tipare.md`)
3. rescrie cu lexic DMR (`references/lexicon-subset.md`, `references/glosar-dmr.md`)
4. verifică: zero fluff, subiect explicit, surse reale, ton moldovenesc

**Reguli dure:** păstrează sensul, schimbă forma; nu inventa cifre/surse.

## Moduri
- **Literar** (implicit): lexic DMR / Stati.
- **Stradal** (`--argou`): listă suplimentară opt-in (`references/argou-chisinau.md`). Intrările ⚠ sînt excluse implicit.
