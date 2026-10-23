# AtelierulRău.ro — Halloween Edition

Joc Canvas 2D în română, într-un singur `index.html`, cu CSS, JavaScript, imagini și sunete încorporate. Fără build sau biblioteci externe.

[JOC PUBLIC](https://neapetrica.github.io/atelierulrau-halloween/)

- Desktop: WASD / săgeți, Space DASH, P / Escape pauză.
- Mobil: D-pad, tap pe culoar, DASH și Hartă / Aproape.
- Patru ecrane de poveste fullscreen, cinci evenimente de brand și trei proiecte.
- Colectează trei scule, obține factura Elenei și ieși cu buget pozitiv.
- Vlad și Andrei: 25% buget și un produs nedorit per ofertă, maximum patru oferte fiecare. Patru pierderi fără recuperări epuizează bugetul.
- Interacțiunile nu se suprapun; după discuții ai două secunde de protecție. DASH durează 1,5 secunde și se reîncarcă în cinci secunde.
- Doi clienți patrulează și te țin de vorbă; al treilea întârzie factura cu șase secunde, o singură dată.
- Muzica rulează numai în jocul activ, în afara conversațiilor. Sunetele sunt deblocate prin butonul de start.
- Texturi pixel-art, mobilier 2.5D, reflexii de neon, personaje animate și transformare în zona centrală.

Pentru GitHub Pages este suficient `index.html` în rădăcină. Nu publica directorul `.review/`, care conține copii de lucru.

Verificare locală: 27 grupe de teste ale logicii în `qa/game.test.cjs`. Aceste teste folosesc DOM/Canvas/Audio simulate; nu certifică performanța sau compatibilitatea pe dispozitive reale. Detalii în `AUDIT-LANSARE.md`.

Joc pamflet de Halloween 2026. Evenimentele, bugetul și reducerile sunt virtuale; nu oferă premii sau vouchere reale.
