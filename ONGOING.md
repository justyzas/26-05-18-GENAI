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
- Konteksto langas
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
