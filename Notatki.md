# Wykład semantyczny internet

## Wykład nr 1

---

### Historia 

Semantyczny internet był ideą stworzenia nowej generacji internetu. Nie przyjął się w globalnej skali lecz w specjalistycznych zastosowaniach odniósł duży sukces i wciąż odnosi. Projekt ten czerpie korzenie z wczesnych badań nad AI. 

### Typowe użycie internetu 

* Szukanie i używanie informacji
* Szkukanie i komunikacja z innymi
* Przeglądanie katalogów, zamawianie 
* Informacja jest prezentowana wizualnie bez oryginalnej struktury którą możemy spotkać w bazie danych, ma to ułatwić użytkowanie. 
* Mimo dużych zasoby informacji ciężko jest nam odnaleźć porządane fragmenty

### Wyszukiwanie po słowie kluczowym

Wyszukiwarki budują swoją bazę stron i informacji do której chcemy się dostać. Ale podstawowy interfejs dla użytkownika jest niezmienny. Wpisujemy słowa kluczowe które silniki przetwarzają. 

Wady:
* Podanie ogólnego słowa klucowego zwróci nam wiele wyników ale o niskiej precyzji
* Bardzo precyzyjne wyszukają dokładne informacje ale jest ich mało
* Sposób użytego słownictwa wpływa na wyniki
* Człowiek dalej jest potrzebny do interpretowania i zbierania wyników
* Wyniki nie są wygodne dla innych narzędzi
* Nie jesteśmy w stanie wykonać złożonych zapytań które będą integrować wiedzę z różnych źródeł

### Połączenia informacji

Mamy na stronach wiele połączeń i odniesień do innych materiałów ale nie wiemy jaki jest sens tego połączeni i czy wartości są wartościowe. 

### Podejście semantycznego internetu 

* Zmiana sposobu reprezentowania treści w internecie tak aby można było ją przetwarzać maszynowo
* Używanie inteligentnych technik do uzyskiwania informacji
* Rozwinięcie istniejącego internetu a nie jego konkurencja
* **Ontologia** schemat reprezentowania wiedzy na temat danej dziedziny i komunkację między osobami
* Fragmenty dokumentu odnoszą się do fragmentów ontologi (*adnotacje*)

### Technologie sieci semantycznej

* Reprezentowanie informacji wraz z ich strukturą bez warstwy wizualnej. Podejście to jest zrozumiałe dla maszyn
* **RDF** - uniwersalny standard do reprezentowania, przetwarzania i przechowywania metadanych 
    * Rozszerzenie języka XML, danym w XML towarzyszy opis metadanych w języku RDF.
    * podmiot -> orzeczenie -> dopełnienie
* **Ontologia** to jawna specyfikacja jakiegoś zbioru pojęć
    * Pojęcia
    * Relacje między pojęciami
    * Własności
    * Ograniczenia
    * Ma postac grafu

    Ontologie dostarczają współpracy rozwiązań przy automatycznym przetwarzaniu danych z zachowaniem ich znaczenia. Są one elementem pośredniczącym w integracji danych z różnych źródeł.
* RDF Schema jest językiem do budowania ontologi

### Podejście warstwowe

* URI do identyfikacji zasobów
* XML do strukturalizowania danych
* RDF do opisu danych 
* RDFS, OWL do porządkowania pojęć w hierarchię
* Języki do zapytań
* Języki do wnioskowania

### Wpływ semantycznego internetu 

Zarządzaie informacją na poziomie organizacji, wewnętrzna wiedza jest dobrem intelektualnym. Wiedza pogrupowana na podstawie znaczenia, definiowanie dostępu do poszczególnych fragmentów dokumentu. 

Agenci wykonujący podstawowe czynności zamiast użytkownika, jak zamawianie zakupów, porówywanie cen, przeszukiwanie najlepszych ofert. 

> Technologie są wdrożone albo dopiero są wdrażane lub odkrywane.

## Wykład nr 2

---

### Formaty querowania danych 

* SELECT 
    <br>Zwraca całość bądź fragment zmiennych określonych przez zapytanie
* CONSTRUCT
    <br>Zwraca graf złożony z trójek
* ASK
    <br>Zwraca informację czy udało się znaleźć wzorzec
* DESCRIBE 
    <br>Opisuje informacje o danym węźle (fragment grafu)
* UPDATE
    <br>Zarządzanie grafem na podstawie zapytań

## Wykład nr 3

---

cdn.