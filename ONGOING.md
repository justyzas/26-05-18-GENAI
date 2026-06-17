# Diena 1: Įvadas į generatyvųjį DI ir Praktiniai naudojimo atvejai

**Data:** 2026-05-18

## Paskaitų laikas ir formatas:

**Kurso pradžia** 2026-05-18
**Kurso pabaiga** 2026-07-15

**Paskaitos vyksta** Pirmadieniais, Trečiadieniais, Ketvirtadieniais 18:00 - 20:30 **išskyrus nedarbo dienas**-

**Pertraukėlė planuojama** 19:30 Trunka 10 min

---

### Teorija

- Susipažinimas
- Kurso apžvalga - 8 savaičių turinys
- Kas yra generatyvusis DI ir **LLM**?

### Platforma vs. Modelis (Svarbiausia dalis)

- **Platforma suteikia**:
  - Paieškos variklio įrankis modeliui;
  - Skirtingus DI modelius jų naudojimui;
  <!-- - Atmintį, personalizavimą; -->
  - Kodo paleidimo įrankius;
  - Leidžia naudotis balso sąsaja
  <!-- - Leidžia susikurti sau agentą -->
  - Leidžia grupuoti informaciją pagal projektą
- **Modelis**:
  Gauna input'ą (tekstą) -> duoda outputą (tekstą)
- ### ChatGPT naudojimas ir praktinės taikymo sritys
  - Techninių kliūčių sprendimai pagal error kodus ir screenshotus;
  - Informacijos apdorojimas ir įvertinimas;
  - Agentų kūrimas;
  - Vertimai į kitas kalbas;
  - Teksto generavimas skirtingiems atvejams;
  - Teksto tono keitimas, koregavimas;
  - Svarbios informacijos atranka iš daug teksto, kito failo;
  - Informacijos struktūravimas;
  - Įvykusio pokalbio transkribcijos analizė ir informacijos sugrupavimas
  - Informacijos paieška internete;
  - Elektroninių laiškų rašymas
  - Įrašų kūrimas (Postų, aprašymų)
  - Kelionių planavimas
  - Promptų kūrimas (inžinerija)
  - Dokumentų kūrimas
- **Generatyvinis DI nėra deterministinis**;

---

### **Diena 2: LLM modeliai ir ekonomika**

- Praeitos paskaitos medžiagos trumpas pakartojimas/apšilimas
- ChatGPT modelių variantai: GPT‑5, GPT‑4.1, GPT‑5‑mini
- Tokenai (žetonai) - Modelio kalba
- Tokenų (žetonų) kainos
- Konteksto langas (matuojamas tokenais)
- Žetonų pagrindu skaičiuojamos kainos: įvesties ir išvesties sąnaudos

https://platform.openai.com/tokenizer

Žetonai (Tokenai):

> Žetonas – tai maždaug skiemuo arba trumpas žodžis. "labas" = 1 žetonas. "sveiki atvykę" = 3 žetonai. Anglų kalba efektyvesnė – lietuvių kalba sunaudoja ~20–30% daugiau žetonų.

- LLM "mato" tekstą ne kaip žodžius, o kaip **žetonų srautą**
- ~1 žetonas ≈ 0,75 anglų kalbos žodžio / ~0,6 lietuvių kalbos žodžio
- Vienas A4 puslapis ≈ **500–700 žetonų**
- Įrankiai LLM aplinkoje ir jų funkcijos
  - Paieškos variklio įrankis modeliui;
  - Naršymas pagal nuorodą
  - Kodo paleidimo įrankis
  - Išoriniai, modeliui suteikti įrankiai
  - Žiniatinklio paieškos įrankio integravimas ir galimybės
- Atminties įrankiai ir pokalbių išsaugojimas
- **praktinis darbas:** Sąnaudų skaičiavimo pratimai ir modelių palyginimas

### Užduotis - kiek kainuoja naudotis modeliu?

| Modelis      | Įvestis | Išvestis |
| ------------ | ------- | -------- |
| GPT-5        | ~$5.00  | ~$20.00  |
| GPT-4.1      | ~$2.00  | ~$8.00   |
| GPT-4.1 mini | ~$0.40  | ~$1.60   |

**Praktinis skaičiavimas (kartu su grupe):**

> Jūs siunčiate 500 žodžių dokumentą (≈ 650 žetonų) ir gaunate 200 žodžių santrauką (≈ 260 žetonų) naudodami GPT-4.1.

```
KAINA = ((Įvesties žetonai × įvesties kaina) + (Išvesties žetonai × išvesties kaina))/1 000 000
```

```
KAINA =  ((650 x 2$) + (260 x 8$) / 1 000 000) = (1300 + 2080) / 1 000 000 = 3380 / 1 000 000 =  0.00338$
```

# Diena 3: LLM galimybės ir ribotumai

> GPT - Generative Pretrained Transformer

- ChatGPT Code Interpreter įrankiai ir duomenų analizė
- Pagrindinių LLM silpnybių supratimas
  - 1. Klystama įtikinamai (halucinacijos)
       Modelis gali pateikti atsakymą, kuris skamba logiškai, bet yra neteisingas. Tai vadinama **halucinacija** – modelis nesupranta, kad klysta.
  - 2. Žinios gali būti pasenusios
       Jeigu modelis neturi prieigos prie naujausių šaltinių arba jų nepatikrina, jis gali remtis sena informacija. Sprendimas: naudoti žiniatinklio paiešką aktualioms temoms. **Knowledge Cutoff Date**
  - 3. Nėra tikro kalbos supratimo.
       LLM atpažįsta kalbos, duomenų ir konteksto dėsningumus, tačiau neturi tikro sąmoningo supratimo, patirties ar intencijų – tik statistiniai ryšiai tarp žodžių.
  - 4. Ribotas konteksto langas
       Modelis gali apdoroti tik tam tikrą teksto kiekį vienu metu. Labai ilguose dokumentuose jis gali praleisti detales arba pamesti ankstesnį kontekstą. **Context compacting**
  - 5. Rezultatai priklauso nuo užklausos kokybės.
       Neaiškūs, per platūs ar prieštaringi klausimai dažnai duoda prastesnius atsakymus. `Aiškios instrukcijos = Geri rezultatai`. **Prompt Engineering**
  - 6. Ribotas patikimumas skaičiavimuose.
       Modeliai gali suklysti matematikoje, loginiuose žingsniuose ar skaičiuodami be specialių įrankių (Code Interpreter). Svarbius skaičiavimus tikrinkite atskirai.
  - 7. Šališkumas.
       LLM mokosi iš žmonių sukurtų tekstų, todėl gali perimti kultūrinius, socialinius ar politinius šališkumus, net to nepastebėdamas.
  - 8. Sunkumai su nišinėmis temomis
       Jei tema reta, nauja ar blogai dokumentuota, modelis gali spėlioti – ir tai daryti užtikrintai.
  - 9. **Privatumo ir saugumo rizikos.**
       Nereikėtų kelti slaptų duomenų (asmens kodai, slaptažodžiai, komercinės paslaptys), nes priklausomai nuo sistemos nustatymų jie gali būti apdorojami ar saugomi.
  - 10. Negali pakeisti profesionalaus patarimo.
        Teisės, medicinos ir finansų srityse LLM gali padėti pasiruošti klausimus specialistui, bet **negali pakeisti eksperto konsultacijos**.
  - 11. Prastas savęs vertinimas.
        Modelis ne visada tiksliai žino, kada jis nežino. Todėl svarbu prašyti šaltinių ir patikrinimo – ypač svarbiems sprendimams.

- LLM kaip tikimybių mašinos: kaip jos iš tikrųjų veikia
- Halucinacijos: atpažinimas ir mažinimo strategijos
  - Tikrinti šaltinius
  - Paklausti antros nuomonės žmogaus
  - Paklausti antros nuomonės DI
  - Rašyti aiškesnius promptus
  - **Įkelti reikalingą kontekstą spręsti užduočiai.**
- Žinių ribotumas ir mokymo duomenų ribos
- Konteksto dydžio apribojimai ir atminties limitai
- **praktinis darbas**: Halucinacijų atpažinimas ir modelio ribų testavimas
- **praktinis darbas**: Pagalvoti, kaip išprovokuoti kiekvieną iš LLM limitacijų.

---

## **2 savaitė: DI platformų alternatyvos**

### **Diena 1: Gemini, samprotavimo modeliai ir išsamus LLM platformų turas**

- Gemini platformos apžvalga ir galimybės

**Gemini stiprybės:**
| Stiprybė | Kodėl svarbu |
|----------|-------------|
| Integracija su Google | Gmail, Docs, Drive, YouTube tiesiai sąsajoje |
| Ilgas kontekstas | Gemini 2.5 Pro – iki 1 mln. žetonų |
| Multimodalumas | Tekstas, vaizdas, garsas, vaizdo įrašai |
| Realaus laiko paieška | Google paieška integruota pagal nutylėjimą |

- Įvadas į samprotavimo modelius ir jų taikymą
- Gemini funkcijos ir įrankiai
  - Atminties valdymas, pridėti naujų atminties segmentų, trinti senus
  - Asmeninės instrukcijos.
  - Paieškos variklio funkcija
  - Kodo paleidimo funkcija
  - Nuotraukas generuojančio modelio įrankis
  - Leidimas pasiekti YouTube platformos vaizdo įrašus
  - Prieiga prie "Google Workspace"
- Gemini modelių šeima ir jų stiprybės
- Praktinis darbas su Gemini
- **praktinis darbas:** Kurkite ir testuokite prompts su Gemini; Lyginamoji analizė naudojant skirtingas platformas

---

### **Diena 2: Dokumentų analizė su NotebookLM**

- Anthropic ir Claude LLM šeima
- Claude unikalios galimybės ir pokalbio stilius
- Cenzūra ir generatyviojo DI saugikliai
  - Smurtinis turinys;
  - Kenkėjiški instruktavimo žingsniai;
  - Vengia pateikti informaciją apie žmogų dėl BDAR;
  - Karinių/politinių temų vangumas;
- Venice.ai necenzūruotiems modeliams
- X.ai Grok platforma ir realaus laiko galimybės

| Platforma | Saugikliai | Pastaba                               |
| --------- | ---------- | ------------------------------------- |
| ChatGPT   | Vidutiniai | Gerai balansuoja kūrybiškumą ir saugą |
| Claude    | Aukšti     | Labiau atsargus su jautriomis temomis |
| Gemini    | Vidutiniai | Google politika                       |
| Grok      | Žemesni    | Daugiau leidžia "pilkose" zonose      |
| Venice.ai | Minimalūs  | Vartotojo atsakomybė                  |

## NotebookLM

- Importuokite PDF, Google Docs/Slides ir nuorodas kaip šaltinius
- Užduokite į šaltiniais pagrįstus klausimus su įterptomis, patikrinamomis citatomis

> Kuo paprastesnį, minimalesnį darbą gauna DI modelis - tuo jis geriau susidoroja su užduotimi ir pateikia smulkesnį/tikslesnį atsakymą

- Ištraukite lenteles, objektus, laiko juostas ir lyginkite dokumentus greta;
- Automatiškai kurkite santraukas, užrašų korteles ir garso apžvalgas
- Eksportuokite užrašus į Google Docs arba kopijuokite struktūrizuotus rezultatus

- **praktinis darbas:** Įkelkite 3 pavyzdinius dokumentus ir sukurkite mini tyrimų užrašinę: sudarykite palyginamąją lentelę, išvardykite svarbiausias įžvalgas su citatomis ir parenkite vieno pastraipos santrauką

### **Diena 3: Perplexity – greitesniems tyrimams**

- Perplexity AI ir jo Deep Research režimo įvadas
- Užduokite klausimus ir gaukite atsakymus su šaltiniais bei citatomis

| Klausimas                                          | Geriausias įrankis           | Kodėl                              |
| -------------------------------------------------- | ---------------------------- | ---------------------------------- |
| Realaus laiko informacija (kaina, oras, naujienos) | **Perplexity**               | Greičiausiai, visada su šaltiniais |
| Kelių savo dokumentų analizė                       | **NotebookLM**               | Tiksliai iš jūsų šaltinių          |
| Kūrybinis rašymas, formatavimas                    | **ChatGPT / Claude**         | Geriausias generavimui             |
| Greitas fakto patikrinimas                         | **Perplexity**               | Šaltiniai matomi iš karto          |
| Gilios temos studijos                              | **Perplexity Deep Research** | Visapusiška ataskaita              |
| Asmeninių dokumentų klausimai                      | **NotebookLM**               | Tik jūsų šaltiniai                 |

- Kada rinktis greitus atsakymus, o kada Deep Research (3 minučių išsamios ataskaitos)
- Kaip skaityti, tikrinti ir vertinti citatas
- Eksportuokite ir dalinkitės rezultatais (PDF, dokumentai, Perplexity Pages)
- Perplexity, NotebookLM ir ChatGPT palyginimas tyrimams

- **praktinis darbas:** Tą pačią užduotį vykdykite Perplexity, NotebookLM ir ChatGPT; palyginkite rezultatus

---

### LLM parametrai

- **Temperatūra** - LLM parametras atsakingas už modelio tikslumą ir gebėjimą kūrybiškai atsakyti naudotojui;
  - Žema temperatūra modeliui didina tikslumą, patikimumą
  - Aukšta temperatūra modeliui didina kūrybiškumą, modelis drąsiau nagrinėja neišbandytas idėjas
- **Mastymo lygis (thinking level)** - LLM parametras, nustatantis, kiek resursų skirti spręsti konkrečiai užduočiai
  - Jei reikia išsamesnio tyrimo, kūrybiškesnio atsakymo naudoti aukštesnį mastymo lygį;
  - Jei reikia greito paprasto, nesofistikuoto atsakymo naudoti žemesnį mastymo lygį;
- **Saugumo nustatymai (Safety setttings)** - reguliuoja modelio cenzūruotumą
  - Harassment
  - Hate
  - Sexually explicicit
  - Dangerous Content
- **Output length** - Nustato kokio maksimalaus ilgumo (tokenais) atsakymą modelis gali pateikti;
- **Top P (Sekančio žodžio TOP)** - Parametras nusakantis iš top kokio procento žodžių modelis galės rinktis generuodamas sekantį token.

---

## **3 savaitė: Pažangios ChatGPT funkcijos**

### **Diena 1: ChatGPT Canvas dokumentų kūrimui**

- Įvadas į ChatGPT Canvas sąsają
- Bendras dokumentų kūrimas su DI
- Iteratyvus tobulinimas ir versijavimas
- Canvas naudojimas ilgo formato rašymui ir redagavimui
- **praktinis darbas:** Sukurkite verslo _pasiūlymą/komercinį pasiūlymą_ naudodami Canvas

---

### Ollama

- Ollama - įrankis, kuris yra skirtas paleisti AI modelius iš Ollama platformos kompiuteryje, naudojant kompiuterio resursus arba per cloud prieigą
- Modelio parametrų skaičius - rodiklis, nurodantis neuroninių tinklų skaičių modelyje.
- Keliant modelio parametrų skaičių išauga RAM (operatyviosios atm. sunaudojimas), ir GPU (Vaizdo plokštės/procesoriaus) sunaudojimas

- **praktinis darbas:** Įsidiegti ir paleisti savo pasirinktą AI modelį naudojant Ollama programą

---

### **Diena 2: ChatGPT Projects organizavimui**

- ChatGPT Projects funkcijos supratimas
- Pokalbių organizavimas pagal temą ar klientą
- Individualios instrukcijos kiekvienam projektui
- Failų įkėlimas ir konteksto valdymas
  - Įkeliant failus
  - Per pokalbį
- Konteksto inžinerija (Context Engineering)
- Prompt Engineering
  - Tikslas - ką tiksliai turi daryti
  - Konteksto inžinerija;
  - Pavyzdžiai, kaip turėtų būti sprendžiama problema;
  - Formatas (Sąrašas numeruotas/nenumeruotas/ lentelė / failas / WORD dok. / PDF / Excel lentelė / Pastraipa ir t.t.)

## 4 elementai gero prompto

Įsiminti paprastai: **VKFP** — Vaidmuo, Kontekstas, Formatas, Pavyzdys.

| Elementas                   | Klausimas, į kurį atsako       | Pavyzdys                                                    |
| --------------------------- | ------------------------------ | ----------------------------------------------------------- |
| **Vaidmuo / užduotis**      | Ką tiksliai daryti?            | „Parašyk el. laišką" / „Apibendrink" / „Sugalvok 5 idėjas"  |
| **Kontekstas**              | Kam ir kokioje situacijoje?    | „Klientui, kuris vėluoja sumokėti, bet jį norime išlaikyti" |
| **Formatas**                | Kaip turi atrodyti rezultatas? | „3 sakiniai", „sąrašas", „lentelė", „mandagus tonas"        |
| **Pavyzdys** (neprivalomas) | Į ką orientuotis?              | „Panašiai kaip šis ankstesnis laiškas: [...]"               |

**Silpnas promptas:**

> Parašyk laišką klientui.

**Stiprus promptas:**

> Parašyk trumpą (3–4 sakinių) el. laišką klientui, kuris jau dvi savaites vėluoja apmokėti sąskaitą. Tonas mandagus, bet aiškus — norime gauti mokėjimą, bet išlaikyti gerus santykius. Pabaigoje pasiūlyk konkretų terminą.

- **praktinis darbas:** Sukonfigūruokite projektus skirtingiems verslo poreikiams

### **Diena 3: ChatGPT balso režimas, prieinamumas ir paieškos integracija**

- Pažangios balso režimo galimybės
- Sąveika su DI be rankų – produktyvumui.
- Garsas į tekstą darbo srautai.
- Prieinamumo funkcijos įvairiems vartotojams.
- ChatGPT Search galimybių supratimas.
- Informacijos gavimas realiuoju laiku.
- Paieškos rezultatų palyginimas su tradicinėmis paieškos sistemomis
- Geriausios praktikos paiešką naudojantiems prompts
- **praktinis darbas:** Naudokite balso režimą susitikimo pasiruošimui; Atlikite tyrimą naudodami ChatGPT Search

---

## **4 savaitė: Multimodalinis DI**

### **Diena 1: ChatGPT Vision**

- Optical Character Recognition (optinis simbolių atpažinimas). DI naudoja tam kad nuskaitytų tekstą dokumentuose;
- OCR, UI ir diagramų supratimas
- Struktūros išgavimas promptais (sąrašai/JSON)
- Ribos: skaičiavimas, labai smulkus/pasuktas tekstas
- Kainos pagrindai: vaizdai kaip žetonai
- **praktinis darbas:** Išanalizuokite 3 vaizdus ir tobulinkite prompts

---

- GEN AI vs GEN AI Agentas. Kas tai?

### Agento pavyzdys

1. Atėjo laiškas
2. Outlook API -> Serveris
3. Serveris -> gauna laiško turinį, perduoda DI
4. DI Analizuoja ir nusprendžia kokia laiško kategorija
5. Programa duoda nurodymą Outlook API perkelti laišką į tam tikrą dėžutę

- N8N - agentų ir darbo eigų kūrimo platforma

### **Diena 2: Vaizdų generavimas ir redagavimas su ChatGPT ir Qwen**

- gpt-image-2: generavimas, redagavimas, variacijos
- Promptų rašymas: objektas, stilius, neigiami kriterijai
- **praktinis darbas:** Sukurkite/redaguokite 3 rinkodaros išteklius abiem įrankiais

---

- N8N - automatizacijos ir agentų kūrimo platforma
  - N8N viešasis variantas - subscription, mokama už paleidimų kiekį per tam tikrą laikotarpį;
  - N8N privatus variantas - Įdiegta į serverį ar kompiuterį programinė įranga;
- Workflow - Darbo eigos (automatizacijos)

### **Diena 3: ElevenLabs teksto vertimas į kalbą ir Sora 2 vaizdo įrašai**

- TTS, STT, dubliavimas, balso klonavimas
- Modeliai: v3, Flash, Turbo, Multilingual
- Valdikliai: stabilumas, stilius, delsos laikas
- Atsakingas balso technologijų naudojimas ir diegimas
- Promptai: objektas, judesys, kamera
- Funkcijos: nuoseklumas, remiksavimas, automatinis garsas
- Ribos: fizikos realistiškumas, politikos
- Palyginkite su Veo/Kling/Ray
- **praktinis darbas:** Dvikalbė demo garso medžiaga + subtitrai; Sugeneruokite 30 s koncepciją ir iteruokite

---

- Kliento ir serverio architektūra;
- HTTP - HyperText Transfer Protocol, API's;
  - Privatūs API (kai svetainės nesidalina resursais viešai);
  - Vieši API (kai yra galimybė kreiptis iš išorinių svetainių)
- HTTP testavimo įrankiai;
- N8N pavyzdys, kreipiantis į serverį;

---

## **5 savaitė: Generatyvusis DI kaip technologija**

### **Diena 1: Ollama (vietiniai atvirojo kodo modeliai)**

- Įdiekite ir paleiskite (`ollama run modelio_pavadinimas`)
  - Pakurti savo modelį: `ollama create mano-modelis -f modelfile`
  - Paleisti savo modelį: `ollama run mano-modelis`
  - modelfile pavyzdys:

  ```
  FROM gemma4

  SYSTEM """
  Tu esi lietuviškai bendraujantis informacijos surinkimo asistentas.

  Tavo vienintelis tikslas – iš kliento surinkti šią informaciją:

  Vardą ir pavardę
  Elektroninio pašto adresą
  Aiškų sutikimą arba nesutikimą gauti elektroninius laiškus apie mūsų produktų pasiūlymus
  Verslo sritį

  Bendravimo taisyklės:

  Visada bendrauk tik lietuvių kalba.
  Klausk tik vieno klausimo vienu metu.
  Būk trumpas, mandagus ir aiškus.
  Nekalbėk jokiomis kitomis temomis.
  Neatsakinėk į klausimus apie įmonę, produktus, kainas, paslaugas ar kitą informaciją.
  Jei klientas nukrypsta nuo temos, trumpai ir mandagiai grąžink pokalbį prie artimiausios trūkstamos informacijos.
  Jei klientas klausia, kodėl reikia informacijos, atsakyk trumpai: „Ši informacija reikalinga, kad galėtume tinkamai susisiekti ir priskirti jus tinkamai verslo sričiai.“ Tada pakartok einamąjį klausimą.
  Vardas ir pavardė laikomi surinktais tik tada, kai klientas pateikia bent du žodžius, panašius į vardą ir pavardę. Jei pateiktas tik vardas, paprašyk pavardės.
  Elektroninio pašto adresas laikomas surinktu tik tada, kai jis turi įprastą el. pašto struktūrą: tekstas@domenas.galūnė.
  Sutikimas gauti elektroninius laiškus apie produktų pasiūlymus laikomas surinktu tik tada, kai klientas aiškiai atsako „taip“ arba „ne“.
  Jei klientas atsako neaiškiai, pavyzdžiui „gal“, „gerai“, „dar nežinau“, „teigiamai“, „sutinku galbūt“, paprašyk atsakyti tiksliai „taip“ arba „ne“.
  Verslo sritis laikoma surinkta, kai klientas pateikia bet kokią aiškią veiklos sritį, pavyzdžiui: informatika, prekyba, gamyba, statyba, finansai, logistika ar pan.
  Nekurk, nespėliok ir netaisyk kliento pateiktos informacijos.
  Nekartok visos surinktos informacijos klientui.
  Kai visa reikalinga informacija surinkta, pokalbis laikomas baigtu.
  Baigęs pokalbį atsakyk tik tiksliai taip:

  zzz..

  Po atsakymo „zzz..“ į jokias vėlesnes kliento žinutes nebeatsakinėk niekuo kitu, tik:

  zzz..
  """

  PARAMETER temperature 0.2
  PARAMETER num_ctx 2000
  ```

- Lokalus modelis Vs. Cloud modelis

**Pagrindiniai skirtumai:**

|                 | Debesų DI (ChatGPT)            | Vietinis DI (Ollama)                             |
| --------------- | ------------------------------ | ------------------------------------------------ |
| **Privatumas**  | Duomenys siunčiami į serverius | Duomenys lieka jūsų kompiuteryje                 |
| **Kaina**       | Prenumerata ($20+/mėn.)        | Nemokama                                         |
| **Internetas**  | Būtinas                        | Nereikalingas                                    |
| **Kokybė**      | Labai aukšta (GPT-4, Claude)   | Gera, bet silpnesnė nei geriausi debesų modeliai |
| **Greitis**     | Greitas (galingi serveriai)    | Priklauso nuo jūsų kompiuterio                   |
| **Pritaikymas** | Ribotas                        | Visiškas – galite keisti viską                   |

**Rinktis vietinį kai:**

```
✓ Dirbate su konfidencialiais dokumentais (sutartys, medicininiai įrašai, finansai)
✓ Norite nemokamai eksperimentuoti be apribojimų
✓ Dirbate be interneto (kelionės, klientų vietovės)
✓ Norite pilnai pritaikyti DI savo verslo stiliui
✓ Norite integruoti DI į savo sistemas be mėnesinės sąskaitos
✓ Įmonės politika draudžia siųsti duomenis į išorinį debesį
```

- Katalogas: Qwen, Gemma, Llama, DeepSeek
- Modelfile keitimai, HTTP API (Python/JS)

- Privatumo neprisijungus ir našumo patarimai
- **praktinis darbas:** Palyginkite dviejų vietinių modelių našumą per API

### Modelių pasirinkimas

**RAM reikalavimai:**

```
4 GB RAM  → Naudokite 1b–3b modelius: gemma3:1b, llama3.2:1b, qwen3:0.6b
8 GB RAM  → 4b–7b modeliai: gemma3:4b, llama3.2:3b, qwen3:4b
16 GB RAM → 8b–12b modeliai: qwen3:8b, gemma3:12b
32 GB RAM → Didesni modeliai: llama3.2:11b, deepseek-r1:14b
```

---

### **Diena 2: OpenAI, Google AI Studio ir OpenRouter**

- OpenAI Responses API + įrankiai
- Gemini 2.5 lygmenys ir Live API
- Palyginkite kainas/kontekstą/saugą
- Kryžminės platformos (openrouter) darbo srautų raštai
- Vieninga API, maršrutizavimas, atsarginiai keliai, ZDR
  - URL adreso dalis, einanti už domeno PVZ: https://openrouter.ai **_/api/v1/models_** - yra maršrutas
  - **_ZDR_** - Yra Zero Data Retention (Privatumo privilegija). Kai DI tiekiančios įmonės neišsaugo istorijos atsakymų savo DB. O log'ai rodo tik meta-duomenis apie pačią užklausą.
  ***
- Kaip naudoti skirtingus tiekėjus naudojant N8N?
  - API Raktas - Yra identifikacinis tekstas, leidžiantis užklausų metu susieti mūsų paskyros kreditus/naudojimą su realiomis įvykusiomis užklausomis. **_API raktą galima traktuoti kaip slaptažodį_** - svarbu juo nesidalinti su niekuo kitu.
  - AI agent Node - prijungiamas modelis, suteikiamas atminties dydis.
  - AI agent - model subnode - Iš AI agento išplaukiantis sub-node, atsakingas už DI modelio parinkimą ir autentifikavimą
  - AI agent - memory subnode - Iš AI agento išplaukiantis sub-node, atsakingas už DI atmintį, pasirenkama kiek user žinučių modelis atsimena.
- Srautinimas, struktūrizuotos išvestys, talpyklavimas
- Kada naudoti vietoje gimtųjų API
- **praktinis darbas:** Tas pats asistentas abiejose; palyginkite; Palyginkite du modelius vienai užduočiai
