---
title: Inledning
icon: fa-th
order: 2
---

För att lösa uppgifterna som du ser på denna sida så behöver du först skapa en konsol-applikation i Visual Studio för språket C#. Var uppmärksam när du skapar detta projekt så att du väljer **C#** och inte **Visual Basic** (som är ett annat programmeringsspåk). När du gör detta så kommer du att bemötas av koden som du ser nedan:
```cs
using System;

namespace PracticeAssignments // This name depends on what you have named your project as
{
  public class Program
  {
    public static void Main(string[] args)
    {
      // Write to console
      Console.WriteLine("Hello World!");
      Console.WriteLine("Press the Enter key to exit.");

      // Keep the terminal open until the user presses Enter.
      Console.ReadLine();
    }
  }
}
```
Det är inom *metoden* <code>Main</code> som du kommer att skriva din kod, till en början. Om vi kör koden från ovan exempel så kommer vi t.ex. att skriva ut "Hello World!" i konsolen. Konsolen kommer därefter att vänta på att du, eller användaren, klickar på Enter-tangenten innan applikationen stängs ned. Vi nyttjar alltså <code>Console.WriteLine()</code> för att skriva ut information i konsolen och <code>Console.ReadLine()</code> för att läsa in information från användaren.

För nästan varje uppgift på denna sida så förväntas det att du nyttjar dessa verktyg för att lösa uppgiften så lägg dem på minnet!

### Metod/funktion ###
Då det snabbt kan bli jobbigt att skapa en ny konsolapplikation för varje uppgift så rekommenderar vi till en början att ni arbetar enbart i <code>Main</code>-metoden och att ni separerar varje uppgift mha. kommentarer. Dvs. exempelvis enligt nedan:
```cs
public static void Main(string[] args)
{
  // Uppgift 1 - Datatyper
  bool b = ...
  
  // Uppgift 2 - Att deklarera gentemot att instansiera
  ...
}
```
Där "..." så klart representerar den kod du skriver för att lösa uppgiften.

Det finns dock ett annat, tydligare sätt att separarera uppgifterna och detta är mha. egendefinierade metoder (detta täcks ytterligare udner Metod-sektionen). Detta innefattar att du, istället för att placera all kod i <code>Main</code>-metoden, skapar en ny metod för resp. uppgiften som du sedan __anropar__ från <code>Main</code>-metoden. Exempel:
```cs
public static void Main(string[] args)
{
  // Uppgift 1 - Datatyper
  Uppgift1();
  
  // Uppgift 2 - Att deklarera gentemot att instansiera
  Uppgift2();
}

void Uppgift1(){
  ...
}
```
