# Audit — simulatorul echipei, 28 octombrie 2026

Versiune jucabilă inițială a simulatorului, cu bonusul Halloween păstrat integral în același fișier. Echilibrarea pentru jucători noi rămâne de validat prin partide reale.

## Implementat

Hartă extinsă showroom + depozit, coliziuni și trasee către toate stațiile, opt personaje, roluri aleatorii fără repetare în grup, 40 de clienți programați pe zi, sarcini cu pași și termene, consecințe asupra recenziilor și economiei, alertă comună sub 4,3★, recuperare, costuri zilnice și raport final. Colegii necontrolați sunt simulați automat; nu este multiplayer.

Fluxurile de depozit, vânzări, support, oferte, achiziții și facturare includ decizii bune și greșeli remediabile. Jucătorul trebuie să finalizeze minimum trei misiuni; activitatea automată nu este suficientă pentru victorie. Sunetul este opțional și se oprește în pauză/dialoguri. Trecerea în fundal pune jocul pe pauză.

## Verificări automate

21 grupe simulator: acoperirea rolurilor, toate fluxurile, pașii omişi în vânzări, traseele depozitului, media recenziilor, alertă/recuperare/eșec, limite de răspuns, vestiar/deghizare, aprovizionare/preț/fonduri, întârzieri, feedback, zi completă cu 40 de clienți, conectivitatea tuturor destinațiilor și integrarea bonusului.

27 de grupe existente trec pentru bonusul Halloween. Replica despre Alin Petrea este acum pozitivă: clientul caută oferta personalizată; numele NPC este „Client cu ofertă”.

## Limite și probe recomandate

- Modelul economic folosește unități de stoc agregate și cost mediu simplificat, nu gestiune contabilă reală.
- Termenul de 30 de zile, deghizările și suspendările sunt mecanici fictive, nu recomandări profesionale sau juridice.
- Cele 40 de sosiri au loc dacă ziua continuă; o pierdere anticipată încheie ziua înainte de toate sosirile.
- Nu există salvare între sesiuni, conturi online sau multiplayer.
- Testați câte o zi în fiecare rol și reglajul termenelor cu oameni care nu cunosc traseul.
- Testați pe iPhone/Android: gesturi simultane, redimensionare, sunet, revenire din fundal și revenire din bonus.
- Nu se garantează 60 FPS pe orice dispozitiv. Fișierul este de aproximativ 3,9 MB, în mare parte ilustrația inclusă în bonus.


## Claritate și tutorial — 29 octombrie 2026

Prima misiune se învață fără cronometru sau sosiri de clienți. Obiectivul principal indică acțiunea și locul, iar următorul pas apare imediat după alegere. Recepția include numărarea cutiilor; verificările de comandă folosesc liste bifabile. Coletele transportate, livrările și răbdarea clienților sunt vizibile pe hartă. Solicitările apar progresiv, iar feedbackul explică modificarea ratingului.


## Comenzi, personalități și recuperare

Clienții grăbiți, nehotărâți și profesioniști au indicatoare distincte, cerințe explicite și răbdare diferită. Numărul și culoarea comenzii o urmăresc la punctul de lucru; comenzile colegilor trec vizual prin înregistrare, colectare, ambalare și facturare. O comandă incompletă eligibilă deschide o singură misiune de recuperare de 40 de secunde: completare cu Mihai, apoi predare clientului. Expirarea sau renunțarea închid cazul fără bucle.


## Partidă cu zar — 29 octombrie 2026

Interfața pornește 8 ture × 90 secunde active, 5 clienți/tură, cu rating și fonduri păstrate. Tutorialul inițial și dialogurile se adaugă duratei. Zarul alege prima variantă cu probabilitatea 4/6, iar celelalte două fețe aleg uniform dintre alternative. Rezultatul este confirmat explicit; remedierea rămâne manuală. 12% dintre clienți au așteptări foarte ridicate și cel mult 3,8 stele pentru rezolvare, fapt explicat în dialog. Validare: 24 grupe simulator și 27 bonus.
