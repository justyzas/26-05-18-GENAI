# Generatyvaus DI žodynėlis

Terminai abėcėlės tvarka pagal kategorijas. Kiekvienam – paprastas paaiškinimas be techninių žargonų.

---

## 1. Pagrindinės DI sąvokos

**Dirbtinis intelektas (DI)** *(Artificial Intelligence, AI)*
Kompiuterių sistemų gebėjimas atlikti užduotis, kurios paprastai reikalauja žmogaus intelekto – suprasti kalbą, atpažinti vaizdus, priimti sprendimus.

**Generatyvusis DI** *(Generative AI)*
DI rūšis, kuri kuria naują turinį – tekstą, vaizdus, garsą, vaizdo įrašus, kodą. Skirtingai nuo seno DI, kuris tik klasifikuodavo ar prognozuodavo, generatyvusis DI gamina originalų išvestį.

**LLM – Didysis kalbinis modelis** *(Large Language Model)*
Dirbtinio intelekto modelis, išmokytas iš didžiulių tekstų kiekių. Gebėjimas suprasti ir generuoti natūralią kalbą. Pavyzdžiai: GPT-5, Gemini, Claude, Llama.

**Prompts / Promptai** *(Prompt)*
Tekstinė instrukcija arba klausimas, kurį siunčiate DI modeliui. Tai, ką įrašote į ChatGPT langą. Prompto kokybė tiesiogiai lemia atsakymo kokybę.

**Promptų inžinerija** *(Prompt Engineering)*
Menas ir mokslas rašyti efektyvias instrukcijas DI modeliams. Apima struktūrą (vaidmuo + kontekstas + užduotis + formatas), iteraciją ir testavimą.

**Žetonai / Tokenai** *(Tokens)*
Mažiausi teksto vienetai, kuriuos modelis „mato". Apytikriai 1 žetonas ≈ 0,75 žodžio anglų kalba (lietuvių – šiek tiek daugiau). Kainos skaičiuojamos pagal žetonų skaičių.

**Kontekstas / Konteksto langas** *(Context / Context Window)*
Visa informacija, kurią modelis „mato" vieno pokalbio metu – jūsų klausimai, jo atsakymai, įkelti dokumentai. Kiekvienas modelis turi maksimalų ribą (pvz., 128 000 žetonų).

**Halucinacija** *(Hallucination)*
Kai DI modelis pateikia faktiškai neteisingą informaciją užtikrintai – sugalvoja faktus, citatas, datas, žmonių vardus. Tai struktūrinis LLM bruožas, ne klaida. Todėl visada reikia tikrinti.

**Mokymo duomenų riba** *(Training Cutoff)*
Data, po kurios modelis nebeturi informacijos. Pvz., modelis išmokytas iki 2024 m. nieko nežino apie 2025 m. įvykius, nebent naudoja interneto paiešką.

**Multimodalus DI** *(Multimodal AI)*
DI, galintis dirbti su keliais formatais vienu metu – tekstas, vaizdai, garsas, vaizdo įrašai. ChatGPT Vision yra multimodalus, nes supranta ir tekstą, ir paveikslėlius.

**Samprotavimo modeliai** *(Reasoning Models)*
Pažangūs LLM, galintys spręsti sudėtingesnes logines ir matematines problemas žingsnis po žingsnio. Pavyzdžiai: OpenAI o3, Gemini 2.5 Pro.

---

## 2. Platformos ir įrankiai

**ChatGPT**
Populiariausia vartotojams skirta DI pokalbių platforma, sukurta OpenAI. Naudoja GPT modelių šeimą.

**GPT-5 / GPT-4.1 / GPT-5-mini**
OpenAI modelių variantai. GPT-5 – galingiausias ir brangiausias; GPT-5-mini – greitesnis ir pigesnis paprastoms užduotims.

**Claude** *(Anthropic)*
Anthropic sukurtas LLM, žinomas dėl ilgo konteksto lango, atsargaus tono ir stipraus teksto analizės. Alternatyva ChatGPT.

**Gemini** *(Google)*
Google sukurtas LLM. Integruotas su Google ekosistema (Docs, Gmail, Search). Gemini 2.5 Pro – vienas galingiausių šiuo metu.

**Grok** *(X.ai)*
Elon Musk X (Twitter) platformos LLM. Pasižymi realaus laiko interneto duomenimis ir mažiau ribojančiu stiliumi.

**NotebookLM** *(Google)*
Google įrankis dokumentų analizei. Leidžia įkelti PDF, straipsnius, nuorodas ir užduoti klausimus – atsakymai pateikiami su tiksliais šaltinių citatų nuorodomis.

**Perplexity**
DI paieškos variklis su šaltinių citavimu. Deep Research režimas per ~3 minutes sukuria išsamias ataskaitas su nuorodomis. Puikus tyrimams.

**ElevenLabs**
Garso DI platforma. Paverčia tekstą į kalbą (TTS), klonuoja balsus, dubliuoja vaizdo įrašus į kitas kalbas.

**Sora** *(OpenAI)*
OpenAI vaizdo įrašų generavimo modelis. Kuria vaizdo įrašus pagal teksto aprašymą.

**Ollama**
Programa, leidžianti paleisti atviro kodo LLM modelius vietiniame kompiuteryje be interneto. Visiškai privatu – duomenys niekur nesiunčiami.

**Lovable.dev**
No-code svetainių kūrimo įrankis su DI pagalba. Aprašote norimą svetainę tekstu – sistema ją sukuria.

**OpenRouter**
Tarpinė platforma, suteikianti prieigą prie daugelio LLM per vieną API. Leidžia lengvai perjungti ir lyginti modelius.

**GitHub Copilot**
DI kodo asistentas, integruotas į programavimo aplinkas (VS Code ir kt.). Siūlo kodo užbaigimus, rašo funkcijas pagal aprašymą.

**OpenAI Codex Cloud**
OpenAI platforma, leidžianti deleguoti kodavimo užduotis DI agentui, kuris dirba debesyje ir pateikia rezultatus kaip GitHub PR.

**n8n**
Atviro kodo no-code automatizavimo platforma. Leidžia kurti darbo srautus, jungiant įvairias programas ir DI modelius be programavimo.

**Make.com**
Komercinė no-code automatizavimo platforma. Populiari alternatyva n8n. Intuityvesnė pradedantiesiems, bet ribota nemokamame plane.

---

## 3. Techniniai terminai

**API** *(Application Programming Interface)*
„Jungtis" tarp programų. Leidžia jūsų programai kalbėti su kita programa (pvz., siųsti klausimą ChatGPT iš savo sistemos ir gauti atsakymą).

**OCR** *(Optical Character Recognition – optinis simbolių atpažinimas)*
Technologija, paverčianti vaizdus ar skenuotus dokumentus į mašininio skaitomo tekstą. ChatGPT Vision naudoja OCR analizuojant nuotraukas su tekstu.

**TTS** *(Text-to-Speech – tekstas į kalbą)*
Technologija, paverčianti rašytinį tekstą į garsą. ElevenLabs yra TTS platforma.

**STT** *(Speech-to-Text – kalba į tekstą)*
Technologija, paverčianti garso įrašus į rašytinį tekstą. ChatGPT balso funkcija naudoja STT.

**Code Interpreter**
ChatGPT funkcija, leidžianti modeliui rašyti ir vykdyti Python kodą – atlikti skaičiavimus, analizuoti duomenis, kurti grafikus.

**Canvas** *(ChatGPT)*
ChatGPT funkcija ilgų dokumentų kūrimui ir redagavimui. Atidaro atskirą langą, kuriame galima iteratyviai tobulinti tekstą kartu su DI.

**Projects** *(ChatGPT)*
ChatGPT funkcija, leidžianti grupuoti pokalbius pagal temą ar klientą su atskiromis instrukcijomis ir failais kiekvienam projektui.

**Vision** *(ChatGPT)*
ChatGPT gebėjimas analizuoti ir aprašyti paveikslėlius, ekrano nuotraukas, diagramas, dokumentų nuotraukas.

**MCP** *(Model Context Protocol)*
Standartas, leidžiantis DI modeliams prisijungti prie išorinių įrankių ir duomenų šaltinių (failų sistemos, duomenų bazių, API).

**ZDR** *(Zero Data Retention)*
Nuostata, kuri neleidžia API tiekėjui saugoti jūsų duomenų savo serveriuose. Svarbu dirbant su konfidencialia informacija.

**Vibe coding**
Neformalus terminas kodavimui su DI pagalba, kai „jaučiate" kryptį ir DI realizuoja – minimaliai rašant kodą rankiniu būdu.

---

## 4. Automatizavimas ir agentai

**No-code automatizavimas**
Darbo srautų kūrimas be programavimo – vizualiais įrankiais jungiant programas ir automatizuojant pasikartojančias užduotis.

**Darbo srautas / Workflow**
Automatizuotų veiksmų seka. Pvz.: gaunu el. laišką → DI jį susumuoja → atsakymas išsiunčiamas automatiškai.

**Mazgas / Node**
Vienas veiksmas darbo sraute (pvz., „išsiųsk el. laišką", „gauk duomenis iš svetainės", „klausk DI").

**Trigeris / Trigger**
Įvykis, paleidžiantis automatizuotą darbo srautą. Pvz.: naujas el. laiškas, naujas kalendoriaus įrašas, nauja eilutė skaičiuoklėje.

**DI agentas** *(AI Agent)*
DI sistema, galinti savarankiškai planuoti ir atlikti kelių žingsnių užduotis naudodama įrankius (paieška, el. paštas, kalendorius). Skirtingai nuo paprasto LLM, agentas veikia autonomiškai.

**Human-in-the-loop (HITL)**
Automatizacijos modelis, kai svarbiausiuose žingsniuose sistema sustoja ir laukia žmogaus patvirtinimo prieš tęsdama.

**RAG** *(Retrieval-Augmented Generation – išgavimas prie generavimo)*
Technika, kai DI prieš atsakydamas ieško relevantinės informacijos jūsų dokumentų bazėje ir grindžia atsakymą ja. Rezultatas: tikslūs atsakymai su citatomis iš jūsų failų.

**Įterpiniai / Embeddings**
Matematinė teksto reprezentacija kaip skaičių vektorius. Leidžia DI rasti panašius tekstus pagal prasmę, o ne tik pagal žodžius.

**Vektorių saugykla** *(Vector Store)*
Specializuota duomenų bazė, sauganti įterpinius ir leidžianti greitai rasti semantiškai panašią informaciją. RAG pagrindas.

**Fragmentai / Chunks**
Didelių dokumentų dalys, į kurias jie suskaidomi prieš įrašant į vektorių saugyklą. Dydis lemia paieškos tikslumą.

**Fine-tuning / Pritaikymas**
LLM papildomas mokymas su specifiniais duomenimis, kad modelis specializuotųsi tam tikroje srityje. Brangiau ir sudėtingiau nei RAG.

---

## 5. Rodikliai ir vertinimas

**MMLU** *(Massive Multitask Language Understanding)*
Testas, matuojantis LLM žinias 57 srityse – nuo matematikos iki teisės. Standartinis akademinis modelių palyginimo rodiklis.

**MT-Bench**
Testas, matuojantis modelio gebėjimą vykdyti daugiažingsnes nurodymo užduotis ir pokalbio kokybę.

**Arena Elo**
Reitingas, pagrįstas žmonių vertinimais – vartotojai palygina dviejų modelių atsakymus ir balsuoja. Laikomas realistiškiausiu rodikliu.

---

## 6. Greitoji nuoroda

| Santrumpa | Pilnas pavadinimas | Lietuviškai |
|-----------|-------------------|-------------|
| DI | Dirbtinis intelektas | — |
| LLM | Large Language Model | Didysis kalbinis modelis |
| API | Application Programming Interface | Programų sąsaja |
| RAG | Retrieval-Augmented Generation | Išgavimas prie generavimo |
| TTS | Text-to-Speech | Tekstas į kalbą |
| STT | Speech-to-Text | Kalba į tekstą |
| OCR | Optical Character Recognition | Optinis simbolių atpažinimas |
| HITL | Human-in-the-loop | Žmogus grandinėje |
| MCP | Model Context Protocol | Modelio konteksto protokolas |
| ZDR | Zero Data Retention | Duomenų nesaugojimas |
| Q&A | Question & Answer | Klausimų–atsakymų |
| PR | Pull Request | Kodo pakeitimų užklausa |
