---
title: Strängar
icon: fa-th
order: 6
---

# <a name="strings"></a>Strängmanipulering #
En sträng är egentligen en array utav tecken (<code>char</code>). Detta innebär att vi kan behandla en sträng likt hur vi behandlar en array. Föreställ dig exempelvis att vi har en sträng i stil med: 
```cs
string hello = "Hello World!";
```
och att vi är intresserade av att hämta det tecken som förekommer på just indexposition 4. Vi kan uppnå detta genom att skriva <code>hello[4]</code> (som då är 'o'). <br><br> Vi skulle även kunna iterera över en sträng, likt hur vi skulle göra för en array som består av heltal. Exempelvis enligt:
```cs
string text = "Hello everybody!";
char c = '';
for (int i = 0; i < text.Length; i++)
{
    c = text[i]; // nyttjar indexering. 'c' kommer första iterationen att innehålla 'H' sedan 'e' osv.
}
```
Datatypen <code>string</code> innehåller även många olika inbyggda metoder som gör det möjligt att enkelt hantera och manipulera strängar på olika sätt. Några exempel på några vanligt förekommande metoder är <code>IndexOf</code>, <code>Substring</code>, <code>Split</code>, <code>ToUpper</code> och <code>ToLower</code>. I denna sektion så förväntas du öva på dessa olika former av strängmanipulering.

## Uppgiftsförteckning ##

Uppgift 1 | StringLength
----------|-------------------------------
Beskrivning | Skriv en metod, <code>StringLength</code>, som tar emot en sträng som argument och beräknar längden på strängen (antalet tecken). Då en <code>string</code> kan, som tidigare nämnt, tolkas som en array av bokstäver så kan man självfallet nyttja egenskapen <code>Length</code> precis som vi har gjort i tidigare uppgifter men detta är inte syftet sett till uppgiften. Metoden <code>StringLength</code> ska dock beräkna längden via iteration istället.<br><br>**TIPS!** Nyttja en <code>foreach</code>-loop för att iterera över strängen.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
int StringLength (string input){
  int length = 0;
  foreach(char c in input)
  {
      length++;
  }
  return length;
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 2 | Reverse string
----------|-------------------------------
Beskrivning | Skriv en metod, <code>StringReversed</code>, som tar emot en sträng som argument och skriver ut strängen i bakvänd ordning. Dvs. givet strängen <code>"Hello world!"</code> så ska <code>"!dlrow olleH"</code> skrivas ut.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
void StringReversed (string input){
  for(int i = 0; i < input.Length; i++)
  {
      Console.Write(input[i]);
  }
}
```
</details>

{::options parse_block_html="false" /}

---

Uppgift 3 | RemoveSpaces
----------|-------------------------------
Beskrivning | Skriv en metod, <code>RemoveSpaces</code>, som tar emot en sträng som argument och skriver ut den efter att alla mellanslag har tagits bort från strängen. Om inga mellanslag förekommer i strängen så ska "No spaces in string." skrivas ut istället. <br><br>**TIPS!** Nyttja den inbyggda metoden <code>Split</code>.

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs
void RemoveSpaces (string input){
  string[] noSpaces = input.Split(' ');
  if(noSpaces.Length < 2)
      Console.WriteLine("No spaces in string.");
  else
  {  
      string output = string.Empty;
    
      for(int i = 0; i < noSpaces.Length; i++)
      {
          output += noSpaces[i];
      }
      
      Console.WriteLine(output);
}

// Alt. lösning
void RemoveSpaces (string input){
    string output = string.Empty;
    int count = 0;

    for(int i = 0; i < input.Length; i++)
    {
        if(input[i] != " ")
            output += input[i];
        else
            count++;
    }

    if(count > 0)
        Console.WriteLine("No spaces in string.");
    else
        Console.WriteLine(output);
}
```
</details>

{::options parse_block_html="false" /}

---
