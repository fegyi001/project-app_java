# project-app

A megoldandó feladat egy **Java API backend létrehozása Dockerizált környezetben** meglévő adatbázissal, frontend alkalmazással. 
Az adatbázis egy PostgreSQL, egyetlen táblával: `projects`. A frontend alkalmazás egy Angular alapú weboldal. 
Előbbi helye a `database`, utóbbi helye a `frontend` mappában található.
Mindkettő Docker környezetben van, `docker compose up` paranccsal indíthatóak. A frontend a [http://localhost](http://localhost) url-en nyitható meg (80-as port).

Az `api` mappa néhány induló fájl kivételével üres. **Ebbe a mappába szeretnénk kérni a Java API backend alkalmazást, illetve a Docker-specifikus fájlokba az oda vonatkozó részeket**.
A cél, hogy egyetlen `docker compose up` paranccsal a teljes projekt elinduljon (adatbázis, API és frontend). A frontend a `http://localhost:8080` url-en keresztül fogja meghívni a backend-et, vagyis ez legyen az API baseUrl-je.

Az API szerver segítségével **projektek**-et kell tudni létrehozni, listázni, módosítani és törölni, vagyis egy CRUD alkalmazás létrehozása a feladat.
A mellékelt `api/openapi.yaml` fájl tartalmazza a lehetséges végpontokat a projektek kezeléséhez. Az adatbázis induláskor egyetlen projektet tartalmaz.

Az oldal elvárt működését a következő screen capture mutatja be: [link megtekintése](https://e1.pcloud.link/publink/show?code=XZitDzZ3B772xudjuFuAtFT8URorLxoCrIy)

A megoldást egy **GitHub repository**-ba várjuk.

Ha bármilyen kérdésed van, vagy valami nem akar úgy működni ahogy kéne, kérlek jelezd!

Előre is köszönjük a munkádat!
