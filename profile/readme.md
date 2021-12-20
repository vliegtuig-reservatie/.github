# JETLIST
Vliegtuig reservatie applicatie

## Project vereisten
- User kan:
  - Vluchten boeken en zetels reserveren
  - Beoordelingen plaatsen
- Admin kan:
  - Rapport opvragen van beoordelingen
- Als een maximum type aantal zetels bezet is wordt de vluchtleiding verwittigd voor het mogelijks inzetten van een tweede vlucht
- De vluchtreservatieprijs is afhankelijk van het moment, het type (eerste klasse) en bestemming (afstand)

## Technische vereisten
#### Front-end
- Framework: Vue
- Styling: Tailwind
- Bundler: Vite

#### Back-end
- Framework: Node Express
- Auth: Firebase
- Database: MariaDB
- API: GraphQL

## Test users
- Front-end (Admin)
  - User: docent@howest.be
  - Password: P@ssw0rd
- Front-end (User)
  - User: test@user.com
  - Password: verysafepassword123
- Back-end
  - User: admin
  - Password: P@ssw0rd

## Werkverdeling
- Aaron
  - Backend en frontend
- Marco
  - Backend en frontend

## Milestones
### 08/11 
- Front-end
  - [X] Setup
  - [X] Login, register pagina
  - [X] Header
  - [X] Firebase authenticatie
- Back-end
  - [X] Setup
  - [X] Firebase authenticatie
  - [X] Mongodb opgezet
### 15/11 
- Front-end
  - [X] Dashboard design
  - [X] Dashboard functionality, data, ...
- Back-end
  - [X] Entities (Flight, Airport, Plane, Seat, User)
  - [X] Basic resolvers
### 22/11 
- Back-end
  - [X] More resolvers
  - [X] Moved to mariadb
  - [X] Making relations
### 29/11 
- Front-end
  - [X] Booking page design & functionality
  - [X] Account dropdown + pages
- Back-end
  - [X] Seeding
  - [X] Some more resolvers & relations

### 06/12 
- Front-end
  - [X] Seat selection design & functionality
  - [X] My bookings page
  - [X] Responsiveness
- Back-end
  - [X] More seeder data
  - [X] Even more resolvers & relations
### 13/12 
- Front-end
  - [X] Dashboard filter inputs
  - [X] Reviews pages & functionality
  - [X] Fine tuning
- Back-end
  - [X] Authentication
  - [X] Custom claims for roles
### 20/12 
- Front-end
  - [X] Admin pages
  - [X] Account settings
  - [X] Reviews summary for admin
  - [X] Added First Class, Business and Economy classes to seat selection
  - [X] Added problems page for admin
  - [X] Some more fine tuning, extras
  - [X] Dockerizing
  - [X] Kubernetes deployment
  - [X] Tried to get unit/integration tests to work, guess what it didn't work :(
- Back-end
  - [X] Dockerizing
  - [X] Kubernetes deployment
### 21/12 
- [X] Finish project
- [X] Prepare for presentation

## Checklists
- Back-end
  - [X] Is een NodeJS Express API die via Docker gehost wordt op Kubernetes
  - Gegevens worden persistent gestockeerd in de meest passende datastructuur. Maak
een goed onderbouwde keuze.
    - [X] SQL
    - [ ] NoSQL
  - [X] Backend communiceert naar frontend in realtime en vice-versa met de gepaste
protocollen.
  - [X] Firebase of dergelijke
  - PKCE Flow gebruiken
  - [X] Minimaal 2 rollen: gebruiker en administrator
  - [X] Admin is voorzien: “docent@howest.be” met paswoord “P@ssw0rd”
  - [X] CORS is enabled
  - [ ] Extra beveiligingen tegen Cross Site Forgery, Cross Site Scripting
  - [X] De API documenteert zichzelf op basis van een self-documenting library. (bv.: Swagger
of GraphiQL)
  - [ ] Ook statuscodes bij foutcondities worden gedocumenteerd.
  - [X] Kies een goede manier om je project te structureren
  - [X] Via een seeder wordt de database bij opstarten van de applicatie automatisch
aangemaakt.
  - [X] Gebruik logische microservices in Docker / Kubernetes.
  - [X] Eén service maakt gebruik van gRPC of GraphQL.
  - [ ] Het crashen van de applicatie wordt verhinderd door het gebruik van een try/catch
structuur waarbij de oorzaken bijgehouden worden via een logger.
  - [ ] Foutboodschappen worden altijd via een JSON aan de front bezorgd.
  - [X] Source controle gebeurt via GitHub door regelmatig te pushen. 
  - [X] De applicatie draait volledig in Docker.
  - [ ] Container wordt automatisch via GitHub Actions gebuild en gepushed naar een Image
Registry (DockerHub / Harbor) (met versiebeheer van de Container tags)
  - [ ] Image beschikbaar op DockerHub / Harbor
  - Kies een gepaste Kubernetes deployment methodiek (Canary, blue-green, rolling …)
  - Extra uitbreidingsmogelijkheden, niet gezien in de les. 
    - [ ] Versiebeheer
    - [ ] Response Caching en Ratelimiting
    - [ ] Memory Caching
    - [ ] Gebruik Ocelot als API gateway
    - [ ] Unittesten / Integratie testen van de API
    - [ ] Voorzie een interactie met hardware
    - [ ] Integratie met een AI service in cloud

- Front-end
  - Met een JS-framework gemaakt, met TypeScript.
    - [X] Vue.js
    - [ ] Angular
    - [ ] Svelte
    - [ ] React
  - [ ] Minstens één unit test
   - Dit geprobeerd met jest en cypress maar heel veel problemen mee, bij installatie alleen al.
  - [ ] Minstens één integratie test.
  - [X] Je werkt met SCSS met een solide achterliggende structuur of tailwindCSS.
Je voorziet ghosts, skeletons / loading states.
  - [X] Je voorziet input-validatie en error meldingen.
  - [ ] De web app kan fullscreen launchen en heeft een correcte PWA-setup
   - Dit ook geprobeerd, service worker wil niks doen.
  - [ ] De applicatie meertalig maken kan zeker een meerwaarde zijn. Indien je dit op een
goede manier uitwerkt, kan dit zeker extra punten opleveren.
  - [ ] Het is een meerwaarde om fouten te loggen. Iets in de aard van https://sentry.io/.
  - [ ] Gebruik van https://codeclimate.com voor code testing en reviews is een
meerwaarde.
  - [X] De applicatie draait volledig in Docker.
Werken met gitflow is aangeraden.
  - [X] Gebruik vite voor een betere JS-files delivery.
  - Werk iets kleins uit, dat niet uitgewerkt werd in de cursus, waar je via zelfstudie
extra punten mee wil verdienen.
    - [ ] Gebruik van Svelte, Vue of Angular.
    - [ ] Testing in deployment pipeline (speedtest, functional).
    - [ ] Transities tussen schermen
     - Geprobeerd, transities deden rare dingen.
    - [ ] Gebruik van Next.js, Gatsby of Nuxt indien relevant voor SEO
    - [ ] Uitwerking van onderdeel met Web Assembly.
    - [ ] Web worker die zware taken van de main thread halen
    - [ ] Shared workers voor syncrone werking over meerdere tabs (indien
  relevant).
  
## Grootse moeilijkheid
- Kubernetes deployment
  - [X] Opgelost
- Unit & integration test
- PWA
- Vue transitions

