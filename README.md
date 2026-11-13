# AtelierulRău.ro — Halloween Edition

Un singur joc: ești CLIENTUL, alegi un eveniment și un proiect, explorezi showroomul și depozitul, colectezi trei scule și obții factura de la Elena înainte de ieșire. Pierzi dacă bugetul ajunge la zero. Nu există roluri de angajat, rating de firmă sau cronometru de trei minute. Timpul afișat este durata partidei.

Depozitul se află deasupra showroomului, cu trecere în dreapta-sus, rafturi, ambalare și biroul lui Sebi. Două scule ale proiectului sunt în depozit, una în showroom. WC-ul și separeul închis rămân mobilier inaccesibil conform schiței.

## Pornire și controale
Deschide `index.html` local sau pe GitHub Pages. WASD/săgeți ori D-pad pentru mers; tap/click pe culoare pentru traseu; Space/DASH pentru sprint. Butonul Hartă comută între camera apropiată și planul complet. Dialogurile, coșul și pauza păstrează mecanicile originalului.

## Surse și verificare
Sursa activă: `src/client-game.html`. Build: `python tools/build-game.py`. Teste: `node qa/game.test.cjs` (31 grupuri, inclusiv accesul în depozit, camere, coliziuni, retur, checkout și Game Over). Testele nu înlocuiesc verificarea pe telefoane reale.

Fișierele simulatorului și campaniilor anterioare sunt păstrate ca istoric, dar nu sunt incluse în jocul public. `game-sources.zip` conține numai sursa și testele jocului client.
