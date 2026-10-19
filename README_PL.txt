# Dojazd Live · Gdańsk (PWA starter)

## Co zawiera
- Responsywny interfejs dla iPhone'a i komputera.
- Mapa OpenStreetMap.
- Warstwa ruchu TomTom Traffic Flow po wprowadzeniu klucza.
- Wyznaczanie trasy z uwzględnieniem ruchu przez TomTom Routing API.
- Lista porównawcza celów i odświeżanie co 5 minut, gdy karta jest aktywna.
- Manifest i service worker dla instalacji PWA.

## Ważne ograniczenia
- Bez klucza API aplikacja pokazuje tylko mapę bazową. Nie pokazuje fikcyjnych danych live.
- Heatmapa w tej wersji oznacza kolorową warstwę prędkości na drogach, nie izochronę czasu dojazdu dla każdego punktu terenu.
- Współrzędne Nowego Portu są punktem orientacyjnym w publicznej części dzielnicy; zmień START w index.html, jeśli chcesz użyć dokładniejszego punktu.
- Czasy tras są estymacjami dostawcy w chwili zapytania, nie gwarancją.
- iOS może wstrzymywać odświeżanie w tle; aplikacja odświeża dane co 5 minut, gdy karta jest widoczna.
- Klucz wpisany w przeglądarce nie jest tajny. Ogranicz go do domeny i odpowiednich usług w panelu TomTom. Do publicznego wdrożenia zalecany backend z kluczem po stronie serwera i limitami zapytań.
- Trzeba sprawdzić aktualne warunki licencji, pokrycie, limity i cennik dostawcy przed publikacją.

## Jak uruchomić
1. Rozpakuj ZIP.
2. Opublikuj folder na hostingu HTTPS obsługującym pliki statyczne (np. własny hosting).
3. Otwórz adres w Safari na iPhonie i wybierz Udostępnij → Dodaj do ekranu początkowego.
4. W aplikacji wybierz „API”, wklej klucz TomTom i zapisz.

Dokumentacja:
- TomTom Traffic API: https://docs.tomtom.com/traffic-api/documentation/tomtom-orbis-maps/v2/product-information/introduction
- TomTom Routing API: https://developer.tomtom.com/routing-api/documentation/routing/calculate-route
- OpenStreetMap attribution: https://www.openstreetmap.org/copyright
