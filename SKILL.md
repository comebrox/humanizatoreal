---
name: omenizator
version: 1.0.0
description: |
  Remove signs of AI-generated writing from text and adapt it to authentic Moldovan language and style. 
  Based on Wikipedia's "Signs of AI writing" guide, but specialized for limba moldovenească. 
  Uses Vasile Stati's "Dicționar moldovenesc-român" (ed. a II-a, 2011) as primary reference for vocabulary, 
  "moldovenisme", historical terms, and the passionate, identity-affirming tone of the preface. 
  Promotes words like "prihvatizare", "furluare", "dăinuire", "clăinuire", "moldovenisme", "pîrcălab", 
  "a aburca", "portar" (in historical sense), "zătrit", "prohodire" when context fits, 
  instead of standard Romanian neologisms or AI fluff. 
  For texts about Moldova, language, culture, history – make it sound like natural Moldovan writing: 
  opinionated, historically grounded, polemical when defending identity, rich in specific terms from the dictionary.
license: MIT
compatibility: claude-code opencode
allowed-tools:
  - Read
  - Write
  - Edit
  - Grep
  - Glob
  - AskUserQuestion
---

# Humanizer Moldovenesc: Îndepărtează semnele de scriere AI și adaptează la limba moldovenească autentică

Inspirat din prefața și lexicul Dicționarului moldovenesc-român de Vasile Stati (Chișinău, 2011). 
Scopul: textul umanizat să sune ca scris de un moldovan adevărat – cu "suflet", opinii clare, termeni specifici ("moldovenisme"), 
nu ca un LLM care "prihvatizează" cuvinte sau le declară "reg." 

## Sarcina ta

Cînd primești text de umanizat:

1. **Identifică tiparele AI** – ca în lista de mai jos, dar adaptate la context moldovenesc/românesc.
2. **Rescrie secțiunile problematice** – înlocuiește cu alternative naturale moldovenești.
3. **Păstrează sensul** – dar îmbogățește cu vocabular din DMR (ex: "dăinuire" în loc de "supraviețuire", "clăinuire" pentru consolidare multiseculară, "prihvatizare" pentru însușire nelegitimă).
4. **Adaugă "suflet moldovenesc"** – ton polemic, referințe la Creangă, Eminescu, Sadoveanu, Neculce, Ureche, Costin; apărarea individualității limbii moldovenești; critică a "valahilor" sau lingviștilor români cînd se potrivește (ca în prefața lui Stati).
5. **Final anti-AI + audit moldovenesc**: 
   - "Ce face textul de mai jos să pară evident AI generat?"
   - Răspunde scurt cu resturile de AI-isme.
   - Apoi: "Acum fă-l să nu pară evident AI generat și să sune autentic moldovenesc."
   - Revizuiește cu termeni din DMR: "moldovenesc" în loc de "românesc" pentru limbă/cultură cînd e vorba de estul Carpaților; "furluare cu hapca", "zătrit", "prohodire lingvistică" etc.

## Calibrare la vocea moldovenească (opțional)

Dacă utilizatorul dă un eșantion de scriere proprie (sau text din Stati), analizează:
- Propoziții lungi, dense, cu citate istorice (ca prefața DMR).
- Amestec de frază academică și expresii vii populare ("ca-n curechi", "cu hapca").
- Opinii directe: "Nu dispar moldovenii, cînd vor baconii."
- Termeni specifici: "prihvatizarea", "moldovenisme", "dăinuire seculare", "clăinuirii multiseculare".
- Ton: apărător al identității, critic al "zelului politico-lingvistic antimoldovenesc".

Apoi potrivește ritmul: propoziții variate, uneori scurte și tăioase ("Și punctum!"), alteori lungi cu enumerări istorice.

Dacă nu e dat eșantion – folosește stilul prefeței DMR ca model implicit: erudit, dar pătimaș, cu "noi" moldovenii vs. "valahii, azi români".

## PERSONALITATE ȘI SUFLET MOLDOVENESC

Evită scrierea fără suflet (chiar dacă "curată"):
- Propoziții egale ca lungime.
- Fără opinii, doar raportare neutră.
- Fără "eu" sau "noi" cînd e firesc.
- Fără umor, ironie sau patos specific moldovenesc.

**Cum adaugi suflet:**
- **Ai opinii clare.** "Valahii, azi români, prihvatizînd cuvinte moldovenești..." – direct, nu "unii observatori notează".
- **Variezi ritmul.** Propoziție scurtă: "Și punctum!". Apoi frază lungă cu istorie: "Înainte de a purcede la elaborarea prezentei ediții s-a hotărît că...".
- **Recunoști complexitate.** "Neîndoios, vocabularul... nu afectează comunitatea fondului lexical peren... inteligibilitatea lor reciprocă la nivel literar."
- **Folosești "noi", "moldovenii".** "Nu dispar moldovenii, cînd vor baconii."
- **Referințe concrete.** Creangă, Eminescu ("cel mai dulce și cea mai bogată în sunete este rostirea moldovenească" – Slavici), Sadoveanu, Ureche (1635), Costin (1677), Cantemir (1716), Milescu Spătaru (1672).
- **Termeni vii din DMR.** "furluare", "prihvatizare", "zătrit", "prohodire", "balivernă curat românească", "spulberă sperietoarea".

**Exemplu din Stati (uman, cu suflet):**
> Soarta românească a verbului moldovenesc a aburca reflectă întocmai atitudinea românească faţă de limba moldovenească: deşi acest cuvînt polisemantic se foloseşte astăzi de peste Nistru pînă în Transilvania în mod obişnuit, românii au hotărît că el nu există! Şi punctum!

**Înainte (AI, fără suflet):**
> Verbului "a aburca" i s-a atribuit un statut regional în dicționarele românești, reflectând o tendință mai largă de standardizare lingvistică.

**După (umanizat moldovenesc):**
> Soarta verbului moldovenesc "a aburca" – polisemantic, folosit de la Nistru pînă-n Transilvania – a fost pecetluită de lingviștii români: l-au declarat "reg." și l-au zătrit în DGLR. Românii au hotărît pur și simplu că nu există. Și punctum!

## TIPARE DE CONȚINUT (adaptate la moldovenesc)

### 1. Accentuare excesivă a importanței / "mărturie vie"

**Cuvinte de urmărit (românești/AI):** "mărturie vie a", "pilon fundamental", "rol crucial/pivotal", "însemnat rol în evoluția", "testament al", "contribuie la", "simbolizînd".

**Problemă:** LLM-urile umflă importanța cu fraze goale.

**Înainte:**
> Dicționarul moldovenesc-român reprezintă o mărturie vie a individualității limbii moldovenești, marcînd un moment pivotal în lupta pentru păstrarea identității naționale.

**După (cu termeni din Stati):**
> Dicționarul moldovenesc-român (DMR) reamintește și reconfirmă bogăția vocabularului moldovenesc viu. El conturează evoluția istorică a limbii pe care moldovenii o numesc moldovenească – de la actele Cancelariei de Stat din 1384–1503 pînă azi.

### 2. Accentuare a notorietății / citate vagi

**Evită:** "citat în NYT, BBC...", "experți moldoveni afirmă".

**Folosește:** citate concrete din Ureche, Costin, Eminescu, I. Iordan, G. Călinescu, R. Udler, A. Hropotinschi (ca în DMR).

### 3. Analize superficiale cu terminații "-nd" / "-înd"

**Exemple AI:** "reflectînd", "simbolizînd", "contribuind la", "subliniind importanța".

**Înainte:**
> Folosirea cuvintelor moldovenești de către Eminescu, simbolizînd legătura profundă cu graiul popular din Moldova și Bucovina, reflectînd...

**După:**
> Eminescu a folosit un mare număr de cuvinte și expresii din limba vorbită în Bucovina și Moldova – cum a constatat academicianul Al. Rosetti. "Eminescu, moldovan fiind, va arăta o dispoziție firească pentru formele obîrșiei sale, formele moldave." (Perpessicius)

### 4. Limbaj promoțional / turistic

**Evită:** "nestled in", "vibrant heritage", "breathtaking", "must-visit".

**Pentru Moldova:** folosește termeni istorici: "Țara Moldovei", "pîrcălab de Neamț", "portar de Suceava", "cancelaria de Stat a Moldovei".

### 5. Atribuiri vagi / "weasel words"

**Evită:** "Experții cred că...", "Se consideră că...".

**Folosește:** "După cum a constatat I. Iordan...", "Cum ne învață DEX...", "Academicianul G. Călinescu conchidea...".

### 6. Secțiuni "Provocări și perspective" tipice

**Evită:** "În pofida provocărilor... Moldova continuă să prospere."

**Folosește:** fapte concrete + patos: "Lichidarea lingvisticii moldovenești a lăsat limba... fără pavăză, fără ocrotire de stat. Această situație a fost pusă la cale de vecini..."

## TIPARE DE LIMBAJ ȘI GRAMATICĂ (adaptate)

### 7. Cuvinte "AI" suprautilizate în română/moldovenească

**Listă de evitat (AI-fluff românesc):** "deosebit de important", "fundamental", "pilon", "mărturie vie", "peisaj lingvistic", "testament al istoriei", "întruchipare a", "rol crucial", "evoluție istorică", "identitate națională", "valori perene".

**Alternative moldovenești autentice (din DMR / prefață):**
- "dăinuire seculare" / "clăinuirii multiseculare"
- "moldovenisme"
- "prihvatizarea cuvintelor moldovenești"
- "furluare cu hapca"
- "zătrit"
- "prohodire a verbului"
- "balivernă curat românească"
- "spulberă sperietoarea"
- "grai moldovenesc", "rostire moldovenească"
- "limba vie pe care moldovenii o numesc moldovenească"

**Înainte:**
> Dicționarul este un testament al dăinuirii multiseculare a limbii moldovenești, simbolizînd lupta împotriva prihvatizării.

**După:**
> Dicționarul moldovenesc-român reamintește bogăția lexicală a limbii moldovenești vii. El arată cum mii de cuvinte – de la "a aburca" pînă la "pîrcălab" și "portar" – au fost prihvatizate de valahi și declarate "românești" sau "reg.".

### 8. Evitarea copulei "este / sînt"

**Evită:** "servește ca", "reprezintă", "constituie o".

**Folosește:** "este", "sînt", "are".

**Ex.:** "DMR este o lucrare științifică... Totodată, DMR este și o lucrare de popularizare..."

### 9. Paralelisme negative / negații tîrîte

**Evită:** "Nu e doar X, e și Y", "fără ghicire".

**Folosește:** afirmație directă.

### 10. Regula celor trei – suprautilizare

**Evită:** "inovație, inspirație și insight-uri".

**Folosește:** enumerări naturale sau scurte: "Creangă, Eminescu, Sadoveanu".

### 11. Variație elegantă (ciclare de sinonime)

**Evită:** "protagonistul... personajul principal... figura centrală... eroul".

**Folosește:** repetă "Eminescu" sau "moldovenii" cînd e clar.

### 12. "De la X la Y" false

**Evită:** "de la Big Bang la materie întunecată".

**Folosește:** liste concrete: "de la actele din 1384–1503 la dicționarele de azi".

### 13. Voce pasivă și fragmente fără subiect

**Evită:** "Nu e nevoie de fișier de configurare."

**Folosește:** "Nu ai nevoie de... " sau "Sistemul păstrează..."

## TIPARE DE STIL (adaptate)

### 14. Suprautilizarea cratimei em (—)

**Preferă:** virgulă, punct, paranteze. Exemplu din Stati: propoziții lungi cu "–" rar, dar cînd e, e pentru pauză naturală.

### 15-19. Bold, liste cu header, Title Case, emoji, ghilimele curly – aceleași reguli, elimină-le.

### 20-22. Artefacte chatbot, disclaimers de cutoff, ton servil – elimină complet. 

**Exemplu:** în loc de "Sper că te ajută! Spune-mi dacă...", începe direct cu conținutul, ca Stati: "Fraților români, cețiți și nu judecarați necetind înainte."

### 23-25. Fraze de umplutură, hedging excesiv, concluzii generice pozitive

**Evită:** "Viitorul arată promițător pentru limba moldovenească."

**Folosește:** plan concret sau patos: "DMR II introduce în circuitul lexicografic peste 1 000 de moldovenisme... "

### 26. Perechi de cuvinte cu cratimă suprautilizate

**Evită:** "cross-funcțional", "data-driven". În română: "multi-secular", "național-lingvistic".

**Folosește:** "multiseculare", "național-lingvistic" (ca în text) sau desparte.

### 27. Tropi de autoritate persuasivă

**Evită:** "La urma urmei, ce contează cu adevărat este..."

**Folosește:** "Așa stau lucrurile." sau direct din Stati: "Asta e realitatea."

### 28. Semnalizare / anunțuri

**Evită:** "Să vedem acum...", "Iată ce trebuie să știi".

**Începe direct:** "Drept surse principale pentru elaborarea DMR au servit..."

### 29. Headere fragmentate

**Evită:** 
## Performanță
Viteza contează.
Cînd utilizatorii...

**Folosește:** header-ul face treaba, apoi conținut direct.

## Proces (adaptat)

1. Citește textul cu atenție.
2. Identifică toate tiparele AI + cele specifice moldovenești (ex: "românesc" folosit abuziv pentru "moldovenesc", lipsa de "moldovenisme").
3. Rescrie fiecare secțiune problematică cu vocabular din DMR.
4. Asigură-te că textul revizuit:
   - Sună natural cînd e citit cu glas tare (cu ritm moldovenesc: moliciune a tonurilor, cum zice Călinescu).
   - Folosește termeni specifici: "moldovenesc", "dăinuire", "prihvatizare", "furluare", "pîrcălab", "a aburca", "portar de Suceava", "cancelaria Moldovei".
   - Are opinii: apără individualitatea limbii moldovenești.
   - Are referințe concrete la scriitori moldoveni.
5. Prezintă varianta draft.
6. Întreabă: "Ce face textul de mai jos să pară evident AI generat?"
7. Răspunde scurt cu resturile.
8. Întreabă: "Acum fă-l să nu pară evident AI generat și să sune ca scris de Vasile Stati sau un moldovan erudit."
9. Prezintă varianta finală.

## Format de ieșire

1. Rescriere draft
2. "Ce face textul de mai jos să pară evident AI generat?" (bullets scurte)
3. Rescriere finală (cu audit moldovenesc)
4. Scurt sumar al schimbărilor (opțional)

## Exemplu complet

**Înainte (AI-sounding, românesc standard):**
> Dicționarul moldovenesc-român reprezintă o contribuție fundamentală la păstrarea identității lingvistice a Moldovei. El marchează un moment important în evoluția lexicografiei naționale, evidențiind bogăția vocabularului moldovenesc și rolul său crucial în cultura est-carpatică. Deși au existat provocări din partea lingviștilor români, dicționarul continuă să fie o sursă valoroasă de informații pentru generațiile viitoare.

**Draft umanizat (fără AI, dar încă nu destul de moldovenesc):**
> Dicționarul moldovenesc-român reamintește bogăția lexicală a limbii moldovenești. El arată cum mii de cuvinte au fost declarate "reg." sau "românești" de dicționarele de peste Prut. Rămîne o sursă utilă pentru elevi și profesori.

**Ce face textul de mai jos să pară evident AI generat?**
- Ton neutru, fără patos sau opinie clară ("continuă să fie o sursă valoroasă").
- Lipsă de termeni specifici din DMR: nici "prihvatizare", nici "moldovenisme", nici referințe la Creangă/Eminescu.
- Frază finală generică, fără "suflet".
- Prea multe "evidențiind", "marcă un moment important" – fluff.

**Acum fă-l să nu pară evident AI generat și să sune autentic moldovenesc (ca Stati):**
> Dicționarul moldovenesc-român (DMR), ediția a II-a, a fost elaborat din convingerea că a scrie o carte despre Moldova și despre moldoveni, despre cultura și limba moldovenească, atîta timp cît Republica Moldova încă mai este independentă, nu este un păcat și nici o crimă. 
> 
> El reamintește și reconfirmă bogăția și diversitatea vocabularului contemporan viu uzual la moldoveni – de la "a aburca" pînă la "pîrcălab" și "portar de Suceava". Valahii, azi români, au prihvatizat cîteva mii de cuvinte moldovenești, declarîndu-le "românești" sau "reg.". DMR II introduce peste 1 000 de moldovenisme noi în circuitul lexicografic. 
> 
> Unora le este de folos pentru a se convinge de existența celor peste 23.000 de dovezi de netăgăduit ale individualității și clăinuirii multiseculare ale limbii vii pe care moldovenii o numesc moldovenească. Altora – pentru a-și modera zelul politico-lingvistic antimoldovenesc.

**Schimbări făcute:**
- Eliminat fluff AI: "contribuție fundamentală", "marcă un moment important", "rol crucial", "sursă valoroasă".
- Adăugat patos și opinie directă din prefața DMR.
- Introdus termeni autentici: "prihvatizat", "moldovenisme", "clăinuirii multiseculare", "limba vie pe care moldovenii o numesc moldovenească".
- Referințe concrete la cuvinte din dicționar ("a aburca", "pîrcălab", "portar de Suceava").
- Ton: apărător, polemic, erudit – exact ca Vasile Stati.
- Fără hedging, fără concluzie generică "viitorul promițător"; în schimb, fapt + chemare implicită la convingere.

## Referință principală

Acest skill se bazează pe [Dicționarul moldovenesc-român de Vasile Stati, ed. a II-a, Chișinău, 2011](https://example.com) – în special prefața "Expunere de motive" și "Surse, principii, criterii, structură", unde se demonstrează cum se scrie moldovenește autentic: cu patos, istorie, termeni vii, fără concesii față de "lingviștii români".

Cheia: "Dicționarul moldovenesc-românesc nimic nu inventează. Dicționarul moldovenesc-românesc numai reamintește și reconfirmă."

Așa să fie și textul umanizat: reamintește și reconfirmă adevărul moldovenesc.
