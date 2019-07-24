---
title: Iteration/Arrayer
icon: fa-th
order: 5
---

# <a name="iteration"></a>Iteration och arrayer #
Datatypen array är oftast något svår att förstå sig på inledningsvis. Exempelvis så kan man inte manipulera storleken (t.ex. lägga till en plats eller ta bort en plats i listan) på en array då dessa är statiska. Vi måste dessutom alltid ha i åtanke att, åtminstone för C#, indexpositionerna i en array alltid startar från position 0. Dvs. att när vi då exempelvis itererar över en array så måste man <br>1) börja på 0 (om vi inte vill hoppa över det första elementet) och <br>2) vara försiktig så att vi inte pekar på en indexposition som inte finns. <br>Se nedan exempel:
```cs
int[] arr = new int[] { 2, 4, 6, 8, 10, 12, 14, 16, 18, 20 };

int x = arr[0]; // x = 2;
x = arr[9]; // x = 20;
x = arr[10]; // IndexOutOfRangeException då vi pekar på en position som inte existerar.
```

Iteration är ett koncept som tillåter oss att återupprepa ett stycke kod tills dess att vi når ett angivet resultat. En vanlig tillämpning av detta är nyttjandet av loopar såsom <code>for-loopar</code>, <code>while-loopar</code> och <code>foreach-loopar</code>. Föreställ dig exempelvis att vi vill söka efter ett angivet heltal i en array av heltal. Utan iteration så skulle vi behöva manuellt gå igenom varje element i arrayen och kontrollera dess värde mha. <code>if-satser</code>. Genom att istället tillämpa iteration så kan vi säga åt vårt program att gå igenom hela arrayen åt oss och vi behöver bara skriva en <code>if-sats</code> istället för 10 (om arrayen från föregående kodexempel skulle nyttjas). Dvs. i stil med:
```cs
int search = 12; // Elementet vi letar efter i arrayen.
int[] arr = new int[] { 2, 4, 6, 8, 10, 12, 14, 16, 18, 20 };

for(int i = 0; i < arr.Length; i++){
  if(arr[i] == search){
    Console.WriteLine("Elementet hittades på plats:" + i);
  }
}
```
**OBS!** I ovan kodexempel så är det värt att lägga märke till följande aspekter:

+ Syntaxen för en <code>for-loop</code>. 
  + Vi skapar först en <code>int</code> som representerar indexpositionen i arrayen och tilldelar den värdet 0 (för att starta på den första positionen i arrayen). 
  + Vi säger därefter att loopen ska fortsätta köras __tills dess att__ <code>i</code> inte längre är mindre än 10 (<code>i < arr.Length</code>). 
  + Därefter så exekveras koden i loopen så att vi under den första iterationen får <code>arr[0] == search</code>. Då detta inte stämmer så hoppar vi upp till <code>i++</code> som kommer att öka värdet på <code>i</code> så att vi under nästa iteration istället får <code>arr[1] == search</code> osv.
+ Egenskapen <code>Length</code> hos arrayer som tillåter oss att hämta längden hos en array. I ovan fall så skulle vi därför få 10.

## Uppgiftsförteckning ##

Uppgift 1 | De första 100 positiva heltalen
----------|-------------------------------
Beskrivning | Skriv en metod, <code>PrintNumbers</code>, som skriver ut alla positiva heltal från 1 till och med 50.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
void PrintNumbers(){
  for(int i = 1; i <= 50; i++){
    Console.WriteLine(i);
  }
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 2 | Strukturerad utskrift
----------|-------------------------------
Beskrivning | Skriv en metod, <code>PrintNumbersTwo</code>, som skriver ut alla positiva heltal från 1 till och med 50. Metoden ska skriva ut heltalen i intervaller av 10. Dvs. att utskriften ska följa formatet nedan:<br><br>1, 2, 3, ..., 10<br>11, 12, 13, ..., 20<br> ... <br> 41, 42, 43, ..., 50

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
void PrintNumbers(){
  for (int i = 1; i <= 50; i++)
  {
      if(i == 10)
      {
        Console.Write(i);
        Console.WriteLine();
      }
      else if (i == 20)
      {
        Console.Write(i);
        Console.WriteLine();
      }
      else if (i == 30)
      {
        Console.Write(i);
        Console.WriteLine();
      }
      else if (i == 40)
      {
        Console.Write(i);
        Console.WriteLine();
      }
      else if (i == 50)
      {
        Console.Write(i);
        Console.WriteLine();
      }                   
      else
        Console.Write(i + ", ");
  }
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 3 | Strukturerad utskrift II
----------|-------------------------------
Beskrivning | Skriv en metod, <code>NestedPrint</code>, som skriver ut följande mönster:<br><br> <code>*</code> <br> <code>**</code> <br> <code>***</code> <br> <code>****</code> <br> <code>*****</code> <br><br> **TIPS!** För att lösa denna uppgift så rekommenderas det att du nyttjar nästlade loopar, dvs. en loop inuti en annan. Ha i åtanke att all kod i den inre loopen kommer att köras __för varje__ iteration i den yttre loopen. Nyttja gärna debugging i Visual Studio för att felsöka om något blir tokigt eller helt enkelt för att följa med i koden.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
void NestedPrint(){
  for(int i = 1; i <= 5; i++)
  {
    for(int j = 1; j <= i; j++)
    {  
      Console.Write("*");
    }
    // Används för att "gå till nästa rad", dvs. en break-line.
    Console.Write("\n"); // Går även att byta ut mot Console.WriteLine();
  }
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 4 | Strukturerad utskrift III
----------|-------------------------------
Beskrivning | Skriv en metod, <code>NestedPrintTwo</code>, som skriver ut följande mönster:<br><br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <code>*</code> <br style="display:block; content:""; margin-top:-18px;">&nbsp;&nbsp;&nbsp;&nbsp; <code>**</code> <br style="display:block; content:""; margin-top:-18px;">&nbsp;&nbsp;&nbsp; <code>***</code> <br style="display:block;content:"";margin-top:-18px;">&nbsp;&nbsp; <code>****</code> <br style="display:block;content:"";margin-top:-18px;">&nbsp; <code>*****</code>

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
void NestedPrintTwo(){
  for(int i = 1; i <= 5; i++)
  {
    for(int j = 1; j <= i; j++)
    {  
      Console.Write("*");
    }
    // Används för att "gå till nästa rad", dvs. en break-line.
    Console.Write("\n"); // Går även att byta ut mot Console.WriteLine();
  }
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 5 | Strukturerad utskrift IV
----------|-------------------------------
Beskrivning | Skriv en metod, <code>NestedPrintThree</code>, som tar emot ett heltal som användaren anger. Metoden ska sedan iterera så pass många gånger som heltalet representerar och, för varje iteration, skriva ut enligt följande mönster:<br><br>Givet heltalet 7 som input:<br> 1 <br style="display: block; content: ""; margin-top: -18px;"> 22 <br style="display: block; content: ""; margin-top: -18px;"> 333 <br style="display: block; content: ""; margin-top: -18px;"> 4444 <br style="display: block; content: ""; margin-top: -18px;"> 55555 <br style="display: block; content: ""; margin-top: -18px;"> 666666 <br style="display: block; content: ""; margin-top: -18px;"> 7777777

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
void NestedPrintThree(int iterations){
  for(int i = 1; i <= iterations; i++)
  {
    for(int j = 1; j <= i; j++)
    {  
      Console.Write(i);
    }
    Console.WriteLine();
  }
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 6 | Strukturerad utskrift V
----------|-------------------------------
Beskrivning | Skriv en metod, <code>NestedPrintFour</code>, som tar emot ett heltal som användaren anger och skriver ut följande mönster:<br><br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <code>*</code> <br> &nbsp;&nbsp;&nbsp;&nbsp; <code>***</code> <br> &nbsp;&nbsp;&nbsp; <code>*****</code> <br>&nbsp;&nbsp; <code>*******</code> <br>&nbsp; <code>*********</code> <br><br> **Notera** att enbart udda antal <code>*</code> skrivs ut per rad. Antalet rader som skrivs ut bestäms av det heltal som tas emot som argument.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
void NestedPrintFour(int iterations){
   for(int i = 0; i < iterations; i++)
   {
      for(int j = 1; j <= iterations-i; j++)
        Console.Write(" ");
      for(int k = 1; k <= 2 * i-1; k++)
        Console.Write("*");
     Console.WriteLine();
   }
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 7 | Summan av alla heltal mellan 1-100
----------|-------------------------------
Beskrivning | Skriv en metod, <code>GaussianSum</code>, som skriver ut summan av alla positiva heltal från 1 till och med 100. <br>**OBS!** Resultatet av beräkningen är 5050, men detta ska beräknas i metoden. Du ska mao. inte hårdkoda resultatet och skriva ut det.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
void GaussianSum(){
  int sum = 0;
  for (int i = 1; i <= 100; i++)
  {
    sum += i;
  }
  Console.WriteLine(sum);
}

// alt. lösning
void GaussianSum(){
  Console.WriteLine(100(100+1)/2));
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 8 | Beräkna medelvärdet
----------|-------------------------------
Beskrivning | Skriv en metod, <code>Average</code>, som beräknar medelvärdet av heltal som anges av användaren. Metoden ska fortsätta ta emot heltal tills dess att användaren anger <code>-1</code>. När detta sker så beräknas medelvärdet vilket metoden sedan skriver ut __och__ returnerar. <br><br>Ett körexempel av metoden skulle kunna efterlikna nedan interaktion:<br><br> Ange ett heltal: 50 <br><br> Ange ett heltal: 11 <br><br> Ange ett heltal: 116 <br><br> Ange ett heltal: -1 <br><br> Medelvärdet är: 59

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
int Average()
{
    int sum, count, input;
    sum = count = input = 0;

    while (input != -1)
    {
        Console.Write("Ange ett heltal: ");
        int.TryParse(Console.ReadLine(), out input);
        if (input == -1)
            break;
        sum += input;
        if (input != 0)
            count++;
    }

    if(count == 0)
    {
        Console.WriteLine("Beräkning kan ej genomföras");
        return 0;
    }
    else
    {
        Console.WriteLine("Medelvärdet är: " + (sum / count));
        return sum / count;
    }
    return 0;
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 9 | Fakultet (matematik)
----------|----------
Beskrivning | Skriv en metod, <code>CalculateFactorial</code>, som tar emot ett heltal som argument och skriver ut fakulteten hos det talet. <br><br> **OBS!** För att beräkna fakulteten hos ett tal så beräknar man produkten hos alla heltal - från och med 1 - till och med heltalet i fråga. Dvs. att om vi exempelvis vill beräkna fakulteten för heltalet 5 så skulle det se ut enligt: !5 = 1 * 2 * 3 * 4 * 5 vilket ger oss 120. __Notera__ att heltalet i fråga måste vara större än 0, annars kan ingen beräkning ske.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
void CalculateFactorial(int input){
  if(input > 0){
    for(int i = 1; i < input; i++){
      input *= i;
    }
    Console.WriteLine("Fakulteten är: " + input);
  }
  else
    Console.WriteLine("Heltalet måste vara större än 0!");
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 10 | Rekursiv metod (Fakultet II)
----------|-------------------------------
Beskrivning | En rekursiv metod är en metod som anropar sig själv tills dess att ett s.k. "basfall" uppnås. Denna typ av metod är mer vanligt förekommande i funktionella språk, men det är fullt möjligt att nyttja dem även i <code>C#</code>. Fördelarna med denna typ av metoder är att de resulterar i mindre kod och oftast är mer resurseffektiva (dvs. snabbare). Nackdelarna är det kan vara svårt att förstå sig på processen samt att det är betydligt svårare att felsöka dem i jämförelse med vanlig iteration.<br><br>Ett exempel på rekursion skulle vara följande:<br> <code>string Rec(int n) {<br>// Kontrollera att heltalet är ett positivt tal.<br>&nbsp; if (n <= 0)<br>&nbsp;&nbsp; return n + " must be higher than -1";<br>&nbsp; else if (n > 9){<br>&nbsp;&nbsp; Console.Write(n);<br>&nbsp;&nbsp; return "Completed"; // När vi har nått 10 så vill vi avsluta<br>&nbsp; }<br>&nbsp; else<br>&nbsp;{<br>&nbsp;&nbsp; Console.Write(n + ", ");<br>&nbsp;&nbsp; return Rec(n + 1); // Rekursivt anrop. 1 + 1 -> 2 + 1 osv.<br>&nbsp; }<br>}</code> <br><br> Där metoden <code>Rec</code> räknar från det heltal som skrivs in till och med 10 och skriver ut följden i konsolen.<br><br> Uppgiften är att försöka lösa Uppgift 9 (Fakultet) på nytt fast genom att nyttja rekursion istället.<br><br>**OBS** att denna uppgift är svår och egentligen faller utanför kursens ramar (dvs. att innehållet är överkurs). Tanken med uppgiften är att introducera begreppet rekursion samt tillhandahålla möjligheten att testa på det.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
void CalculateFactorial(int input){
  if(input == 0)
    return 1;
  else
    return input * CalculateFactorial(input - 1);
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 11 | Primtal?
----------|----------
Beskrivning | Skriv en metod, <code>IsPrime</code>, som tar emot ett heltal och avgör om heltalet är ett primtal eller ej. <br><br> Ett primtal är ett heltal som är större än 1 och som enbart är jämnt delbart med 1 eller sig självt. <br><br> Exempelvis så är 2, 3 och 5 primtal medan 4 och 6 inte är det då de även är jämnt delbara med 2. <br><br> **TIPS!** Nyttja modulus och iteration för att kontrollera om det finns fler än två (<code>1 resp. talet självt</code>) faktorer. Tänk på att jämna tal, utöver <code>2</code>, inte kan vara primtal.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
bool IsPrime(int input){
  // De första fallen kan hanteras via selektion.
  if (input == 1) return false;
  if (input == 2) return true;

  for (int i = 2; i * i <= input; i++)
  {
      if (input % i == 0)
          return false;                
  }
  // Om talet har passerat loopen så är det ett primtal.
  return true;
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 12 | Alla primtal upp till...
----------|----------
Beskrivning | Skriv en metod, <code>PrimeNumbers</code>, som tar emot ett heltal och skriver ut samtliga primtal från 1 upp till och med det heltalet. <br><br> **TIPS!** Nyttja din implementation från Uppgift 10 för att lösa uppgiften.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
void PrimeNumbers(int input){
  // De första fallen kan hanteras via selektion.
  if (input < 2)
    Console.WriteLine("Ange ett heltal större än 1.");
  else
  {
    for (int i = 1; i <= input; i++)
    {
      if(IsPrime(i))
        Console.WriteLine(i + " is a prime.");
    }
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 13 | Fibonacci
----------|----------
Beskrivning | Skriv en metod, <code>Fibonacci</code>, som tar emot ett heltal och skriver ut tal i Fibonnaci-sekvensen. Antalet tal som skrivs ut avgörs av det angivna heltalet. <br><br> Ett Fibonnaci-tal är summan av de två föregående talen i en sekvens av heltal. Exempelvis är de första 5 Fibonnaci-talen: 0 1 1 2 3. Vi kan i denna talföljd identifiera det tidigare nämnda mönstret givet <code>0+1 = 1</code>, <code>1+1 = 2</code>, <code>1+2 = 3</code> osv.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
void Fibonacci(int input)
{
    int n1, n2 = 1, n3;
    n1 = n3 = 0;

    Console.WriteLine(n1);
    Console.WriteLine(n2);

    for (int i = 2; i < input; i++)
    {
        n3 = n1 + n2;
        Console.WriteLine(n3);
        n1 = n2;
        n2 = n3;
    }
}

Alt. lösning:
void Fibb(int input)
{
    int i = 0;
    for (int n1 = 0, n2 = 1, n3 = 0; i < input; n3 = n1 + n2, n1 = n2, n2 = n3, i++)
    {
        Console.WriteLine(n1);
    }
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 14 | Multiplikationstabellen för X
----------|-------------------------------
Beskrivning | Skriv en metod, <code>CalculateMultTable</code>, som tar emot ett heltal som argument och returnerar en array av heltal. Metoden ska beräkna multiplikationstabellen (från 1 till och med 10) för heltalet och bygga upp en array innehållandes denna multiplikationstabell. <br><br>Givet exempelvis heltalet 3 så ska en array returneras som innehåller följande värden:<br>[3, 6, 9, 12, 15, 18, 21, 24, 27, 30].

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
int[] CalculateMultTable(int input){
  int[] arr = new int[10];
  
  for(int i = 1; i <= arr.Length; i++){
    arr[i-1] = input * i;
  }
  
  return arr;
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 15 | Utskrift av arrayer
----------|-------------------------------
Beskrivning | Skriv en metod, <code>PrettyPrint</code>, som tar emot en array av heltal som argument och inte returnerar någonting. Problemet med Uppgift 1 är att vi inte kan skriva ut innehållet i den array som skickas tillbaka i nuläget. Om vi exempelvis nyttjar <code>Console.WriteLine(CalculateMultTable(3));</code> så kommer vi enbart att skriva ut dess datatyp snarare än innehållet i arrayen. För att skriva ut innehållet så behöver man istället peka på vilket element man specifikt vill skriva ut och det är detta <code>PrettyPrint</code> är ämnad att utföra. <br><br>Metoden ska skriva ut en array enligt följande format: 5, 10, 15, 20, 25, 30, 35, 40, 45, 50<br><br>**NOTERA** att det alltså inte ska förekomma ett kommatecken efter det sista värdet. Metoden ska även kunna skriva ut innehållet i en array av heltal oavsett dess storlek.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
void PrettyPrint(int[] input){  
  for(int i = 0; i < input.Length; i++){
    if(i == input.Length-1)
      Console.Write(input[i]);
    else
      Console.Write(input[i] + ", ");
  }
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 16 | Största värdet i en array
----------|-------------------------------
Beskrivning | Skriv en metod, <code>HighestNumber</code>, som tar emot en array av heltal som argument och returnerar det största värdet i arrayen.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
int HighestNumber(int[] input){
  int max = 0;
  for(int i = 0; i < input.Length; i++){
    if(input[i] < max)
      max = input[i];
  }
  return max;
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 17 | Medelvärdet i en array
----------|-------------------------------
Beskrivning | Skriv en metod, <code>AverageNumber</code>, som tar emot en array av heltal som argument och returnerar medelvärdet av alla värden i arrayen.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
int AverageNumber(int[] input){
  int sum = 0;
  for(int i = 0; i < input.Length; i++){
    sum += input[i];
  }
  return sum / (input.Length-1);
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 18 | Summering av arrayer
----------|-------------------------------
Beskrivning | Skriv en metod, <code>SumArrays</code>, som tar emot två arrayer av heltal som argument (<code>arrayA och arrayB</code>) och returnerar en array - <code>arrayC</code> - som innehåller summan av talen på resp. position. Dvs. att om värdet på position 0 i <code>arrayA</code> är 5 och värdet på position 0 i <code>arrayB</code> är 13 så ska position 0 i <code>arrayC</code> innehålla värdet 18 osv.<br><br> **OBS!** Metoden kan utgå från att arrayerna alltid är av samma längd.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
int[] SumArrays(int[] arrayA, int[] arrayB){
  int[] arrayC = new int[arrayA.Length];
  
  for(int i = 0; i < arrayA.Length; i++){
    arrayC[i] = arrayA[i] + arrayB[i];
  }
  return arrayC;
}
```
</details>

{::options parse_block_html="false" /}

---
