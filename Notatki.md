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

### Założenie sieci semantycznej 

Główne założenie to aby maszyny i algorytmy potrafiły korzystać z informacji udstępnianych w internecie. 

> Umożliwenie maszynom zrozumienie zawartości dokumentów (pod względem semantyki czyli związków zachodzących między wyrażeniem języka a przedmiotami do których się odnoszą), a nie mowy i pisma ludzkiego.

Podstawą do posługiwania się dokumentami są **metadane**.

### Zasób

* Zasób 

    Jest to treść i struktura treśni. Z takimi zasobami są związane pewne metody korzystania z nich.
* Opis zasobu

    Niezależny od treści, wyjaśnia do czego służy treść dokumentu.

* Do opisu zasobów używamy:
    * RDF jest złożony ze stwierdzeń
    * XML
    * Zasób jest identyfikowany przez URI

### Trójki 

Stwierdzenia składają się z trójek:
* Podmiot - obiekt który opisujemy
* Orzeczenie - relacja, zależność
* Dopełnienie - własność obiektu

### Założenia RDF

* Prosty i przejrzysty model danych
* Interpretacja trójek w sposób formalnych na poziomie znaczenia 
* Rozszerzanie opisów o słowniki
* Składnia XML-owa
* Każdy może formułowac stwierdzenia na temat dowolnych zasobów

### Prosty model danych

Trójki tworzą grafową bazę wiedz poprzez abstrakcyjną składnię. Semantyka jest zdefiniowana w sposób formalny tak że wnioskowanie ma podstawy logiczne.

### Open world assumption

Każdy może tworzyć stwierdzenia o wszystkim, brak kontroli nad tym procederem. Nie możemy założyć że istnieje spójna i zupełna baza wiedzy.

### Struktura RDF

* Grafowy model danych

    Baza wiedzy to kolekcja trójek. Podmiot i orzeczenie to są wązły.
    * Podmiot - URI, lub blank node
    * Orzeczenie - URI
    * Dopełnienie - URI, lub blank node lub literał

* URI i słowniki

    URI identyfikuje zasoby nie tylko te umieszczone w intrnecie. Możemy też przy jego pomocy używac fragmentów zasoby poprzez `#`.

    Słowników używamy do dzielenia się fragmentami opisów. Aby tego dokonać grupuje się pojęcia w przestrzeń nazw.
    
* Typy danych i literały

    * Kontenery
    * Kolekcje

* Serializacja do XML

    Dokument ma korzeń RDF, do bydowania trujek służy `Description` z atrybutem `about` mówiącym jakiego tyczy obiektu. Następnie znajdują się predykaty.

* Blank node

    Umożliwia tworzyć relacje zachodzące między większą liczbą obiektów poprzez łączenie "binarnych" trójek używając pustego pomocniczego węzła.

* Reifikacja

    Opis zasobu który nie odnosi się do innego zasobu a do całej trójki.

* Wnioskowanie

    Z treści jednej trójki jesteśmy w stanie wywnioskować inną trójkę. Mechanizm ten umożliwia tworzene silników wnioskowania w sieci semantycznej i możemy dowieść prawdziwości takiego wniosku.

### RDF Schema

Używamy go do budowy struktur, do opisu własności i cech. Pozwala on na powiązanie pojęć w struktury, najczęściej pozwala na budowanie własnych typów danych a także precyzowanie zakresu pojęć.


## Wykład nr 4

---

### Problemy z metadanymi 

Metadane nie mówią nam jak zasoby powiązane są z obiektem. Aby pozbyć się tych problemów wprowadzno techniki tematycznej klasyfikacji. 

* Słowniki kontrolowane 

    Lista pojęć używanych do klasyfikajci obiektów z jakiejś dziedziny, w jawny sposób wylicza te pojęcia i można go skojarzyć poprzez słowa kluczowe. 

    Pojedynczy termin może określać wiele pojęć, może mieć wiele nazw i unika dwóznaczności poprzez zakazanie duplikacji.

* Taksonomie 

    Wywodzą się z botanki. Struktura jest hierarchiczna, klasy, obiekty.

* Tezaurusy

    Obiekty są grupowane w hierarchie i stwierdzenia mogą formułować stwierdzenia o innych stwierdzeniach.

* Ontologie

    Jest to model do opisu świata składający się z typów obiektów, własności i relacji zachądzących między nimi. Opierają się na otwartych słownikach i otwiartych zbiorach własności. 

    Jawna specyfikacja pewnej wspólnej konceptualizacji. Nie zakładamy dodatkowej wiedzy poza tej określonej jawnie, wiedza jest określona w sposób sformalizowany. Konceptuazlizacja jest dzielona między pewnymi osobami, dziedzinami.

    Ontologie wykorzysują logikę opisową przez co jest sformalizowanym elementem w logice pierwszego rzędu, a wniosowania będą zdefiniowane na poziomie logicznym. 

* Folksonomie

    Jest to specjalny przypadek ontologii, mówimy że folksonomia to ontlogia stworzona oddolnie przez jakąś społeczność. 

### Elementy ontlogii

* Słownik - definiuje pojęcia i ich znaczenia
* Klasyfikacja obiektów 
* Relacje i ich ograniczenia

### Cele ontloigii

Uchwycene wspólnego rozumienia i wykorzystania wiedzy z określonej dziedziny a także udostępnienia sformalizowanej metody operowania wiedzą poprzez maszyny.

### Języki wykorzystywane do budowy ontologii

* RDF Schema

    Prostota ale brak formalnej i logicznej semantyki co utrudniało budowę narzędzi do automatycznego wnioskowania.

* OWL (Web Ontology Language)

    Zdefiniowany na poziomie logicznym

### Wymagania dla języja ontologii

* Rozszerzanie obecnych standardnów
* Łatwy do zrozumienia i użycia
* Określony w sposób formalny
* Mający odpowiednią siłę wyrazu
* Automatyczne wsparcie dla wnioskowania

### Zastosowanie OWL

* Budowanie ontologii 
    * Definiowanie klas i dostarczanie informacji o nich 
    * Defniowanie własności i dostarczanie informacji o nich
* Definiowanie faktów w dziedzienie 
    * Tworzenie indywidułów (instancji)
* Wnioskowanie w sposób automatyczny


## Wykład nr 5

---


## Wykład nr 6

---

### Po co opisywć i walidować RDF

* Dla twórców 
    * Zrozumienie zawartości nad którą pracują
    * Upewnienie się że produkt ma odpowiednią strukturę
    * Wygenerowanie interfejsów 
    * 
* Dla użytkowników
    * Pozwala na zrozumienie kontekstu
    * Weryfikowanie struktury przed procesowaniem jej
    * Generowanie zapytań i optymalizacje

### Walidacja grafów RDF

* Zalety
    * Można zapisać w SPARQL wszystko
    * Wszechobecny
* Wady
    * Można zapisać w SPARQL wszystko
    * Wiele sposobów na zakodowanie ograniczeń

### Wnioskowanie

OWL nakierowany jest na sprawdzanie logiczne. Nie był nastawiony na sprawdzanie poprawności a na to co można jeszcze wywnioskować z naszej ontologii.

Wnioskowanie w OWL jest ograniczone więc trzeba go mieszać z dodatkowymi technologiami.

> Problemem jest wnioskowanie gdy mamy otwarty świat.

### SHACL (Shapes Constraint Language)

Sprawdza czy graf z danymi zgadza się z grafem kształtów mówiącym jak ma wyglądac baza wiedzy.

Wybieramy z nazego grafu grupę którą chcemy walidować i następnie sprawdzamy czy spełna ona reguły określone dla tej grupy. 

Każdy kształt składa się z:
* Targetów
    * Wybieramy klasę
    * Konkretne węzły
    * Obiekt z określonym property
    * Podmity z określonym property
* Ograniczeń
* Reguł

### SHEX 

* Ma abstrakcyjną składnię, później serializowaną do RDF
* Nastawienie aby shape wykonywane wielokrotnie
* Pokazuje które węzły przeszły walidację