# GiftFlow 

## Informacje o projekcie
* uczelnia i wydział: Politechnika Białostocka Wydział Informatyki
* kierunek: Informatyka i Ekonometria
* przedmiot: Inżynieria Oprogramowania
* rok i semestr: 2 rok (semestr IV)
* grupa: 1
* temat:
* ** System GiftFlow służy do pełnej automatyzacji i cyfryzacji łańcucha dostaw operacji wigilijnej.

Moduł Beneficjentów i Weryfikacji
Każdy Beneficjent (posiadający unikalny ID, adres i współrzędne GPS) może przesłać w danym roku jeden List. System przesyła dane z Listu do zewnętrznego modułu Grzecznościometr, który zwraca ocenę punktową. Na tej podstawie system automatycznie nadaje Listowi status: „Zatwierdzony” (dla dzieci grzecznych) lub „Odrzucony” (skutkujący wygenerowaniem zlecenia na dostawę węgla). Tylko zatwierdzone listy stają się podstawą do utworzenia Zlecenia Produkcyjnego.

Moduł Produkcji i Magazynu
Zlecenie Produkcyjne trafia do jednego z Warsztatów, gdzie przypisana jest do niego brygada Elfów. Aby rozpocząć pracę, system sprawdza dostępność i rezerwuje w Magazynie odpowiednie Surowce (określone przez typ i ilość). Produktem końcowym jest Prezent, który posiada przypisaną kategorię, wagę oraz wymiary. Każdy Prezent przed wysyłką musi przejść kontrolę jakości i otrzymać status „Gotowy”.

Moduł Logistyki i Transportu
Gotowe Prezenty są grupowane w Ładunki i przypisywane do Sani. Sanie mają zdefiniowane limity techniczne: maksymalną wagę ładunku oraz maksymalną objętość. System odpowiada za takie rozmieszczenie prezentów, aby zachować stabilność sani. Trasa przelotu jest generowana jako sekwencja punktów dostaw z przypisanym czasem dotarcia i strefą czasową. Podczas lotu system koryguje parametry trasy na podstawie danych z modułów GPS oraz Pogodynka.

Administracja i Raportowanie
Po zakończeniu dostaw (26 grudnia), system archiwizuje dane o zrealizowanych prezentach i trasach. Na żądanie administratora generowany jest Raport Wydajności, który zestawia czas pracy poszczególnych warsztatów oraz całkowite zużycie surowców z magazynu.

[KLIKNIJ TUTAJ, ABY OTWORZYĆ PEŁNE SPRAWOZDANIE (PDF)](./sprawozdanie/Sprawozdanie_Finalne.pdf)

## Struktura plików (Dodatek A)
* [**/sprawozdanie**](./sprawozdanie) - wersja PDF oraz [**wersja edytowalna**](./sprawozdanie/edytowalne).
* [**/diagramy**](./diagramy) - źródła diagramów (UML).
* [**/interfejs**](./interfejs) - makiety UI.

   
