---
title: Metoder
icon: fa-th
order: 3
---

Gällande metoder så behandlades konceptet kortfattat i inledningen, men innan vi går vidare så behöver vi först titta på syntaxen för dessa samt bilda oss en uppfattning av hur de nyttjas och varför. Vi börjar med en metodsignatur, vad är det och hur ser den ut?<br><br> En metodsignatur består utav namnet på metoden och ev. parametrar som metoden tar emot. En parameter för metoden <code>Addition</code> skulle exempelvis kunna tänkas vara 2 st. heltal som ska summeras. Dvs. något i stil med:
```cs
Addition(int num1, int num2){
  // Code goes here.
}
```
Nämnvärt är att metodens- och parametrarnas namn ska vara beskrivande. Exempelvis blir det snabbt väldigt svårt att avgöra vad en omfattande metod förväntas genomföra om dess namn är X och tar emot 14 parametrar döpta enligt x1, x2 osv.<br><br>Utöver själva metodsignaturen så behöver man även en s.k. returtyp. Det är denna som säger åt programmet vad det är, om något, som metoden ska skicka tillbaka. I fallet av metoden <code>Addition</code> så kan vi exempelvis tänka oss att det är rimligt att metoden skickar tillbaka summan som ett heltal. Dvs. enligt följande:
```cs
int Addition(int num1, int num2){
  int sum;
  // Code goes here.
  return sum;
}
```
**OBS!** Om metoden har en returtyp så __måste__ metoden också skicka tillbaka något. Om metoden inte ska skicka tillbaka något, t.ex. om den enbart förväntas skriva ut information till konsolen så nyttjas returtypen <code>void</code>.
## Uppgiftsförteckning ##

Uppgift 1 | Metodsyntax
----------|-------------------------------
Beskrivning | Skriv en lämplig metodsignatur och tillhörande returtyp för metoder som förväntas utföra följande funktion:<br><br> - Räkna ut något givet 3 st. parametrar. <br> - Avgöra om värdet hos en parameter är korrekt eller ej. <br> - Skickar tillbaka ett datum om input kan konverteras till ett sådant. Annars ska ett felmeddelande skrivas ut. <br> - Skriver ut innehållet i en array. <br><br>**OBS!** Ingen kod behöver skrivas för att lösa denna uppgift och du förväntas skriva en metodsignatur - och tillhörande returtyp - för resp. funktion.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
// Det spelar ingen roll om vi nyttjar int eller double här.
double CalculateSum(int x, double y, int z) { }

bool IsLoggedIn(string usr, string psw) { }

// Givet returtypen så måste vi returnera något, i detta fall blir det en tom DateTime.
// Om konverteringen misslyckas så har vi en else-sats som skriver ut att ett fel har uppstått.
DateTime ConvertToDate(int date) {
  // Code goes here.
  else{
    Console.WriteLine("Error.");
  }
  return new DateTime();
}

// void då vi enbart vill skriva ut innehållet i arrayen.
void PrintArray(int[] arr){ }
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 2 | KontrolleraRader
----------|-------------------------------
Beskrivning | Skriv en metod som jämför om två meningar är identiska. Metoden ska ha namnet: <code>KontrolleraRader</code>. Presentera resultatet på lämpligt sätt och reflektera kring en lämplig returtyp.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
// Notera att metoden inte nödvändigtvis måste returerna något.
// Det kan dock vara aktuellt om vi t.ex. vill nyttja resultatet i en annan metod.
bool KontrolleraRader(string a, string b){
  if(a == b)
  {
    Console.WriteLine("The strings match!");
    return true;
  }
  else
  {
    Console.WriteLine("The strings are not identical!");
    return false;
  }
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 3 | Summering av udda tal
----------|-------------------------------
Beskrivning | Skriv en metod som adderar två udda tal. Om talen inte är udda så ska ingen beräkning utföras. Användaren bör dock informeras om att ingen beräkning utförs. Denna metod är tänkt att nyttjas i en annan metod. 

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
// Notera att metoden inte nödvändigtvis måste returerna något.
// Det kan dock vara aktuellt om vi t.ex. vill nyttja resultatet i en annan metod.
int SumOddNumbers(int x, int y){
  if(x % 2 == 0 && y % 2 == 0)
    return x + y;
  else
  {
    Console.WriteLine("At least one of the numbers is even.");
    return 0; // Agerar som felkod i den metod som nyttjar denna metod.
  }
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 4 | Metoder med samma namn
----------|-------------------------------
Beskrivning | Skriv en metod, <code>PrintUserInfo</code>, som tar emot två strängar. Metoden ska sedan skriva ut informationen enligt följande format: <br><br> <code>Hello, Name!></code><br> <code>Your number is: Number</code> <br><br> Där <code>"Name"</code> är det ena argumentet och <code>"Number"</code> är det andra argumentet. <br><br> Skriv därefter ytterligare en metod med samma namn men som tar emot två strängar och ett heltal där heltalet representerar ett årtal. Denna metod ska skriva ut enligt samma format som den första metoden men även beräkna och skriva ut användarens ålder (dvs. antal år snarare än årtal).<br><br> ***OBS!*** Metoderna har samma namn men inte samma metodsignatur (två argument gentemot tre). Vi kommer att behandla detta koncept (method overloading) ytterligare i senare kurser, men i nuläget så är det tillräckligt att veta om att det existerar. 

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
void PrintUserInfo(string name, string number){
  Console.WriteLine("Hello, " + name + "!");
  Console.WriteLine("Your number is: " + number);
}

void PrintUserInfo(string name, string number, int year){
  Console.WriteLine("Hello, " + name + "!");
  Console.WriteLine("Your number is: " + number);
  Console.WriteLine("You are " + (2019 - year));
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 5 | En metod i en metod
----------|-------------------------------
Beskrivning | Skriv en metod som avgör om ett heltal är udda eller jämnt. Skriv därefter ytterligare en metod - som nyttjar den första metoden - för att antingen dividera heltalet med 2 (om det är ett _jämnt_ tal) eller dividera heltalet med 5 (om det är ett _udda_ tal).<br><br> Skriv ett metodanrop till båda metoder med korrekta argument (dvs. att argumentet är av typen <code>double</code>. ***NOTERA*** att namnet på de parametrar som anges för en metod __enbart__ existerar i det kodblock som metoden avser. Detta innefattar att du inte måste skicka en variabel med samma namn som anges i metodens parametrar. Det __enda__ som spelar någon roll är att datatypen är korrekt.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
// Notera att metoden inte nödvändigtvis måste returerna något.
// Det kan dock vara aktuellt om vi t.ex. vill nyttja resultatet i en annan metod.
bool IsOdd(double x){
  if(x % 2 != 0)
    return true;
  else
    return false;
}

double DivideOddAndEvenNumbers(double x){
  // Notera att "IsOdd(x)" är samma sak som att skriva "IsOdd(x) == true".
  // Detta då det är placerat som ett villkor i if-satsen och metoden returnerar en bool.
  if(IsOdd(x)) 
    return x / 5;
  else
    return x / 2;
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 6 | En enkel meny II
----------|-------------------------------
Beskrivning | Skriv en metod som presenterar användaren till en enklare meny med 3 alternativ. Dessa alternativ ska vara:<br><br> - Summera 3 heltal.<br> - Avgör om ett heltal är positivt eller negativt.<br> - Avgör först om 3 heltal är positiva eller negativa och sedan summera dem. Notera att enbart positiva heltal ska summeras med varandra och vice versa för negativa heltal.<br><br> Funktionaliteten ska placeras i lämpliga metoder. Med lämpligt så avses exempelvis att en metod inte bör utföra funktionaliteten för både det första och det andra menyalternativet. **OBS!** Ingen kod ska dupliceras, dvs. förekomma mer än en gång.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
void ASimpleMenu(){
  Console.WriteLine("Choose one of the following options:");
  Console.WriteLine("1. Sum 3 numbers.");
  Console.WriteLine("2. Check if a number is positive or negative.");
  Console.WriteLine("3. Check if 3 numbers are positive or negative then sum them based on category.");
  
  int.TryParse(Console.ReadLine(), out int input);
  switch(input){
    case 1:
        Console.WriteLine("The sum is: " + SumNumbers(x, y, z));
        break;
    case 2:
        Console.Write("Enter a number: ");
        int.TryParse(Console.ReadLine(), out int num);
        Console.WriteLine("The number is positive: " + IsPositive(num));
        break;
    case 3:
        Console.WriteLine("The sum of PosNeg is: " + PosNegSum());
        break;
    default:
        Console.WriteLine("Incorrect input.");
        break;
}

int SumNumbers(int x, int y, int z){
    Console.Write("Enter the first number: ");
    int.TryParse(Console.ReadLine(), out int x);
    Console.Write("Enter the second number: ");
    int.TryParse(Console.ReadLine(), out int y);
    Console.Write("Enter the third number: ");
    int.TryParse(Console.ReadLine(), out int z);
            
    return x + y + z;
}

bool IsPositive(int n){   
    if(n >= 0)
      return true;
    else
      return false;
}

int PosNegSum()
{
    Console.Write("Enter the positive number: ");
    int.TryParse(Console.ReadLine(), out int pos);

    if (IsPositive(pos))
    {
        Console.Write("Enter the negative number: ");
        int.TryParse(Console.ReadLine(), out int neg);

        if (!IsPositive(neg))
            return pos + neg;
        else
            return 0;
    }
    else
        return 0;
}
```
</details>

{::options parse_block_html="false" /}

---
