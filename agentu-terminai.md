# AI agentų terminai

## 1. Modelių ansamblis

Modelių ansamblis reiškia, kad naudojami keli AI modeliai vietoje vieno.

Paprasta analogija: ne vienas žmogus sprendžia problemą, o maža komisija.

Pvz.:

```
Klausimas → Modelis A
          → Modelis B
          → Modelis C
          → Galutinis atsakymas
```

Tada sistema gali:

- paimti daugumos atsakymą;
- palyginti, kuris modelis atsakė geriau;
- vieną modelį naudoti tikrinimui;
- vieną modelį naudoti kūrybai, kitą logikai, trečią saugumui.

**Pavyzdys:**

Vartotojas klausia: *"Ar šis laiškas skamba profesionaliai?"*

- Modelis A: pataiso gramatiką.
- Modelis B: įvertina toną.
- Modelis C: sutrumpina.
- Galutinė sistema sujungia geriausią variantą.

Tai ir yra ansamblis.

## 2. Modelių „choras“

Choras dažniausiai yra metafora. Reiškia, kad keli modeliai „dainuoja kartu“, t. y. generuoja, vertina arba balsuoja dėl atsakymo.

Skirtumas nuo paprasto ansamblio nėra labai griežtas. Dažnai „choras“ reiškia labiau tokį principą:

1. Tas pats klausimas duodamas keliems modeliams.
2. Visi pateikia savo atsakymus.
3. Sistema išrenka arba sujungia geriausią.

**Pvz.:**

- Modelis 1: siūlo techninį sprendimą.
- Modelis 2: sako, kad sprendime yra saugumo rizika.
- Modelis 3: pasiūlo paprastesnę alternatyvą.
- Finalinis atsakymas: paima geriausias dalis iš visų.

Tai tarsi AI „choras“, nes vienas atsakymas gimsta iš kelių balsų.

## 3. Voting / balsavimas

Tai paprasta ansamblio forma.

Pvz. trys modeliai atsako į klausimą:

- Modelis A: Taip
- Modelis B: Taip
- Modelis C: Ne

Sistema pasirenka „Taip“, nes 2 iš 3 taip atsakė.

Tai ypač naudinga, kai atsakymas yra klasifikacija:

- Ar laiške yra asmens duomenų?
- Ar klientas piktas?
- Ar užklausa skubi?
- Ar promptas saugus?

## 4. Judge modelis

Judge modelis yra modelis-teisėjas.

Jis pats nebūtinai sprendžia pagrindinę užduotį, bet vertina kitų modelių atsakymus.

**Pvz.:**

- Modelis A parašo atsakymą.
- Modelis B parašo kitą atsakymą.
- Judge modelis įvertina, kuris geresnis.

**Arba:**

- Pagrindinis modelis atsako klientui.
- Judge modelis patikrina:
  - ar atsakyta lietuviškai;
  - ar nėra išgalvotų faktų;
  - ar tonas mandagus;
  - ar surinkta visa reikalinga informacija.

Tavo n8n workflow atveju tai būtų labai naudinga.

**Pvz.:**

- AI agentas surenka kliento informaciją.
- Judge modelis patikrina, ar yra:
  - vardas;
  - el. paštas;
  - sritis;
  - sutikimas dėl marketingo.
- Jeigu kažko trūksta, grąžina pokalbį atgal.

## 5. Routeris

Routeris nusprendžia, kuriam modeliui arba agentui perduoti užklausą.

Paprasta analogija: registratūra.

**Pvz.:**

- Klientas rašo: *"Noriu pagalbos su sąskaitomis"* → Routeris siunčia buhalterijos agentui.
- Klientas rašo: *"Noriu pasikalbėti dėl svetainės"* → Routeris siunčia web projektų agentui.
- Klientas rašo: *"Noriu darbo pasiūlymo"* → Routeris siunčia HR agentui.

Routeris gali būti:

- paprastas if;
- AI modelis;
- embeddings paieška;
- taisyklių sistema;
- hibridas.

## 6. Mixture of Experts

Mixture of Experts, arba MoE, reiškia „ekspertų mišinį“.

Čia idėja tokia: vietoje vieno didelio modelio yra daug mažesnių specializuotų dalių — ekspertų. Užduoties metu aktyvuojami tik keli reikalingi ekspertai.

**Pvz.:**

- Klausimas apie kodą → aktyvuojamas programavimo ekspertas.
- Klausimas apie matematiką → aktyvuojamas matematikos ekspertas.
- Klausimas apie kalbą → aktyvuojamas kalbos ekspertas.

Svarbu: MoE dažnai vyksta modelio viduje, o ansamblis dažniau reiškia kelis atskirus modelius iš išorės.

Labai supaprastintai:

- **Ansamblis** = keli atskiri modeliai dirba kartu.
- **MoE** = vieno modelio viduje yra daug ekspertų dalių.

## 7. Agentai

Agentas yra AI modelis su konkrečia role, instrukcijomis ir galbūt įrankiais.

**Pvz.:**

- Klientų aptarnavimo agentas
- Buhalterijos agentas
- Techninis agentas
- Kokybės tikrinimo agentas
- El. laiškų rašymo agentas

Agentas nėra tik modelis. Agentas paprastai turi:

```
Modelis + instrukcijos + atmintis + įrankiai + tikslas
```

**Pvz. n8n sistemoje:**

- AI modelis: GPT / Gemini / Claude / Ollama
- Instrukcija: rink kliento informaciją lietuviškai
- Įrankiai: siųsti el. laišką, skaityti darbo laiką, tikrinti specialistus
- Rezultatas: struktūruotas JSON

Tai jau agentas.

## 8. Multi-agent sistema

Tai sistema, kurioje keli agentai dirba kartu.

**Pvz.:**

1. Intake agentas surenka informaciją iš kliento.
2. Router agentas nusprendžia, kuriam specialistui siųsti.
3. Calendar agentas patikrina darbo laiką.
4. Email agentas paruošia laišką.
5. Judge agentas patikrina, ar viskas gerai.

Čia jau būtų multi-agent workflow.

## 9. Chain / grandinė

Chain reiškia, kad AI veiksmai vyksta vienas po kito.

**Pvz.:**

1. Ištraukti informaciją iš kliento žinutės.
2. Patikrinti, ko trūksta.
3. Sugeneruoti papildomą klausimą.
4. Kai viskas surinkta, grąžinti JSON.

Tai yra grandinė.

n8n labai natūraliai tam tinka, nes visas workflow ir yra grandinė iš node'ų.

## 10. RAG

RAG reiškia, kad modelis atsakymui naudoja išorinę informaciją.

Pvz. turi dokumentą su specialistų darbo laikais:

- Jonas dirba I–III 08:00–16:00
- Aistė dirba IV–V 10:00–18:00
- Marius dirba tik su verslo klientais

Kai klientas parašo užklausą, sistema pirma susiranda aktualią informaciją, tada modelis atsako.

```
Kliento užklausa → paieška dokumentuose/DB → modelis → atsakymas
```

Svarbu: RAG nėra tas pats, kas „memory". RAG dažniausiai ieško informacijos dokumentuose, duomenų bazėje ar vektorinėje saugykloje.

## 11. Memory

Memory reiškia, kad sistema prisimena ankstesnį kontekstą.

**Pvz.:**

- Klientas jau pasakė vardą.
- Sistema neturi klausti vardo dar kartą.

**Trumpalaikė memory:**

Šio pokalbio istorija.

**Ilgalaikė memory:**

Duomenų bazėje išsaugota informacija apie klientą.

n8n atveju ilgalaikė memory gali būti:

- PostgreSQL
- Redis
- SQLite
- Google Sheets
- Airtable
- Supabase
- Qdrant / Pinecone / Chroma

## 12. Structured output

Tai kai modelis turi atsakyti ne laisvu tekstu, o konkrečiu formatu.

**Pvz.:**

```json
{
  "vardas": "Jonas Jonaitis",
  "email": "jonas@example.com",
  "sutinka_gauti_pasiulymus": true,
  "verslo_sritis": "Statyba"
}
```

Tai labai svarbu automatizacijose, nes n8n gali lengvai naudoti JSON laukus kituose node'uose.

## 13. Guardrails

Guardrails yra apsauginės taisyklės.

**Pvz.:**

- Neleisti modeliui atsakyti ne lietuviškai.
- Neleisti generuoti atsakymo, jei trūksta el. pašto.
- Neleisti siųsti laiško, kol Judge modelis nepatvirtino.
- Neleisti priimti neteisingo el. pašto formato.

Tai kaip apsauginiai borteliai keliuose.

## 14. Prompt filter

Tai modelis arba taisyklė, kuri prieš perduodant užklausą pagrindiniam modeliui patikrina, ar viskas tvarkoje.

**Pvz.:**

- Ar žinutėje yra slaptažodis?
- Ar yra asmens kodas?
- Ar klientas prašo kažko neleistino?
- Ar užklausa tinkama šiam agentui?

Tavo anksčiau minėtam „prompt filter" variantui galima daryti taip:

```
User input → Filter modelis → Pagrindinis modelis
```

Jeigu filtras randa problemą:

Sustabdyti / anonimizuoti / paprašyti patikslinti.

## 15. Orkestravimas

Orkestravimas reiškia visų šitų dalių sujungimą į vieną veikiančią sistemą.

Pvz. n8n yra orkestravimo įrankis.

Jis nusprendžia:

- Kada kviesti AI modelį.
- Kada kviesti Gmail.
- Kada tikrinti darbo laiką.
- Kada rašyti į duomenų bazę.
- Kada siųsti laišką.
- Kada stabdyti procesą.

## Trumpas palyginimas

| Terminas | Reikšmė |
|---|---|
| Ansamblis | Keli modeliai dirba kartu |
| Choras | Keli modeliai pateikia „balsus", kurie sujungiami |
| Voting | Balsavimas tarp kelių atsakymų |
| Judge | Modelis, kuris vertina kitų atsakymus |
| Routeris | Nusprendžia, kur siųsti užklausą |
| MoE | Ekspertų sistema modelio viduje |
| Agentas | Modelis su role, instrukcijomis ir įrankiais |
| Multi-agent | Keli agentai vienoje sistemoje |
| Chain | Veiksmų grandinė |
| RAG | Atsakymai pagal išorinius dokumentus/duomenis |
| Memory | Ankstesnės informacijos prisiminimas |
| Structured output | Atsakymas JSON ar kitu griežtu formatu |
| Guardrails | Apsauginės taisyklės |
| Prompt filter | Užklausos patikrinimas prieš pagrindinį modelį |
| Orkestravimas | Visų dalių sujungimas į workflow |
