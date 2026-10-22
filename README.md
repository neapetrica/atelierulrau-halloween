# AtelierulRău.ro — Halloween Edition

Joc Canvas 2D în limba română. Deschide `index.html` în browser. Același fișier conține CSS, JavaScript, ilustrațiile și sunetele sintetizate; nu necesită build sau instalare.

- Desktop: WASD / săgeți, Space pentru DASH, P / Escape pentru pauză.
- Mobil: D-pad, tap pe culoar, DASH și butonul Hartă / Aproape.
- Scop: colectează trei scule, obține factura Elenei și ieși cu buget pozitiv.
- Patru oferte cumulate de la Vlad / Andrei sau trei întâlniri cu Eugen încheie jocul. Retururile nu resetează acest contor.

Pentru GitHub Pages, fișierul de intrare este `index.html`, în rădăcină. Nu încărca fotografiile și copiile de lucru din `.review/` (sunt excluse prin `.gitignore`). Nu există servicii backend, tracking sau formulare de înscriere.

Verificare logică: `node qa/game.test.cjs`.

Versiune publică pentru testare: https://neapetrica.github.io/atelierulrau-halloween/

Joc pamflet de Halloween 2026, exclusiv pentru divertisment. Evenimentele, bugetul și reducerile sunt virtuale; jocul nu oferă premii sau vouchere reale.

Cele 17 grupe de verificări automate acoperă logica jocului. Randarea și performanța trebuie verificate pe dispozitive reale. Pentru raportarea unei probleme, deschide un Issue și precizează dispozitivul, browserul și pașii de reproducere.
