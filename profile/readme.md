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
