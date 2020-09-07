# Dockerguide Anton & Benjamin

Installera Docker *https://www.docker.com/get-started* 

* Högerklicka på din solution, sedan Add->Docker support

  En Dockerfile kommer nu att genereras i ditt projekt.

![img](https://media.discordapp.net/attachments/280760711620067330/752458331884355640/unknown.png?width=400&height=255)

* Första raden väljer vi basen som är ASP.NET 3.1 core (rad 3)

* Följande kod öppnar portar för din container.

* Väljer vilket directory (rad 4).

* Port 80 exponeras för HTTP (rad 5).

* Port 443 exponeras för HTTPS (rad 6).

![img](https://cdn.discordapp.com/attachments/280760711620067330/752506582385819708/image-20200907112353268.png)

## Ändra vilka portar din container ska lyssna efter

* Öppna launchSettings.json

  ![img](https://cdn.discordapp.com/attachments/280760711620067330/752506582385819708/image-20200907112353268.png)

* Ändra portarna för localhost till 443 och 80 (rad 24).

![img](https://cdn.discordapp.com/attachments/280760711620067330/752506587851128853/image-20200907114359729.png)



## Bygg din image & kör den via Docker

Öppna din CLI och navigera till ditt projekt

Kör följande kommandon:

* docker build --t [*välj ett namn på din image]* .

  exempel:

![img](https://cdn.discordapp.com/attachments/280760711620067330/752506589642096640/image-20200907125035428.png)

* docker run -d -p 8080:80 --name *[välj ett namn på din container]* *[namn på din image]*

  exempel: 

  ![img](https://cdn.discordapp.com/attachments/280760711620067330/752506591273811978/image-20200907125355994.png)

  -d representerar den porten som din container kommer lyssna på lokalt, och -p den port som kommer lyssna efter externt.

  --name är det namn som din container kommer tillges. 

  Efter att kommandot har körts så borde en nyckel skrivas ut i din CLI som svar, samt att du ska nu kunna se din container i Docker Desktop. 

  exempel: 

  ![img](https://cdn.discordapp.com/attachments/280760711620067330/752506591902695454/image-20200907125654256.png)

## Kör din image med  Docker compose

Skapa en fil i din projektmapp med namnet docker-compose.yml

I bash kan du navigera till projektmappen och skrifa *touch docker-compose.yml*

![img](https://cdn.discordapp.com/attachments/280760711620067330/752508920022433833/image-20200907135011276.png)

Bilden visar vårt projekt SimpleWebHalloWorld som en web-service på portarna 8080:80. 

