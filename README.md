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

## Kom igång

1. **Krav**  
   - .NET 6.0 eller senare  
   - Visual Studio 2022 eller senare (eller motsvarande IDE)

2. **Klona repot**
   ```bash
   git clone https://github.com/Grupp-4-Ventixe/VerificationServiceProvider.git
   cd VerificationServiceProvider
   ```

3. **Bygg och kör**
   - Öppna `VerificationService.sln` i Visual Studio och kör projektet,  
     **eller**  
   - Kör via terminalen:
     ```bash
     cd VerificationService.Api
     dotnet run
     ```

4. **API:**  
   Applikationen startas på `http://localhost:5000` (eller enligt konfiguration).  
   Utforska tillgängliga endpoints genom att titta i `Controllers`-mappen.

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
