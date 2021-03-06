# Agila arbetsmetoder

Att arbeta agilt eller iterativt är mest bara sunt förnuft eller en (bättre) arbetskultur.

Klassiskt har metoder för (mjukvaru)utveckling kommit från utveckling i av andra (fysiska) produkter som t.ex. att bygga en bil eller en bro. En bil designas för att sedan byggas exakt likadana kopior av. Mjukvara behöver oftast inte dupliceras på de sättet utan kan eller behöver istället fortsätta utvecklas under hela livscykeln. Skillnaden mellan mjukvara och hårdvara är stor.

En klassisk utvecklingsmetod är Vattenfallsmetoden. En av grundidéerna är att minimera sena ändringar eftersom det kan kosta väldigt mycket pengar att tex. förändra en hel fabrik sent i processen. Fokus är att bli klar med varje fas innan nästa påbörjas. Utvecklingen sker sekvensielt i ungefär dessa steg:

![Vattenfallsmodellen](img/vattenfall.png)

Ett av de absolut största problemet med att använda en såpass tung eller stelbent process för att bygga mjukvara är att steget från krav färdig produkt blir långt. Ofta vet varken team eller kund vad de vill ha förrän efter produkten är färdig och då är det oftast tungt och dyrt att att ändra.

**En väldigt viktig del i utveckling är att förstå vad det var man behövde bygga. Ofta blir det tydligt för kund, utvecklare och team efter att produkten är byggd :)**

I alla agila metoder vänder man på steken och försöker hela tiden utveckla och leverera nästa fungerande produkt så fort som möjligt. Då behöver man arbeta i korta itterationer där fokus är att bryta ner varje större uppgift till lagom stora steg att visa kunden (som kan vara mer närvarande i alla stegen). I varje steg går det då att känna på produkten och försöka försäkra sig om att man är på väg åt rätt håll. 

Längden på en utvecklingsiteration beror på men ofta från några dagar till några veckor. Det finns troligen lika många olika varianter på agila arbetsmetoder som det finns projekt eller företag. Lär er koncepten.

![Agila spiralen](img/agil-spiral.png)

Läs: 
 * https://en.wikipedia.org/wiki/Agile_software_development 
 * https://en.wikipedia.org/wiki/Waterfall_model

## Kanban

Kanban är en slags agil metod från Japan och blev känd från Toyota. Den sk. Kanban-boarden kommer härifrån likaså Cards. Se denna förklaring av att arbeta iterativt: https://www.youtube.com/watch?v=iVaFVa7HYj4 Även om han pratar om Kanban i videon gäller koncepten. Videon är vald för att den tydligt och enkelt visar hur todos kan hanteras med post-it-lappar. Scrums (nedan) motsvarighet till *Kanban-tavlan* heter *Sprint backlog*.

![Kanban board](img/kanban-board-wikipedia.jpg)

Läs: https://en.wikipedia.org/wiki/Kanban_(development) 

## Scrum

Scrum är en av de mest använda agila arbetsmetoden i mjukvaruprojekt. Den bestämmer i större detalj hur arbetet går till.

Läs: 
 * http://extra.lansstyrelsen.se/tillsynsutvecklingivast/SiteCollectionDocuments/M%C3%A5nadens%20goda%20exempel/Scrum%20p%C3%A5%20fem%20minuter.pdf (oväntat bra, enkel och grundläggande beskrivning :))
 * https://en.wikipedia.org/wiki/Scrum_(software_development)

### Roller i Scrum
**Product owner (PO)** är personen som i första hand ansvarar för att ta fram och prioritera de övergripande förändringar som ska göras i en produkt. Om andra personer (som tex. en utvecklare) vill göra en förändring sker det oftast i samtal med PO. Hen representerar kunderna. Kan (lite humoristiskt) ses som en kombination av coach, fixare och dörrvakt.

![Projekt Owner, Scrum](img/scrum-po.png)

**Scrum master (SM)** är personen som hjälper utvecklingsteamet att arbeta så effektivt som möjligt. Ofta, men inte allid, är SM del av utvecklingsteamet.

**Scrum team** är personerna som arbetar med att utveckla produkten. Ofta en grupp om 5-9 personer.

### Arbetsgången i Scrum (förenklad)

Arbetet sker i *Sprints* vilka är ungefär 2v långa (varierar beroende på projektstorlek). Det första som händer när en sprint startar är att *PO* tillsammans med utvecklarna och *SM* kommer överens om vad som ska göras under nästa sprint. De väljer ut lagom många *Product backlog items* från en *Product backlog* och lägger in på sin *Sprint backlog*. En grov estimering av varje *item* görs när den läggs till *Sprint backlog*. *PO* ansvarar för att hålla uppdaterad och prioritera *Product backlog* med alla de förändringar som behöver göras i produkten.

En *Sprint backlog* liknar ofta en *Kanban-board* och kan gärna göras med post-it-lappar som flyttas i kolumner från vänster till höger.

Efter prioriteringarna kan utvecklarna börja arbeta och meningen är att de under sprinten ska få ganska lugn och ro. Är det ändringar eller omprioriteringar som behöver göras ansvarar *SM* för samtalet med *PO* eller om det är andra saker som behöver fixas.

Arbetet varje dag börjar med ett kort möte (ca 10 min) kallat *Daily scrum* eller *Standup meeting* där alla utvecklare en i taget kan ställa frågor eller uppdatera statusen på sitt arbete och om det finns något nytt problem som dykt upp hanteras det här.

När sprinten är slut har utvecklare, *SM* och *PO* ett möte med en demo och utvärdering (*retrospective*) av arbetet i sprinten. En unik sak med Scrum är att här utvärderas även hur många *items* utvecklarna hann med under sprinten. Finns det *items* kvar betyder det att gruppen tagit på sig för mycket arbete för sprinten och mängden arbete utvecklarna kan ta på sig justeras ner till nästa sprint. Detta kallas i Scrum för *Velocity* men mer om det senare.

![Scrum](img/scrum.png)

### Definition of Done (DoD)
För att kunna veta när något räknas som färdigt (och för att kunna göra en tidsuppskattnin) måste alla inblandade komma överens om vad som räknas som färdigt. Detta gäller normalt för alla förändringar i mjukvaran.

Exakta kriterierna skiljer sig nog alltid mellan olika produkter och företag. Det viktigaste är att alla förstår vad de innebär.

Om man tex arbetat på en sprint item och säger att den är klar kanske klar kan betyda att alla tester ska vara körda och fungera eller att förändringen måste godkännas av en kollega (sk. peer review / code review).

![DoD](img/geek-poke_scrum-wall-table.jpg)

### Velocity (tidsuppskattning)
I nästan alla projekt behövs någon form av tidsupskattning. I Scrum-språk översätter vi det till mängden *backlog items* teamet klarar att göra färdigt under en *sprint*. 

Inför varje sprint samlas *PO* och *scrum teamet* i ett *sprint planning meeting* där de väljer ut och estimerar rätt mängd *items* från *product backlog*. *PO* ansvarar för att prioritera och *teamet* för att ta på sig lagom mycket arbete.

#### Story point

För att få reda på hur stor en *item* är används ofta *story points* istället för timmar, dagar eller veckor. Det är ett relativt mått där fokus ligger mer i att förstå komplexiteten för en issue än att sätta ett exakt datum den är färdig. Det finns många saker som måste göras på ett arbete förutom just att producera kod (svara på mail, möten, teambuilding, etc.) så exakta datum är väldigt svåra att hålla.

*Planning poker* är en metod för att gissa storlek på de items som ska göras. En item i taget läggs fram, varje medlem i teamet får sedan gissa hur stor denna uppgiften än. För planning poker använder man en kortlek med olika poäng som t.ex:

**0** = redan färdig
**1/2, 1, 2, 3, 5, 8, 13** = vanliga poäng
**20, 40, 100** = någonstans på skalan blir en item för stor för att estimetas (t.ex. vid 20) då betyder poänget att den måste brytas ner i flera items
**☕️** = jag är trött - ge mig kaffe!
**?** = ingen aning 



![Planning poker](img/planning-poker.jpg)



Olika team använder olika skalor som t.ex. t-shirt-storlek (XS-XL).

Förutom ett sätt att estimera är dessutom planning poker ett team-building-event som förtydligar processen och svårigheten i att sätta rätt poäng på en uppgift.

#### Velocity

Efter varje sprint räknar man ihop hur många *items* som uppfyller *DoD* (dvs blev 100%) under sprinten. Summan av poängen är teamets *velocity* för nästa sprint. Itterativt justerar man teamets velocity efter varje sprint. Vill man kan man sedan göra medelvärde på velocity över tid i ett *velocity chart*.

Sätter teamet poäng på alla backlog items kan man isåfall räkna ut från velocity hur många sprintar som är kvar i en *burn down chart*. Behövs det kan även en projektledare utifrån de göra en grov beräkning på när arbetet kan vara färdigt.

Idén är att man istället för att gissa frammåt använder sig av riktig erfarenhet från tidigare sprintar för att göra en uppskattning.

## Code review / kodgranskning 

Kodgranskning är inte något obligatoriskt moment i Scrum eller någan annan Agile-metod. Det är snarare ett vanligt verktyg för att hitta fel.

De finns många olika sätt att granska kod men förslagsvis måste alla kodändringar granskas av någon som inte jobbat med koden när varje *sprint item* flyttas från *doing* till *done*. 

För att förtydliga arbetet föreslår vi att ni lägger till en kolumn på er *kanban-board* som ni döper till *review* eller *testing*. När en *item* är kodad hamnar den först i den nya kolumnen för att sedan granskas av en kollega innan den blir färdig.

Kodgranskning ska vara något enkelt och kan fungera så här:

* Den som skrivit koden visar ändringarna inkl. commit messages osv för en kollega som sitter bredvid.
* Uppgiften för kollegan är då att ställa frågor så fort något är oklart eller verkar märkligt.
* I bästa fall hittar kollegan (eller den som skrivit koden) fel i koden som antingen lagas direkt eller om det är ett större fel flyttas ditt *item* tillbaka från *testing* till *doing*.

Uppgiften är att hitta fel. Ju tidigare ett fel hittas desto enklare / billigare är det att laga.

Ni får eventuellt en enkel struktur för DoD på köpet? Dessutom får fler chansen att se all kod.

# Uppgifter 1 - Agila metoder

Förklara följande med dina egna ord. Skriv ner det i ett dokument. Nästa gång vi ses går vi igenom dem uppifrån och ner. Varje grupp kommer vara delaktig i diskussionen. Träna på att hitta kärnan i era argument - dvs. försök hålla det kort och exakt.

* Vad är en *Sprint*?
* Förklara de olika rollerna i Scrum: *Product owner*, *Scrum master* och *Scrum team*
* Vad är en *Product backlog item* och till vad / varför änvänds de?
* Vad är en *Product backlog* och vad är en *Sprint backlog*?
* Vad menas med *Minimum Viable Product* (eller *Minimum Viable Feature*)?
* Vad menas med *Definition of Done*?
* Förklara med egna ord vad som menas med att arbeta *agilt*. Reflektera och diskutera kring varför jag säger att det är en kultur snarare än metod att arbeta (eller vara) agilt?
* Diskutera för och nackledar med Scrum jämfört med Kanban. För ert team men också från eventuella tidigare erfarenheter av arbete eller hur ni tänker er att arbetet på ett företag med minst ett scrum team kan gå till.
* Beskriv, efter det ni lärt er om agila metoder, hur ni skulle vilja lägga upp arbetet för ert nästa projekt.
* Har ni några tankar om vattenfallsmetoden?

# Uppgifter 2 - Agila metoder

Återgå och utveckla era svar i uppgifter 1 när ni gör uppgifter 2. Diskutera och reflektera.

* Se en kort repetition: https://www.youtube.com/watch?v=1iccpf2eN1Q 
* Varför behövs både en *Product Backlog* och *Sprint Backlog*?
* Ibland kan man höra någon säga: "produktägaren lägger sig inte i under sprinten". De är inte nödvändigtvis 100% sant men ambitionen är sann. Varför tror ni det är så upplägget är?
* När kan en feature räknas som färdig (DoD)? Fundera ut några konkreta exempel.
* Skulle ni helst vilja arbeta mer som Scrum el. Kanban i nästa projekt? Motivera.
* Om vi är överens om att vara agil handlar om att ha en flexibel arbetsprocess - vad betyder det i verkligheten? Hur påverkar det era projekt? Hur påverkar de ert tillvägagångssätt? Se: https://www.youtube.com/watch?v=J9UjD_cKpnc Han säger typ: *“Change our mindset from: A leads to be B leads to C leads to Done* to *A-B-C-learn-repeat."* Vad säger han egentligen i videon? Diskutera.
* Hur skulle ert arbete se ut om vi skulle tvinga er att arbeta strikt enl. Vattenfallsmodellen i nästa projekt? Hur skulle arbetsdagarna, från start till slut, se ut? Vad tror ni skulle vara lättare / svårare i en sån modell? Förklara, reflektera och motivera.
* Hur kan ni använda *code review* i era projekt?
* Andra funderingar om Agile? Vilka nya kunskaper om agile har ni fått nu?

# Uppgifter 3 - Velocity
 * 
