ŽMOGUS: 

```
<question>
    Nuo kelių metų galima laikyti A kategoriją?
</question>
<system-prompt>
    Tu esi apie vairavimą Lietuvoje nusimanantis ekspertas....
    Tu gali kreiptis į šiuos dokumentus, naudojant RAG:
    1. Saugaus elgesio Keliais Lietuvoje įstatymas
    2. KET kelių ženklai
    3. KET tvarka gyvenvietėse
    ..
    98. Teisę vairuoti įgijimo tvarka Lietuvoje.
    ...
    104. KET tvarka gyvenamosiose zonose
</system-prompt>
<system-question>
    Ar sugebėsi į klausimą atsakyti be papildomo konteksto? Atsakyk tokiu formatu:
    {
        ableToAnswer: true/false,
        document: null/"document-name"
    }
</system-question>
```

ASSISTANT (vidinis):
```
    {
        ableToAnswer: false,
        document: "98. Teisę vairuoti įgijimo tvarka Lietuvoje."
    }
```

ŽMOGUS (vidinis):
```
    <document>
        Teorija – lengvoji dalis

        A kategorijos vairavimo egzaminas, kaip ir visi kiti, sudarytas iš dvejų dalių – teorijos ir praktikos. Tiesa, teorijos egzaminas daliai jaunuolių neatrodo toks baisus, jei jie jau turi teisę vairuoti kitokios kategorijos transporto priemones. Skirtingų kategorijų teoriniai egzaminai gana panašūs.
        30 iš 35 klausimų būna susiję su bendrais vairavimo principais ir tik likę skiriasi priklausomai nuo laikomos kategorijos.

        Sunkesni iššūkiai būsimųjų motociklininkų laukia aikštelėje ir mieste, čia tenka vairuoti motociklą savarankiškai. Visi AB “Regitra” egzaminavimo centrai turi motociklų egzaminams, tačiau galingesnių transporto priemonių, skirtų norintiems iš karto įgyti A kategorijos vairuotojo pažymėjimą be apribojimų yra tik Vilniuje ir Kaune. Kituose miestuose egzaminuojamiesiems patiems reikia pasirūpinti motociklais – patogiausia motociklą išsinuomoti iš vairavimo mokyklos. Tai galioja ir vyresniems nei 21 metų asmenims – jei jie nori pasinaudoti galimybe gauti vairuotojo pažymėjimą be apribojimų, turi laikyti egzaminą galingesniu motociklu.
        Neturint jokios kitos kategorijos naujai iškepti A kat. vairuotojai, nepaisant amžiaus, gauna dviem metams apribotą vairuotojo pažymėjimą.

        Klumpa ties aštuonetu

        Užduotys aikštelėje būsimiesiems motociklininkams skiriamos vienodos, nepriklausomai nuo motociklo galios. Aikštelėje reikia sugebėti valdyti motociklą išjungtu varikliu, stumti atbulomis, lėtai važiuoti siaura juosta, apsukti aštuoniukę, gyvatėle apvažiuoti kliūtį, pasukti mažo spindulio posūkyje į kairę, greitai įsibėgėti iki 50km/h ir sustoti tiksliai nurodytoje vietoje. Sunkiausia užduotis egzaminuojamiesiems yra aštuoniukė, o dažniausiai prie šios užduoties suklumpa merginos, kurioms pasirodo per sudėtinga valdyti daug sveriančią transporto priemonę.

        Mokosi ne dėl reikalo

        Praktinius pratimus verta gerai išmokti, nes jie reikalingi ne tik egzaminui išlaikyti, bet ir pritaikomi vairuojant tikrame eismo sraute. Aštuoniukė yra puikus pratimas išmokti laikyti pusiausvyrą, kad mokinys įgustų skirstyti savo kūno svorį sukdamas iš vieno posūkio į kitą. Važiavimas siaura juosta skirtas išmokti jausti motociklo plotį, nes gyvenime ne kartą susidarys situacija, kai teks pravažiuoti pro siaurą tarpą.

        Mokiniams sunkiausia yra aštuoniukės užduotis, dauguma vis taikosi pasiremti koja, ko daryti negalima. Išvažiavus į gatves jiems sudėtingiausia persirikiuoti, laiku parodyti posūkių signalus ir pakankamai žvalgytis aplinkui.

        Vis tik, A kategorijos egzaminus iš pirmo karto išlaikančiųjų gerokai daugiau, nei iš karto gaunančių B kategorijos teises. Teorijos egzaminą iš pirmo karto išlaiko 74 proc. būsimųjų motociklininkų ir 64 proc. automobilių vairuotojų, o praktikos egzaminų rezultatai dar labiau skiriasi – 75 proc. prieš 39 proc. B kategorijos nenaudai. Toks skirtumas yra dėl to, kad lengvuosius automobilius vairuoti pageidaujančių yra gerokai daugiau ir ne visi jie laiko egzaminus dėl to, kad iš tikrųjų trokštų vairuoti. Motociklininkų motyvacija visai kitokia. Motociklas nėra tikroji transporto priemonė, laikančiųjų amžiaus vidurkis gerokai didesnis. Norintiems vairuoti motociklą išlaidos tenka ne tik egzaminui, bet ir motociklą išlaikyti reikia, o įsigyti jį taip pat nepigus malonumas. Todėl neįsitikinę, kad iš tikrųjų nori vairuoti plieninį žirgą nešvaisto laiko. Tuo tarpu B kategorijos vairuotojo pažymėjimą nesunku panaudoti ir neturint automobilio – galbūt jo prireiks darbe arba pavyks automobilį retkarčiais pasiskolinti iš tėvų ar draugų.

        Nieko nevairavę

        Didelė dalis būsimųjų motociklininkų patys įdeda labai daug pastangų. Jie vairavimo teoriją išmoksta patys iš KET knygelių bei internetinėse vairavimo teorijos mokymo puslapiuose, o į mokyklą atvyksta tik mokytis vairavimo. Tačiau tik mitas, kad A kategorijos vairuotojo pažymėjimo dažniausiai užsigeidžia jau turintys teisę vairuoti automobilį. Apie 80 proc. mokinių, atėjusių į vairavimo mokyklą, nemoka vairuoti jokios transporto priemonės, o kai kurie nėra važiavę net dviračiu.

        Bet net ir mokantiems vairuoti automobilį pamokos motociklu yra nemenkas iššūkis. Motociklo vairavimas nuo automobilio labiausiai skiriasi tuo, kad reikia balansuoti ant dviejų ratų, o kūno nesaugo joks kėbulas. Todėl visiems mokiniams patariama važiuojant įsivaizduoti, kad jų niekas nemato, nes motociklininkų kiti vairuotojai iš tiesų dažnai nepastebi ir patikimiausia saugotis pačiam.
    </document>
    <question>
            Nuo kelių metų galima laikyti A kategoriją?
    </question>
```

ASSISTANT:

```
Pilną A kategoriją galima įgyti:

Nuo 20 metų, jeigu turi bent 2 metų A2 kategorijos vairavimo stažą.
Nuo 24 metų – galima laikyti iš karto, neturint A2 stažo.

Papildomai: A2 galima laikyti nuo 18 metų, o A1 – nuo 16 metų.
```