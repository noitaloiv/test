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
for (int i = 0; i < text.Length; i++)
{
  char c = text[i]; // nyttjar indexering
}
```
Datatypen <code>string</code> innehåller även många olika inbyggda metoder som gör det möjligt att enkelt hantera och manipulera strängar på olika sätt. Några exempel på några vanligt förekommande metoder är <code>IndexOf</code>, <code>Substring</code>, <code>Split</code>, <code>ToUpper</code> och <code>ToLower</code>. I denna sektion så förväntas du öva på dessa olika former av strängmanipulering.

## Uppgiftsförteckning ##

Uppgift 1 | <Name>
----------|-------------------------------
Beskrivning | <Desc>

{::options parse_block_html="true" /}

<details><summary markdown="span">Let's see some code!</summary>
  
```cs

```
</details>

{::options parse_block_html="false" /}

---
