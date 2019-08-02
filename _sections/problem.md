---
title: Problemlösning
icon: fa-lightbulb
order: 7
---

I denna sektion så hittar du övningsuppgifter utan några lösningsförslag. Tanken med dessa uppgifter är att du ska kombinera de koncept som har behandlats i tidigare sektioner för att lösa problem på egen hand. Om du kör fast så kan du i första hand återgå till relevanta tidigare sektioner, se över kursmaterialet eller Googla efter tillvägagångssätt på egen hand.

## Uppgiftsförteckning ##

Uppgift 1 | Summering och sammanslagning av arrayer
----------|-------------------------------
Beskrivning | Skriv en metod, <code>SumArrays</code>, som tar emot två arrayer av heltal som argument (<code>arrayA och arrayB</code>) och returnerar en array - <code>arrayC</code> - som innehåller summan av talen på resp. position. Dvs. att om värdet på position 0 i <code>arrayA</code> är 5 och värdet på position 0 i <code>arrayB</code> är 13 så ska position 0 i <code>arrayC</code> innehålla värdet 18 osv.<br><br> **OBS!** Om den ena arrayen är längre än den andra så ska värdet från den längre arrayen placeras i <code>arrayC</code>.

---

Uppgift 2 | Prisberäkning för inträde
----------|----------
Beskrivning | Skriv en metod, <code>AdmissionPrice</code>, som beräknar priset för inträde till ett nöjesfält baserat på gästernas ålder. Antalet gäster som tillhör gruppen bestäms utav användaren som skriver in <code>N</code> efter att samtliga gäster och deras resp. ålder har angivits. <br><br> Pristabellen som gäller är:<br><br> - Barn (3-12): 50 kr. <br> - Pensionär (65+): 75 kr. <br> Samtliga resterande åldersgrupper betalar alltid 110 kr. <br><br> Om gruppen består utav fler än 4 gäster så ges en rabatt på 20% på totalpriset. Metoden ska efter beräkning skriva ut antalet gäster i gruppen och den totala summan.

---

Uppgift 3 | Palindrom
----------|----------
Beskrivning | Skriv en metod, <code>IsPalindrome</code>, som avgör om en sträng är ett palindrom eller ej. Ett palindrom är ett ord eller en mening som är exakt likadan skrivet baklänges, t.ex. "Sirap i paris". Metoden __ska__ ta mellanslag, specialtecken och versaler/gemener i beaktelse när den avgör om strängen är ett palindrom eller ej.

---

Uppgift 4 | Decimal to binary
----------|----------
Beskrivning | Skriv en metod, <code>DecToBin</code>, som översätter ett heltal enligt det decimala talsystemet till det binära talsystemet. Det decimala talsystemet är det som vi nyttjar till vardags med basen 10 (0-9). Det binära talsystemet nyttjar istället basen 2 där något antingen är av eller på (0 eller 1). Således får vi exempelvis <code>1010</code> om vi översätter <code>10</code>, <code>1100100</code> om vi översätter <code>100</code> osv. ***NOTERA*** att ju längre något är till vänster i ett binärt tal, desto större är det. I <code>1010</code> så har vi 8, 4, 2, 1 där 1:orna indikerar de värden som ska tillgodoräknas (i detta fall 8:an och 2:an för 10).<br><br> Om du vill läsa mer om hur man konverterar från det decimala talsystemet till det binära så kan du nyttja följande länk: [Dec to binary](https://www.wikihow.com/Convert-from-Decimal-to-Binary). Om du vill nyttja en redan existerande konverterare så kan du kika på följande länk: [Dec/Bin Converter](https://www.rapidtables.com/convert/number/decimal-to-binary.html).<br><br> **TIPS!** Nyttja iteration och modulus. Uppgiften __skall__ lösas utan den inbyggda metoden <code>Convert.ToString</code>.

---

Uppgift 5 | Beräkning av heltal
----------|----------
Beskrivning | Skriv en metod som läser in ett godtyckligt antal positiva eller negativa tal från användaren. Metoden ska sedan räkna ut antalet positiva resp. negativa tal. För att avsluta inmatningen så ska användaren ange "e". Metoden ska då avslutningsvis skriva ut antalet positiva och negativa tal. Exempel på interaktion med metoden:<br><br><code>1</code><br><code>-4</code><br><code>-1</code><br><code>0</code><br><code>6</code><br><code>12</code><br><code>e</code><br><code>Antal positiva tal: 3</code><br><code>Antal negativa tal: -2</code><br><br>***NOTERA*** att "0" inte ska tillgodoräknas som ett positivt eller negativt tal. **TIPS!** Nyttja en while-loop för att läsa in heltal från användaren.

---

Uppgift 6 | Tidsberäkning av tågresor
----------|----------
Beskrivning | Ett persontågsföretag vill ha ett program (en metod i detta fall) för att underlätta tidsberäkningen av tågresor med syftet att upprätta en tidtabell. Metoden ska läsa in avgångsort, avstånd mellan avgångsorten och destinationen samt datum och klockslag för avgång. Därefter ska metoden räkna ut vilket datum och vilken tid tåget kommer till destinationen. Tågets genomsnittliga hastighet är 130 km/h. <br><br>***TIPS!*** Nyttja SVT-triangeln för att beräkna tiden (givet hastigheten och avståndet). Datatypen <code>DateTime</code> kan nyttjas för att enklare behandla datum och klockslag, men det krävs då att man utforskar lite vad datatypen har att erbjuda på egen hand. Det är dock fullt möjligt att nyttja strängar istället. Följande länk kan nyttjas för att få en inblick i <code>DateTime</code>: [DateTime](https://www.dotnetperls.com/datetime)

---

Uppgift 7 | Hotellbokning
----------|----------
Beskrivning | Inom en hotellverksamhet önskar man få överblick över vilka rum som är bokade samt vilka som är lediga. Skriv först ett program (eller en metod) som läser in "bokat" kontra "ledigt" i en array som består utav 15 platser. Varje plats i arrayen motsvarar ett rum på hotellet.<br><br>b. Utöka sedan programmet genom att lägga till möjligheten att genomföra bokningar. Vid en bokning så ska det första lediga rummet i rumslistan (arrayen) identifieras och sedan ändra värde till "bokat".<br><br>c. Utöka sedan programmet ytterligare genom att låta användaren ange om ett rum önskas bokas eller avbokas. Om rummet ska bokas kan implementationen i b) nyttjas,  om en avbokning ska ske så behöver vi dock kunna hantera detta. Vid en avbokning så ska rumsnummer anges och efter avbokning så ska värdet i arrayen ändras till "ledigt".

---

Uppgift 8 | Textmarkering
----------|----------
Beskrivning | Skriv ett program som läser in en sträng med valfri text. Programmet ska därefter markera alla förekomster av tecknet "å" genom att skriva ut texten igen och på raden under skriva ett <code>*</code> för varje förekomst av tecknet ("å"). Exempelvis kan interaktion med programmet se ut enligt följande:<br><br>$$\begin{document} \fbox{ \parbox{ \textwidth}{Svenska äpplen och fem året runt-äpplen\\ \vspace*{6mm}* }} \end{document}$$<br><br>Utöka programmet så att det även markerar "ä". Skriv även här ut tecknet <code>*</code>.<br><br>c. Utöka programmet ytterligare så att det istället för att skriva <code>*</code> för "å" och "ä" skriver tecknet <code>*</code> för "å" och tecknet <code>%</code> för "ä". 

---

Uppgift 9 | BMI kalkylator
----------|----------
Beskrivning | Skriv en metod som beräknar BMI (body mass index) värdet för en person. Metoden ska läsa in personens längd och vikt och därefter nyttja en utav två formler för att utföra beräkningen. Vilken formel som ska nyttjas beror på om längd och vikt anges enligt metriska eller imperiska mått (dvs. exempelvis cm gentemot feet + inches). Den metriska formeln är:<br><br>$$\begin{equation}BMI = \frac{weight}{height \times height} \times 703 \end{equation}$$<br><br>och den imperiska formeln är: <br><br>$$\begin{equation}BMI = \frac{weight}{height \times height} \end{equation}$$

---

Uppgift 10 | Summera individuella siffror i ett heltal
----------|----------
Beskrivning | Skriv en metod som summerar samtliga siffror i ett heltal och returnerar summan. Om metoden exempelvis tar emot heltalet <code>1234</code> så ska <code>10</code> returneras. Uppgiften ska lösas __utan__ att konvertera heltalet till en sträng. <br><br>***TIPS!*** Nyttja division och det decimala talsystemet för att "hoppa" en decimal i taget och summera dessa allt eftersom. Dvs. att vi från <code>1234</code> först plockar ut 4:an vilket lämnar oss med <code>123</code>, därefter plockar vi ut 3:an osv.

---

Uppgift 11 | Beräkning av SGD
----------|----------
Beskrivning | Den största gemensamma delaren (SGD) för ett antal heltal är det största heltalet som talen kan delas med utan att ge någon rest. Exempelvis är <code>SGD(6, 9) = 3</code> då 3 är det största talet som är delbart med både 6 och 9. Skriv en metod som beräknar och returnerar den största gemensamma delaren för två heltal. <br><br>För att läsa mer om SGD och se mer utförliga exempel på hur processen går till så kan följande länk nyttjas: [SGD med Euklides algoritm](http://www.matteguiden.se/matte-diskret/de-hela-talen/storsta-gemensamma-delare/). ***TIPS!*** Nyttja modulus för att avgöra huruvida divisionen resulterar i rest kombinerat med iteration för att identifiera SGD.

---

Uppgift 12 | Hitta medianen
----------|----------
Beskrivning | Medianen är det tal som representerar mitten i en talföljd. Om vi exempelvis har heltalen 10, 63 och 15 så agerar 15 medianvärdet. Om vi istället har heltalen 10, 63, 15 och 25 så blir medianen istället 20 (15 + 20 / 2). Skriv en metod som tar emot en array av heltal som en parameter och returnerar medianen. <br><br>***TIPS!*** Tänk på att arrayen först och främst __bör__ sorteras i storleksordning. Uppgift 23 under sektionen "Iteration/arrayer" kan nyttjas för detta syfte. Efter detta så kan vi antingen enkelt plocka ut värdet i mitten (om arrayen består utav ett udda antal element) eller så behöver vi identifiera de två mittenvärden som finns i arrayen och utföra beräkningen enligt ovan exempel.

---

Uppgift 13 | IsInteger
----------|----------
Beskrivning | Skriv en metod, <code>IsInteger</code> som tar emot en sträng och avgör om strängen representerar ett riktigt heltal. Metoden ska ignorera mellanslag men behöver kunna hantera <code>+</code>-tecken och <code>-</code>-tecken. <br><br>***TIPS!*** Metoden <code>char.IsDigit</code> kan nyttjas för att avgöra om ett tecken representerar en siffra eller ej.

---

Uppgift 14 | StringFormat
----------|----------
Beskrivning | Skriv en metod, <code>StringFormat</code> som tar emot en array av strängar och skriver ut samtliga strängar i arrayen enligt nedan format: <br><br>Om arrayen innehåller <code>[apples, oranges]</code> så får vi: <code>apples and oranges</code><br> Om arrayen istället innehåller flera strängar t.ex. <code>[apples, oranges, bananas]</code> så får vi istället: <code>apples, oranges and bananas</code><br><br>***TIPS!*** Nyttja metoden <code>string.Split</code>.

---

Uppgift 15 | Teckenbyte
----------|----------
Beskrivning | Skriv en metod som kan läsa in flera textrader från användaren och byta ut varje förekomst av tecknet "O" till tecknet "Ö" resp. "o" till "ö". Metoden ska läsa in en rad i taget varvid metoden sedan ska presentera raden med de teckenbyten som har skett för att sedan läsa in nästa rad. Denna process ska upprepas tills dess att användaren anger "EXIT". Exempel på interaktion med metoden kan tänkas se ut enligt följande:<br><br>Input: 	Mors lilla Olle i skogen gick.<br>Output: 	Mörs lilla Ölle i skögen gick.<br>Input: 	Om vädret är fint så kommer Ofelia på festen.<br>Output:   Öm vädret är fint så kömmer Öfelia på festen.<br>Input: EXIT

---

Uppgift 16 | Begynnelsebokstäver
----------|----------
Beskrivning | Skriv en metod som skriver ut alla begynnelsebokstäver i en mening. Med begynnelsebokstäver så avses det första bokstaven i resp. ord i en mening. Exempel på interaktion med metoden kan tänkas se ut enligt följande:<br><br>Datorerna Synes Vänliga och Programmen Slutar Vårdslöst.<br>Output: D S V o P S V

---

<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/latest.js?config=TeX-MML-AM_CHTML">
</script>

<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
