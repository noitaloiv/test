# <a name="projectfolder"></a>Projektmappen och relevanta filer #
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
