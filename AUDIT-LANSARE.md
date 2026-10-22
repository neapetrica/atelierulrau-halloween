# AtelierulRău.ro — audit înainte de publicare

Data: 22 octombrie 2026. Verdict: **candidat de lansare**, nu validare completă pe dispozitive reale.

## Ce este rezolvat

- Jocul rămâne într-un singur `index.html`, fără biblioteci, fonturi sau imagini încărcate de pe servere externe. Ilustrația nouă este încorporată ca data URI. Fișierul are aproximativ 3,84 MB.
- Pauza manuală afișează trei scene inspirate din fotografiile din Word: intrarea, culoarul Bosch și consultanța la birou. Săgețile permit navigarea. Revenirea este imediată; nu există pauze publicitare obligatorii.
- Muzica, mișcarea și timpul se opresc în pauză/coș/dialog și la final. Muzica revine numai în gameplay.
- Urmăritorii consumă corect distanța pe mai multe puncte ale traseului în același cadru. Înainte, se opreau câte un cadru la fiecare segment de 6 pixeli și viteza reală era mai mică decât cea declarată.
- Vlad și Andrei au aceeași rază de atingere. Contorul vizibil `OFERTE 0/4` explică apropierea de pierdere; la 3/4 apare avertizarea.
- Pierderea afișată la ultima atingere reflectă suma reală. De exemplu, regula atingerii a patra poate consuma mai mult de 25% dacă anterior au existat retururi. Regula este explicată în intro.
- Numărul de produse din final nu mai include produsele returnate.
- Focalizarea tastaturii revine la Canvas după start/dialog. Space nu mai blochează activarea normală a butoanelor și a coșului.
- Coșul nu poate fi deschis în fundalul altor ecrane. P/Escape din coș deschide pauza, fără blocaj de stare.
- Conversia touch recalculează camera după redimensionare. Totalurile de buget nu mai dispar în orientarea landscape.
- Copiile fotografiilor originale și fișierele de lucru sunt în `.review/`, exclus din Git. Nu sunt necesare pentru joc.

## Verificări automate efectuate

Comandă: `node qa/game.test.cjs` (Node.js, fără instalarea de pachete).

Au trecut 17 grupuri de verificări: cele cinci evenimente și trei proiecte; ciclul audio; pauza și galeria; coșul; accesul la scule/Elena/ieșire; camera touch; cele patru lovituri cumulate; retur unic, expirare și cooldown; bonusurile Mada; Eugen; Game Over; factură obligatorie; obstacole temporare; stamina; slidewall; viteza de urmărire; resetarea meciului.

Testele folosesc DOM, Canvas și Audio simulate. **Nu confirmă aspectul CSS, sunetul auzit efectiv, rata de cadre, compatibilitatea Safari sau dificultatea pentru un jucător uman.**

## Ce trebuie verificat înainte de lansarea publică

| Prioritate | Verificare | Criteriu de acceptare |
|---|---|---|
| Necesară | Un Android și un iPhone, portret și landscape | Bugetul, harta, D-pad, DASH și butonul de revenire rămân accesibile; fără scroll orizontal al paginii sau elemente care acoperă comenzile. |
| Necesară | 3–5 partide cu oameni care nu cunosc jocul | Înțeleg obiectivul și factura; pot finaliza o partidă după ce învață traseul. Viteza urmăritorilor a fost corectată, deci poate necesita reglaj după această probă. |
| Necesară | CTA pentru fiecare proiect | Căutarea `advanced_search_result.php?keywords=...` deschide rezultate relevante. Operatorul `or` și rezultatele nu au fost confirmate în magazin; dacă nu funcționează, înlocuiți cu pagini de categorii verificate. |
| Necesară | Repository și Pages | Proiectul local nu are remote GitHub configurat. Nu s-a făcut push sau publicare. După alegerea repository-ului, testați URL-ul HTTPS final, nu doar fișierul local. |
| Recomandată | Încărcare pe conexiune mobilă | Ilustrația inclusă mărește fișierul la circa 3,84 MB. Verificați încărcarea la prima vizită; imaginile nu trebuie să împiedice începerea jocului. |
| Recomandată | Verificare comercială de către echipă | Confirmați textele „16 Ani”, „Consultanță Gratuită”, „Livrare Rapidă” și separarea evenimentului real de experiența fictivă. Jocul nu înscrie utilizatorul la evenimente și nu oferă vouchere reale. |

Accesul automat la pagina locală `file://` a fost blocat de politica browserului disponibil. Nu s-a încercat ocolirea acestei restricții. Din acest motiv, auditul vizual final pe dispozitive reale rămâne deschis.

## Scenariu scurt pentru acceptare

1. Alege un cort, un proiect și parcurge transformarea. Verifică textul și dezactivarea muzicii în slide-uri.
2. Mergi cu D-pad, apoi cu tap și DASH; schimbă orientarea în timpul jocului. Verifică „Hartă / Aproape”.
3. Acceptă o ofertă: observă procentajul, suma pierdută și produsul. Deschide coșul și verifică oprirea timpului.
4. Mergi la Mihai în 30s: produs returnat și buget recuperat. Încearcă o a doua returnare imediată.
5. Deschide pauza: treci prin cele trei imagini și revino. Sunetul muzical trebuie să fie oprit în pauză.
6. Verifică pierderea prin a patra ofertă sau a treia întâlnire cu Eugen. Repornește fără să reîncarci pagina.
7. Colectează 3/3, încearcă ieșirea înainte de Elena, obține factura și ieși. Testează CTA-ul proiectului.

## Recomandare de produs

Mecanica este deja suficient de bogată: evenimente, proiecte, coș, retur, bonus, dash, cafea, obstacole, urmăritori și checkout. Nu recomand adăugarea altor reguli înainte de lansare. Prioritatea este verificarea clarității și a șanselor reale de câștig. Galeria în pauză adaugă identitate vizuală fără să prelungească fiecare dialog.

## Ilustrații — proveniență și prompt

Instrument: `image_gen` integrat, skill `imagegen`. Referințe: imaginile 3, 6 și 9 extrase din `joc_AtelierulRau.docx`. Rezultatul este salvat în joc, în `pauseImage.src`; copia originală de lucru este `.review/pause-scenes.png`.

Promptul final folosit:

> Create a single horizontal 3-panel sprite sheet for the pause gallery of the Romanian retro game AtelierulRau.ro. Three equal rectangular panels side by side, no borders or gaps, total aspect ratio 3:1. Each panel a carefully authored classic 16-bit Sega adventure background, visible pixel clusters, limited rich palette, dithering, crisp stepped contours, no smooth photographic textures. Left panel inspired by reference 1: actual low gray tool showroom exterior with staircase and railings to central glass doors, red AtelierulTau sign, twilight sky, subtle orange pumpkin near stairs. Middle panel inspired by reference 2: deep perspective long Bosch blue accessory shelves on left and workshop saws on stands, warm fluorescent lights with subtle violet Halloween accents. Right panel inspired by reference 3: friendly gray-haired adviser in black shirt talking to blue-shirt customer across wooden desk with laptop, wall of power tools behind, no identifiable photographic faces necessary, pixel illustration. Preserve key architecture and arrangement from each respective photograph. Welcoming customer service, mild playful Halloween, no gore, no horror faces. No UI, no captions, no watermarks. Tiny brand signage can be rendered as simple red/blue pixel wordmarks, avoid other prose. Each panel must be readable as a standalone landscape game background.


## Personaje: Bogdan și Sebi

Bogdan preia vechiul boss: apariție aleatorie, povestea celor 16 ani, dialog de minimum 3 secunde și pierdere de bază 15% (cu multiplicatorul evenimentului). Sebi este șeful de magazin: traversează în aproximativ 5 secunde active între ușa din dreapta-sus și intrare, alternând sensul. Cât este prezent, angajații urmăresc clientul. Vlad/Andrei și Eugen își păstrează regulile; Mada, Mihai și Elena oferă temporar vânzări de bază 5%, cu excepția facturării Elenei. Dialogurile suspendă traversarea. Apoi angajații revin la posturi. Au fost adăugate teste pentru moștenirea puterilor, traversare, revenire, vânzări și reset.
