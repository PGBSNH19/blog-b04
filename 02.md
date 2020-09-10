Lektion 2 Blogg

En övergripande beskrivningen av hur ni fick en Virtuell maskin att köra med Azure CLI:

Vi valde att inte fokusera på Azure CLI utan lade vårt fokus på Pulumi istället, efter vi var klara med att sätta upp en fungerande VM via portalen. Vi märkte att det var viktigt när man installerar de olika paketen på en VM att man gör saker och ting i rätt ordning, då vi stötte problem med att terminalen inte hittade paketen vi behövde för att hosta en webserver.  Vi märkte också att det var viktigt att man befinner sig i rätt directory innan man kör igång servern, då vi tampades med problemet att servern kördes utan css. Vi stötte även på ett problem med att vi inte kunde köra "pulumi up", eftersom att vi inte hade ändrat rätt inställningar. Vilket utan hjälp hade varit väldigt svårt att hitta. Slutligen hann vi inte dra ned repot från git och öppna portar, men vi hoppas att vi kan göra det under kommande dagar. 

Cache sparar information om headern, om ingenting på servern har förändrats så behöver klienten inte ladda ner sidan igen. 

Stateless protocol: klienten får ett svar beroende på vilket state (http, udp, dns). 

Http blir mer likt stateful med hjälp av cookies och sessions, som skickar med information till servern om klienten (session, session id).  Stateful protocol: klienten förväntar sig ett svar från servern. (FTP, telnet). 

Monolith: server osv på samma ställe. 

Sessions bygger på cookies. * Cookies nödvändigt när det är flera servrar,  så att användaren inte behöver logga in på flera ställen. (Oanvändarvänligt) * Cookies kan hålla information som t.ex. sessionid eller användarnamn och lösenord. 

SaaS = Email, DMS, ECM, CRM, ERP, SCM, dyPas 

PaaS = OS; RDBM, RAD, BPMS, Schedulers

 IaaS = Servers, VM, Storage, Communications, Security 



Fördelar med VM: * Flera på samma server. * Isolerad ifrån de andra maskinerna. 

Nackdelar: * Direkt tillgång till hårdvara. * Stor förbrukning av RAM - Allokera ram som inte kan användas till annat. * Tar upp mycket disk - ett VM innehåller ett helt OS. * Ineffektiv på att skriva och läsa till disk. - beror på att ett VM hanteras som en enda stor fil.



## Pulumi

Styrkor 

- Att man kan använda sig a det språk man kan bäst.
- Man får ju väldigt mycket kontroll som utvecklare med IaC generellt.
- Det känns som att man har allt lite mer samlat när man kör IaC.

Nackdelar

- Det är ganska hög tröskel för att komma igång och få en fungerande VM.
- Svårt att hitta relevant information.

Möjligheter

- Ger utvecklare möjligheten att automatisera någonting som skulle ta längre tid att skapa via t.ex Azure-portalen

Hot 

- Användarnamn och lösenord står förtillfället med i .yaml-filerna och eftersom att vi inte kan nog skulle det kunna vara en sårbarhet.





Kolla vilka resurser som skåpas i Azure när man gör en virtuell maskin, vad är skillnad på dom olika typer:

- CPU - Hur många kärnor, dvs. hur snabbt man kan hantera information
- RAM - Definierar hur mycket han kan läsa och skriva
- HHD/SSD - lagringsutrymme för data
- Offentlig och privat IP - för att kunna komma åt vår VM
- SSH-key - för att kunna ansluta säkert med CLI

