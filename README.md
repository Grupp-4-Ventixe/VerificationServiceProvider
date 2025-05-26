# VerificationServiceProvider

Detta är ett C#-projekt som tillhandahåller en API-tjänst för verifiering, utvecklat av Grupp 4 Ventixe.

## Innehåll

- `VerificationService.sln` – Lösningsfil för hela projektet (.NET).
- `VerificationService.Api/` – Huvudprojektet med källkod för API:t.
  - `Controllers/` – Innehåller API-kontrollers (logik för inkommande HTTP-förfrågningar).
  - `Models/` – Datamodeller som används i API:t.
  - `Services/` – Tjänster och affärslogik.
  - `Properties/` – Konfigurationsfiler för projektet.
  - `Program.cs` – Applikationens startpunkt.
  - `WebApi.csproj` – Projektfil för API-projektet.

## Funktionalitet

Projektet innehåller en verifieringstjänst som skickar och validerar verifieringskoder via e-post. Funktionaliteten är byggd kring en controller (`VerificationController`) och en tjänst (`VerificationService`):

- **VerificationService**  
  Tjänsten använder Azure Communication Services för att skicka verifieringskoder till användarens e-postadress. Koden lagras temporärt i minnet (med IMemoryCache) och är giltig i 5 minuter.  
  - Skickar verifieringskoder via e-post
  - Sparar och validerar koder med cachning
  - Returnerar tydliga svar om koden är ogiltig eller felaktig

- **VerificationController**  
  API-controller som exponerar endpoints för att:
  - Skicka en verifieringskod (`POST /api/verification/send`)
  - Verifiera en kod (`POST /api/verification/verify`)

### Exempel på flöde

1. Klienten skickar en POST-begäran till `/api/verification/send` med användarens e-postadress.
2. Tjänsten genererar och skickar en kod via e-post.
3. Användaren anger koden och skickar en POST-begäran till `/api/verification/verify`.
4. Tjänsten validerar koden och återkopplar om verifieringen lyckades.

## Teknisk översikt

- **Azure Communication Services** används för e-postutskick.
- **IMemoryCache** används för temporär lagring av verifieringskoder.
- **.NET 6+** och ASP.NET Core används för API och tjänster.
- All logik är tydligt separerad mellan controllers (API), services (affärslogik) och models (dataobjekt).

## Strukturell översikt

- **Controllers** – Här finns API-endpoints och logik för att hantera inkommande HTTP-anrop.
- **Models** – Definierar datatyper och objekt som används i tjänsten.
- **Services** – Affärslogik och funktionalitet utanför controllers.
- **Program.cs** – Här startas och konfigureras applikationen (t.ex. host, DI, routing).

## Beroenden

- .NET 6.0+
- Eventuella externa bibliotek definieras i `WebApi.csproj`.

## Publicering

VerificationServiceProvider är publicerad på Azure:

🔗 https://verificatioservice-hcecd5avgddveufy.swedencentral-01.azurewebsites.net

---

## Författare

Utvecklad av Elias Grafström
