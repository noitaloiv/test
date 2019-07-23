---
title: Metoder
icon: fa-th
order: 3
---

# <a name="metod-sektion"></a>Metoder #
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
