# Revizuire comercială — 23 octombrie 2026

## Modificări implementate

- Texturi raster pixel-art memorate pentru gresie, rafturi, valize, zona WC și mobilier; detalii și culori distincte Bosch, Makita, DeWALT și Festool. Coliziunile mobilierului sunt păstrate.
- Sprite-uri mai vizibile, accesorii distincte, umbre, neon radial, scule pulsante și lacăt roșu/verde la ieșire.
- Patru ecrane de intro fullscreen; transformare declanșată o singură dată în centrul showroom-ului, cu logo la opacitate 80%. Efectele respectă preferința de mișcare redusă.
- Oferte Vlad/Andrei de 25%, produs în coș, Game Over imediat la buget zero și factură obligatorie pentru victorie.
- Deblocare AudioContext din gestul de start. Muzica se oprește inclusiv în conversațiile clienților; SFX rămân independente.
- Grila de navigație este reutilizată și invalidată la schimbarea obstacolelor; coada de căutare folosește tablouri reutilizabile. Randarea ecranelor inactive este limitată, iar fila ascunsă nu continuă desenarea.

## Verificare

Au trecut 27 grupe de teste locale (`node qa/game.test.cjs`): poveste, evenimente, proiecte, audio, coliziuni, acces la obiective, cameră touch, oferte, retur, bonusuri, Game Over, checkout, obstacole, DASH, manager, clienți, protecția între interacțiuni și transformarea centrală.

Testele simulează DOM, Canvas și Audio. Nu demonstrează 60 FPS, calitatea sunetului auzit sau compatibilitatea cu toate dispozitivele. Fișierul include aproximativ 3,8 MB de cod și ilustrații.

## Acceptare pe dispozitive reale

- Testați un iPhone și un Android, portret și landscape: lizibilitate, touch simultan, sunet după primul tap și revenire din fundal.
- Verificați 3–5 partide cu jucători noi pentru dificultate și înțelegerea facturii.
- Confirmați destinațiile CTA ale proiectelor și afirmațiile comerciale înainte de promovarea plătită.
- Verificați timpul primei încărcări pe internet mobil. Nu există o măsurătoare certificată de FPS sau timp de încărcare.

Referință audio: [MDN — Web Audio best practices](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API/Best_practices).
