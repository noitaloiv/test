---
layout: home
title: Visual Studio
icon: fa-home
order: 2
---

# Introduktion till utvecklingsmiljön Visual Studio #
### <a name="content"></a>Innehållsförteckning ###

På denna sida så finner du information om hur man sätter igång med Visual Studio, information om VS-projekt och överlag matnyttig kunskap för miljön.

- Installation, versioner och fjärranslutning ([Hoppa hit](#install))
- Att skapa projekt i Visual Studio ([Hoppa hit](#projects))
  - Konsolapplikationer ([Hoppa hit](#console))
- Projektmappen och relevanta filer ([Hoppa hit](#projectfolder))
- Matnyttigt i Visual Studio ([Hoppa hit](#matnyttigt))
  - Solution Explorer ([Hoppa hit](#solutionExplorer))
  - "Debugging" och felsökning ([Hoppa hit](#debugging))
  - Fönster i Visual Studio och radnumrering ([Hoppa hit](#vsWindows))
  - Demoprojekt ([Hoppa hit](#demo))

# <a name="install"></a>Installation, versioner, fjärranslutning #
Visual Studio finns att ladda ned gratis både för Mac ([Länk till nedladdning](https://visualstudio.microsoft.com/vs/mac/)) och för Windows. För att ladda ned programmet till Windows så behöver du dock nyttja ditt studentkonto via Microsoft Dreamspark ([Dreamspark login](https://e5.onthehub.com/WebStore/Welcome.aspx?vsro=8&ws=99931b94-20fd-e111-bd05-f04da23e67f6&JSEnabled=1)).

**Notera** att Mac-versionen inte alltid fungerar felfritt och att det därför kan vara fördelaktigt att istället fjärransluta till datorerna i laborationssalarna. Om du inte vet hur man etablerar en fjärranslutning till dessa datorer så finns instruktioner att tillgå här: [Fjärranslutning till Ekonomikum](https://www.ekonomikum.uu.se/service/itsupport/remotedesktop)

## Att starta Visual Studio ##
Det första steget blir ju såklart att starta en instans av programmet. Förutsatt att du sitter i en utav laborationssalarna så uppnås detta enklast genom att klicka på Windows-tangenten (till höger om vänster CTRL-tangent) och därefter söka efter Visual Studio genom att börja skriva "v-i-s-u…" osv. Visual Studio 20XX kommer då att dyka upp i högerkolumnen och du behöver då enbart klicka på ikonen för att skapa en instans av programmet. Det kommer mao. efterlikna Figur 1.

![Visual Studio i laborationssal](/Images/image11.png)

*OBS!* Det är Visual Studio du vill öppna (_Visual Studio 2017_ i ovan bild), inte någon utav de
andra applikationerna. Notera att vi numera har Visual Studio 2013 installerat i
laborationssalarna och att vi i första hand rekommenderar det över Visual Studio 2013.
Den första gången du startar Visual Studio så kommer du möjligtvis att bemötas av en pop-up
som ber dig logga in. Detta behöver du *INTE* göra, utan klicka istället på "Not now". Du
behöver även välja ett tema. Detta har ingen som helst inverkan på din kod och kan även
ändras i efterhand. Därefter kan det ta ett par minuter innan programmet startar och du ser
Visual Studios "startsida".

# <a name="projects"></a>Att skapa projekt i Visual Studio # ([Hoppa till innehållsförteckningen](#content))
När du väl har startat Visual Studio (VS) så behöver du välja ett projekt. I VS så kan man
däremot skapa flera olika typer av projekt såsom konsol-applikationer, Windows
Forms-applikationer och Webbaserade tjänster. För resp. projekttyp så autogenereras viss kod
åt dig som utvecklare och denna kod ser betydligt annorlunda ut beroende på vilket projekt
du vill arbeta i. Det är således viktigt att man väljer korrekt projekttyp. I denna kurs kommer
ni enbart att använda er utav en s.k. konsol-applikation.

## <a name="console"></a>Konsolapplikationer ##
För att skapa ett nytt projekt så finns det två tillvägagångssätt: Du kan antingen göra detta
genom att klicka på "New Project" på startsidan i Visual Studio eller genom att navigera från
fliken "File" -> "New" -> "Project". I Figur 2 så ser du att det, som tidigare nämnt, finns flera
olika typer av projekt. Men utöver att det är viktigt att kontrollera vilken projekttyp som är
markerad så gäller det även att vara noggrann med att korrekt programmeringsspråk har valts.
I nedan bild ser du i vänsterspalten att "Visual C#" är markerat. Dvs. att det bör mer eller mindre
se likadant ut för dig när du skapar ett eget projekt.

![En C# konsolapplikation.](/Images/image13.png)

Notera att du, om du arbetar i laborationsmiljön, först och främst behöver ändra på "Location". "Location" representerar 
den mapp där du kommer att spara ditt projekt.
Anledningen bakom detta är att hårddisk C: har begränsat med utrymme på laborationsdatorerna vilket ev. kan resultera i att ditt
arbete försvinner. För att undvika detta så bör du istället välja att spara dina projekt på hårddisk U:. Vi rekommenderar
att här att du först skapar två mappar så att du alltid enkelt kan hitta tillbaka till dina projektfiler, t.ex. "Visual Studio"
som i sin tur innehåller en mapp vid namn "Projects". I Visual Studio så ändrar du därefter "Location" till mappen "Projects".

*OBS!* Tänk även på att namnge ditt projekt något rimligt. Exempelvis "GP_Inlamnning1" eller "GP_ChatClient", beroende på 
vilken uppgift och kurs du håller på med etc. Detta underlättar för dig att särskilja projekt från olika kurser.

När du väl har valt platsen där projektet ska sparas, ett projektnamn och klickat på "OK" så möts du därefter av en 
klass kallad "Program" vilken innehåller en metod, "Main". Det bör efterlikna nedan kodexempel (minus kommentarerna). 
```csharp
namespace GP_ChatClient // Namnet beror på vad du har döpt ditt projekt till.
{
  class Program
  {
    static void Main(string[] args)
    {
      // Här placerar du din kod.
    }
  }
}
```
Det är Main-metoden som kommer att exekveras när du startar din applikation och det är därför här du, 
till en början, kommer att vilja placera majoriteten av din kod. Detta innefattar bl.a. funktionaliteten
involverad i att läsa användarinput och skriva ut saker. Du kommer under kursens gång att övergå 
till att placera funktionalitet i s.k. metoder vilka du sedan kommer att anropa från Main-metoden.

# <a name="projectfolder"></a>Projektmappen och relevanta filer # ([Hoppa till innehållsförteckningen](#content))
Under denna sektion hittar du information om exempelvis hur du kan navigera till projektmappen, vad du bör tänka på
när du sparar dina filer och hur man "packar ihop" ett projekt på rätt sätt inför inlämningar.

# Vart hittar jag mina filer och projekt? #
Förutsatt att du har följt instruktionerna gällande hur man skapar ett projekt (dvs. i förhållande till "Location") så
kommer dina filer och projekt att vara sparade på hårddisk U:. Du kan enkelt navigera hit på två sätt antingen via "File Explorer" i
Windows eller genom Visual Studio (om du har projektet öppet där). 

För att navigera via "File Explorer" så öppnar du File Explorer (WIN + E alt. mapp-ikonen i navigationsbaren). 
Du möts då av "Den här datorn" ("This PC") och där hittar du direkt hårddisk K, U och X under "Network locations" (se nedan bild).

![Hårddisk U: i laborationsmiljön.](/Images/image2.png)

Därefter dubbelklickar du på ikonen och hittar där mappen "Visual Studio" . Den
mappen innehåller i sin tur mappen "Projects" och det är i denna du hittar samtliga av dina
projekt.

Det andra alternativet, att navigera hit via Visual Studio (om ett projekt är öppet), gör du genom att 
högerklicka på din "Solution"-fil i Solution Explorer (som du ser i högerspalten när du
arbetar i VS). Nedan bild visar hur detta ser ut.

!["Open Folder in File Explorer" i VS.](/Images/image8.png)

Oavsett tillvägagångssätt bemöts du då utav din projektmapp som ser ut något i stil med
nedan.

![Projektmappen för ett VS-projekt.](/Images/image1.png)

Notera två saker i ovan bild:
- Mappen "Library" är den mapp som innehåller samtliga klass-filer såsom den tidigare
nämnda "Program"-klassen. Dvs. alla filer som du har skrivit kod i och resterande filer som
VS har autogenererat åt dig.
- Filen "Library.sln" är din s.k. "Solution"-fil och det är med denna du kan öppna ditt projekt (genom att dubbelklicka på den)
från projektmappen istället för att gå via "Open project" i VS.

# Hur ska man "packa ihop" projekt?  #
För att spara ditt arbete samtidigt som du arbetar i Visual Studio så räcker det om du trycker
på CTRL + S (eller CTRL + Shift + S för samtliga filer), precis som när du arbetar i
Microsoft Word eller liknande program. Alt. så kan du navigera till fliken "File" och från den
klicka på "Save".

När man sedan är redo för att lämna in sin kod så är det dock inte möjligt att enbart ladda upp en specifik fil
eller en specifik mapp. Man behöver nämligen inkl. *ALLA* filer och mappar. Du
behöver därför paketera (komprimera) den huvudmapp som innehåller resterande filer. I samband med
tidigare avsnitt så beskrevs det hur man navigerar till ett projekt, antingen via VS eller genom Windows. 
Dock så placeras vi i detta fall _inuti_ själva projektmappen, där vi ser två mappar och en solution-fil (.sln). 
Vi behöver därför "backa tillbaka" ett steg för att peka på den mapp som omsluter precis alla filer och mappar (se nedan bild).

![Huvudmappen som innehåller hela projektet.](/Images/image4.png)

För att sedan faktiskt paketera (komprimera) mappen så högerklickar man på mappen, väljer "IZArc" och klickar sedan på "Add to _MappensNamn_.zip".
Det är sedan denna (.zip-filen) fil som du lämnar in inför rättning.

![IZArc för att komprimera mappar.](/Images/image7.png)

Om du inte arbetar via universitetets datorer så har du nödvändigtvis inte just IZArc
installerat och detta är helt okej, huvudsaken är att du nyttjar något program som kan
komprimera filer. Om du exempelvis använder Windows 10 så kan du istället nyttja:
Högerklick -> "Send to" -> "Compressed (zipped) folder".

# <a name="matnyttigt"></a>Matnyttigt i Visual Studio # ([Hoppa till innehållsförteckningen](#content))
Visual Studio (VS) erbjuder oerhört mycket funktionalitet, olika typer av fönster, möjligheten
att testa sin kod i realtid och mycket mer. En nackdel med detta är dock att du med största
sannolikhet aldrig kommer att behöva stora delar av det som erbjuds. Således behandlar denna
sektion olika aspekter av VS som du sannolikt kommer att stöta på eller åtminstone kan dra
nytta utav.

## <a name="solutionExplorer"></a>Solution Explorer ##
Solution Explorer är ett fönster i Visual Studio (VS) där du kan se det projekt som du för närvarande arbetar i
och samtliga filer som detta projekt innehåller. Fönstret är generellt placerat till höger i VS och, även fast det 
kanske inte är högst aktuellt under denna kurs, så kommer det att nyttjas flitigt under framtida kurser på programmet.

I Solution Explorer kan du bl.a. lägga till en ny fil, t.ex. en ny klassfil, textfil eller dylikt. Du
gör detta genom att högerklicka på ditt projekt -> Navigera till Add -> Därefter till "New
Item". Bilden nedan visar hur du navigerar dit.

!["Add item" genom "Solution Explorer".](/Images/image6.png)

Alternativt så kan du välja "Existing Item". Detta är relevant om du t.ex. vill lägga till en redan existerande fil, 
t.ex. en klass från ett annat projekt.

På samma sätt så är det möjligt att exkludera och inkludera filer samt att ta bort dem permanent.
Detta uppnås genom att t.ex. högerklicka på filen och välja "Exclude From Project" (se nedan bild).
"Exclude" innefattar att du exkluderar filen från det nuvarande projektet i VS, men du tar inte
bort filen. "Include" är motsatsen till "Exclude" och "Delete" innebär, som namnet antyder, att du tar bort filen
permanent.

!["Exclude From Project" och "Delete".](/Images/image9.png)

Som du även ser i bilden ovan så har du möjligheten att ändra namn på filer här. Fördelen med att
ändra namnet i denna meny är att du samtidigt erbjuds möjligheten att ändra referenserna i projektet för denna fil till det nya namnet. 
Detta blir mer aktuellt under framtida programmeringskurser.

## <a name="debugging"></a>"Debugging" och felsökning ##
> _90% of coding is debugging. The other 10% is writing bugs._
> - Bram Cohen

> _If debugging is the process of removing bugs, then programming must be the process of putting them in._
> - Edsger W. Dijkstra

Tyvärr så finns det en grad av sanning i ovan påståenden vilket innefattar att debugging och felsökning är något av det
viktigaste att snabbt lära sig och ta till sig som en programmerare. Fördelen med att nyttja Visual Studio som utvecklingsmiljö
är att den förenklar denna process markant. Du har exempelvis möjligheten att "följa med" i din kod samtidigt som den exekveras,
Visual Studio säger ifrån om du försöker exekvera ett program som innehåller fel och du ges även - förhållandevis - tydlig information
om vad som har gått fel.

För att "följa med" i koden så uppnår man detta genom att placera en s.k. "breakpoint" i vänsterspalten (den röda pricken i nedan bild).

![En "Breakpoint" i Visual Studio.](/Images/image12.png)

Notera att en breakpoint enbart kan placeras på samma rad där det förekommer kod. För att ta bort en
breakpoint så räcker det med att du klickar på den igen. För att ta bort alla breakpoints i hela
projektet samtidigt kan du, istället för att manuellt klicka på resp. breakpoint, navigera till 
Debug-fliken -> "Delete All Breakpoints". Alternativt så kan du nyttja kortkommandot CTRL + SHIFT + F9.

När du sedan exekverar ditt program genom att klicka på Start (eller F5) så kommer
programmet att stanna upp vid din placerade breakpoint. Från denna punkt har du då
möjligheten att gå igenom din kod, steg-för-steg. Detta gör du smidigast med tangenterna F10 samt
F11. Under tiden som du "stegar igenom" din kod så kan du även exempelvis kontrollera
innehållet i en variabel genom att placera muspekaren över variabeln (se nedan bild). Detta är
särskilt givande när du arbetar med iteration/loopar och vill se vad som händer varje iteration (varje cykel).

![Kontrollera variabler under run-time.](/Images/image3.png)

## "Error List" ##
I Visual Studio har du ytterligare ett fönster, placerat på botten av VS. I detta fönster hittar du
ev. fel i koden som kommer att hindra dig från att exekvera ditt program tills dessa fel är åtgärdade.
Exempelvis om du har glömt ett avslutande semikolon eller försöker göra något som VS inte
tillåter. I din "Error List" får du då information om vart felet är, vad det beror på och i vilken fil
felet förekommer (se nedan bild). Du kan även dubbelklicka på dessa felmeddelanden för att
direkt nå platsen där felet förekommer, du behöver mao. inte leta igenom din kod.

!["Error List" i Visual Studio.](/Images/image10.png)

## <a name="vsWindows"></a>Fönster i Visual Studio och radnumrering ##
Skulle du av en händelse oavsiktligt stänga ned antingen "Solution Explorer", "Error List" eller
något annat fönster i VS så är det inga problem att återställa dessa. Du gör detta genom att
navigera till View-fliken -> Identifiera det fönster du vill öppna igen -> Klicka på det
alternativet.

Utöver det så är radnumrering eller "lines" inte aktiverat i Visual Studio ifrån början. Detta är
mao. något man måste aktivera manuellt. Detta är självfallet inget krav, men om det är något
som du personligen föredrar så uppnår du detta genom att navigera till Tools-fliken ->
Navigera till Options -> Du kommer då direkt till "Environment" (här kan du även ändra
temat för Visual Studio om du vill). För att aktivera radnummer så behöver du därefter
navigera till "Text Editor" i vänsterspalten -> Välj sedan undermenyn "All Languages" och
checka i checkboxen för "Lines numbers".

## <a name="demo"></a>Demoprojekt ##
[Demoprojekt](DemoProjekt.zip)
Om du känner för att testa på utvecklingsmiljön så hittar du här ett lite mindre demoprojekt som du kan nyttja för att
bli familjär med Visual Studio-miljön och testa på några utav uppgifterna som du hittar på webbplats.

Testa exempelvis på att exekvera ett program (F5), att "följa med" i koden och bli familjär med hur fönster och dylikt
ser ut i Visual Studio.

Ett exempel på vad du kan testa i projektet är hur "felsäkert" programmet är genom att skriva
in text istället för ett årtal när programmet frågar om ditt födelseår. Du märker då att
programmet kraschar och att ett felmeddelande dyker upp, <code>FormatException</code>. Detta beror på att
vi försöker konvertera text till ett heltal (<code>Convert.ToInt32</code>) vilket inte är möjligt. Reflektera kring
hur man kan undvika detta problem eller, om du vill utmana dig själv, lös problemet!
