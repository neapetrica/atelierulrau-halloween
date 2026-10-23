# AtelierulRău.ro — Halloween Edition

Joc Canvas 2D în limba română. Deschide `index.html` în browser. Același fișier conține CSS, JavaScript, ilustrațiile și sunetele sintetizate; nu necesită build sau instalare.

- Desktop: WASD / săgeți, Space pentru DASH, P / Escape pentru pauză.
- Mobil: D-pad, tap pe culoar, DASH și butonul Hartă / Aproape.
- Scop: colectează trei scule, obține factura Elenei și ieși cu buget pozitiv.
- Dificultate moderată: ofertele Vlad / Andrei costă 15%, maximum patru per personaj. Eugen oferă un pachet la a treia întâlnire, fără eliminare instantanee. Pierzi doar la buget zero.
- După dialog ai 2 secunde de protecție. DASH se reîncarcă în 5 secunde.
- Evenimentul și proiectul se aleg pe o singură pagină. Doar transformarea de Halloween ocupă tot ecranul; jocul începe automat după circa 3 secunde.

Pentru GitHub Pages, fișierul de intrare este `index.html`, în rădăcină. Nu încărca fotografiile și copiile de lucru din `.review/` (sunt excluse prin `.gitignore`). Nu există servicii backend, tracking sau formulare de înscriere.

Verificare logică: `node qa/game.test.cjs`.

Versiune publică pentru testare: https://neapetrica.github.io/atelierulrau-halloween/

Joc pamflet de Halloween 2026, exclusiv pentru divertisment. Evenimentele, bugetul și reducerile sunt virtuale; jocul nu oferă premii sau vouchere reale.

Cele 24 grupe de verificări automate acoperă logica jocului. Randarea și performanța trebuie verificate pe dispozitive reale. Pentru raportarea unei probleme, deschide un Issue și precizează dispozitivul, browserul și pașii de reproducere.

Clienții fictivi: doi te rețin până la 5 secunde, timp în care angajații se apropie; poți încheia discuția după 2 secunde. Un al treilea client întârzie factura Elenei cu 6 secunde, o singură dată pe meci. Poți să te deplasezi cât aștepți. Dialogurile angajaților pun în continuare jocul pe pauză.

Săgețile de pe podea au opacitate 15%. Cei doi clienți fără factură patrulează culoarele. Interacțiunile nu se suprapun; după fiecare discuție există un răgaz global de 2 secunde.
