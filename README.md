# AtelierulTău — O zi în echipă

Simulator arcade al firmei, cu showroom și depozit după schița extinsă. Jocul anterior AtelierulRău Halloween rămâne disponibil ca bonus „Client”, inclus în același `index.html`.

[JOC PUBLIC](https://neapetrica.github.io/atelierulrau-halloween/)

## Jocul principal

- Opt colegi jucabili: Cristi, George, Vlad, Andrei, Mihai, Eugen, Sebi și Elena. Rolurile sunt atribuite aleatoriu, fără repetare până la epuizarea grupului în sesiunea curentă.
- O zi are 40 de sosiri programate și durează cel mult 8 minute active. Colegii automatizați procesează o parte dintre cereri; jucătorul primește solicitări pe rol.
- Rezolvă personal minimum trei misiuni, păstrează ratingul de minimum 4,3 din 5 stele și fonduri suficiente pentru costurile zilei.
- Rating mediu calculat din recenzii. Sub 4,3★: alertă comună și 55 secunde pentru recuperare. Recenziile sunt solicitate doar după rezolvări bune, fără recompense.
- Depozit: recepție, numărare, diferențe cu Elena, stocare, căutare cu Mihai, coletare și predare.
- Vânzări: showroom, telefon, WhatsApp, înregistrarea și transmiterea obligatorie a comenzii.
- Support: retururi, tichete, găsirea produselor și escaladări. Termenele de 30 de zile sunt comprimate explicit în timpul jocului.
- Eugen: oferte mari, verificări și sprijin pentru vânzări. Mihai și Eugen au scenete fictive de deghizare, cu risc de pierdere a încrederii.
- Sebi: furnizori, costuri, prețuri, stoc, avertizări și suspendări temporare care reduc capacitatea echipei.
- Elena: facturi și diferențe de recepție.

## Controale

WASD/săgeți, Shift pentru mers rapid, E pentru acțiune, P/Escape pentru pauză. Pe mobil: D-pad, tap pe culoar, mers rapid și butoane mari. „Mergi la destinație” găsește un traseu; decizia se ia la punctul de lucru. Butonul Hartă schimbă între ansamblu și urmărirea jucătorului pe mobil.

## Distribuire și validare

Tot jocul, inclusiv bonusul, este în `index.html`; fără build, backend sau biblioteci externe. Copiile și sursele intermediare din `.review/` nu se publică.

Teste locale: `node qa/simulator.test.cjs` și `node qa/game.test.cjs`. 21 grupe pentru simulator și 27 pentru bonus. Testele nu certifică FPS sau compatibilitatea pe toate telefoanele.

Simulare fictivă pentru divertisment. Nu reprezintă termene legale, politici comerciale, evaluări reale ale angajaților sau promisiuni de preț. Nu oferă premii/vouchere, nu contactează clienți și nu colectează date personale.


## Claritate și tutorial — 29 octombrie 2026

Prima misiune se învață fără cronometru sau sosiri de clienți. Obiectivul principal indică acțiunea și locul, iar următorul pas apare imediat după alegere. Recepția include numărarea cutiilor; verificările de comandă folosesc liste bifabile. Coletele transportate, livrările și răbdarea clienților sunt vizibile pe hartă. Solicitările apar progresiv, iar feedbackul explică modificarea ratingului.


## Comenzi, personalități și recuperare

Clienții grăbiți, nehotărâți și profesioniști au indicatoare distincte, cerințe explicite și răbdare diferită. Numărul și culoarea comenzii o urmăresc la punctul de lucru; comenzile colegilor trec vizual prin înregistrare, colectare, ambalare și facturare. O comandă incompletă eligibilă deschide o singură misiune de recuperare de 40 de secunde: completare cu Mihai, apoi predare clientului. Expirarea sau renunțarea închid cazul fără bucle.
