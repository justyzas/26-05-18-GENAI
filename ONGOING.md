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


| Klausimas | Geriausias įrankis | Kodėl |
|-----------|-------------------|-------|
| Realaus laiko informacija (kaina, oras, naujienos) | **Perplexity** | Greičiausiai, visada su šaltiniais |
| Kelių savo dokumentų analizė | **NotebookLM** | Tiksliai iš jūsų šaltinių |
| Kūrybinis rašymas, formatavimas | **ChatGPT / Claude** | Geriausias generavimui |
| Greitas fakto patikrinimas | **Perplexity** | Šaltiniai matomi iš karto |
| Gilios temos studijos | **Perplexity Deep Research** | Visapusiška ataskaita |
| Asmeninių dokumentų klausimai | **NotebookLM** | Tik jūsų šaltiniai |


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
- **Mastymo lygis (thinking level)** -  LLM parametras, nustatantis, kiek resursų skirti spręsti konkrečiai užduočiai
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
- **praktinis darbas:** Sukurkite verslo *pasiūlymą/komercinį pasiūlymą* naudodami Canvas 
--- 
### Ollama


- Ollama - įrankis, kuris yra skirtas paleisti AI modelius iš Ollama platformos kompiuteryje, naudojant kompiuterio resursus arba per cloud prieigą
- Modelio parametrų skaičius - rodiklis, nurodantis neuroninių tinklų skaičių modelyje.
- Keliant modelio parametrų skaičių išauga RAM (operatyviosios atm. sunaudojimas), ir GPU (Vaizdo plokštės/procesoriaus) sunaudojimas


- **praktinis darbas:** Įsidiegti ir paleisti savo pasirinktą AI modelį naudojant Ollama programą

---

<!-- ### **Diena 2: ChatGPT Projects organizavimui**

- ChatGPT Projects funkcijos supratimas
- Pokalbių organizavimas pagal temą ar klientą
- Individualios instrukcijos kiekvienam projektui
- Failų įkėlimas ir konteksto valdymas
- **praktinis darbas:** Sukonfigūruokite projektus skirtingiems verslo poreikiams -->