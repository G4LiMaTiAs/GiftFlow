# GiftFlow 

## Informacje o projekcie
* uczelnia i wydział: Politechnika Białostocka Wydział Informatyki
* kierunek: Informatyka i Ekonometria
* przedmiot: Inżynieria Oprogramowania
* rok i semestr: 2 rok (semestr IV)
* grupa: 1
* temat:

1.1. Moduł Beneficjentów i Obsługi Korespondencji
System GiftFlow służy do kompleksowego zarządzania procesem obdarowywania dzieci. Głównym obiektem danych jest Beneficjent (dziecko), opisany przez: unikalny numer ID, imię, nazwisko, wiek oraz adres zamieszkania wraz ze współrzędnymi GPS.
Każdy Beneficjent może wygenerować w systemie dokładnie jeden List na dany rok kalendarzowy. List posiada swoją datę wpływu, unikalny numer oraz treść (listę życzeń).

Proces weryfikacji Listu przebiega następująco:

Elf-Listonosz wprowadza List do systemu.

System przesyła zapytanie do zewnętrznego modułu Grzecznościometr. Moduł ten analizuje zachowanie dziecka i zwraca Współczynnik Grzeczności (liczba całkowita od 0 do 100).

Logika decyzyjna: * Jeśli współczynnik wynosi 50 lub więcej, List otrzymuje status „Zatwierdzony”, co automatycznie generuje Zlecenie Produkcyjne na zabawki z listy życzeń.

Jeśli współczynnik wynosi poniżej 50, List otrzymuje status „Odrzucony”. W takim przypadku system automatycznie generuje zlecenie na Rózgę (standardowy przedmiot o stałych wymiarach i wadze), która zastępuje wszystkie inne prezenty.

1.2. Moduł Produkcji i Gospodarki Magazynowej
Zatwierdzone zlecenia trafiają do sekcji produkcyjnej. System zarządza strukturą Warsztatów (każdy posiada nazwę i specjalizację). W każdym Warsztacie pracuje Brygada Elfów.

Elf opisany jest przez: ID, imię, specjalizację oraz przypisanie do jednego konkretnego Warsztatu.

Aby zrealizować Zlecenie, system musi pobrać z Magazynu odpowiednie Surowce. Każdy Surowiec ma nazwę, typ (np. drewno, tkanina) oraz aktualnie dostępną ilość. System blokuje produkcję, jeśli stan magazynowy jest niewystarczający.

Produktem końcowym jest Prezent. Każdy Prezent (w tym Rózga) posiada: unikalny kod QR, wagę (w kg), wymiary (wysokość, szerokość, głębokość w cm) oraz status (aktualny etap: „W produkcji”, „Gotowy”, „Spakowany”).

Zanim Prezent opuści Warsztat, Elf-Inspektor musi przeprowadzić Kontrolę Jakości i oznaczyć go w systemie jako „Gotowy do wysyłki”.

1.3. Moduł Logistyki, Planowania i Transportu
Wszystkie gotowe Prezenty muszą zostać dostarczone w ciągu jednej nocy.

System grupuje Prezenty w Ładunki. Każdy Ładunek przypisany jest do konkretnej jednostki transportowej – Sani.

Sanie posiadają parametry techniczne: unikalny numer boczny, Maksymalną Ładowność (limit wagi) oraz Maksymalną Pojemność (limit objętości). System posiada wbudowany walidator: nie pozwoli na przypisanie Ładunku, który przekracza limity Sani.

Mikołaj (Główny Użytkownik) korzysta z modułu Nawigatora. System generuje dla niego Trasę, która składa się z chronologicznej listy Punktów Dostawy.

Każdy Punkt Dostawy jest powiązany z adresem Beneficjenta i zawiera informację o przewidywanej godzinie przybycia (ETA).

Podczas lotu system w czasie rzeczywistym koryguje Trasę, pobierając dane z systemów zewnętrznych: GPS (aktualna prędkość i pozycja sań) oraz Pogodynka (ostrzeżenia o śnieżycach i kierunku wiatru).

1.4. Moduł Administracji i Raportowania
Po dostarczeniu każdego prezentu, Mikołaj (używając mobilnego terminala) zmienia status Prezentu na „Dostarczony”.

W dniu 26 grudnia system wykonuje proces Archiwizacji – wszystkie dane o Listach, Produkcjach i Trasach z danego roku trafiają do bazy historycznej.

Administrator Systemu może wygenerować Raport Końcowy, który automatycznie podlicza:

Łączną liczbę rozdanych Prezentów oraz Rózg.

Wydajność każdego Warsztatu (ile zleceń ukończono).

Zużycie Surowców z Magazynu (raport braków do uzupełnienia na przyszły rok).

[KLIKNIJ TUTAJ, ABY OTWORZYĆ PEŁNE SPRAWOZDANIE (PDF)](./sprawozdanie/Sprawozdanie_Finalne.pdf)

## Struktura plików (Dodatek A)
* [**/sprawozdanie**](./sprawozdanie) - wersja PDF oraz [**wersja edytowalna**](./sprawozdanie/edytowalne).
* [**/diagramy**](./diagramy) - źródła diagramów (UML).
* [**/interfejs**](./interfejs) - makiety UI.

   
