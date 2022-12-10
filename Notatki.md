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

### Logika opisowa

Są to fundamenty dla ontologii. Skłądają się z wiedzy terminologicznej, taksonomii i złożonych relacji. Potrzebne one są aby przy ich pomocą i przy użyciu ich konceptów modelować formalną semantyką po to aby uzyskać automatyczne wnioskowanie.

### Składnie logik opisowych

* ABox - assertions, są to konkretne obiekty (trójki RDF)
* TBox - terminology, budowa pojęć, hierarchia i własnoći (definicje pojęć)

Klasy złożone są z predykatów jednoarguemntowych, a relacje złożone z predykatów binarnych.

### Reprezentacja bazy wiedzy

Baza taka składa się z dwóch części. Indywidułów i klas oraz relacji między nimi. (ABox i TBox)

### Logika opisowa ALC

* ABox 
    * przypisanie indywidułów - Father(john)
    * przypisanie relacji - hasWife(john, mary)
* TBox
    * podklasa - $\sqsubseteq$
    * koniunkcja - $\sqcap$
    * równość - $\equiv$
    * alternatywa - $\sqcup$
    * negacja - $\neg$

### Unikalne nazwy 

Kiedy dwa indywidua mają różne nazwy są różnymi indywiduałami. OWL nie traktuje tego w ten sposób.

W OWL mogą być dwie instancje o różnych nazwach ale to nie znaczy że to są różne indywiduła. Jeśli chcemy się upwnić że dwa różne obiekty są różne musimy do zdefiniwoać poprzez differentFrom. 

### Założenie otwartości świata

Wnioskując w OWL nie możemy założyć że nasza baza jest kompletna. Nie dedukujemy fałszu tylko z powodu braku prawdy.

### Reguły 

Reguły są natralną formą reprezentacji wiedzy. 

* Poziom składniowy

    Zakodowanie składni reguł i wsparcie aplikacji i elastycznego przetwarzania danych. (RuleML i RIF)

* Poziom semantyki (znaczenie reguł)

    Nawiązują do rozwiązań innych systemów (programowanie w logice), automatyczne wnioskowanie, reguły biznesowe. Składnia dopuszcza różne semantyki więc trzeba to zawiężać. 

    Wynikiem uruchomienia reguły jest wytworzenie nowego faktu nie jest monotoniczne więc jest sprzeczne z ontologią.

* Poziom architektury 
    * Hybrydowa
    
        Semantyczny podział między komponentami a regułami

    * Homogeniczna

### Klauzula Horna

Koniunkcje warunków w części warunkowej i w części decyzyjnej stwierdzenia/hipotezy. Aby reguła została uruchomiona musi być spełniona pełna część warunkowa. Nie używamy tutaj też negacji i innych symboli.

### SWRL

Dołączenie klauzul Horna do języka OWL. Ma on jednak charakter nierozstrzygalny co jest jego problemem.

### Systemy semantycznych wiki

Systemy które pojawiają się jako rozwiniecie klasycznych systemów wiki. Dodanie do takiego systemu mechanizmów semantycznych aby reprezentować wiedzę w sposób semantyczny. Miało to się opierać na dodawaniu adnotacji smantycznych które dla użytkowanka były by widoczne w dalszym stopniu w sposób czytelny i normalny.


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


## Wykład nr 7

---

### Inżyniernia wiedzy

Dyscyplina w której wprowadzmy wiedzę do jakiegoś systemu komputerowego po to aby rozwiązać problemy wymagające dużej ilości ludzkiej ekspertyzy.

### Grupowa inżynieria wiedzy

Proces inżynierji w której wprowadzana jest wiedza do systemów aby rozwiązywać problemy, wykonywany przez grupę ludzi.

### Sposoby tworzenia wiedzy

- Kooperacja

    Dzielenie wiedzy na fragmenty i osoby które robią danyc fragment niezależnie bez przeszkadzania innym.

- Kolaboracja

    Współpraca wielu ludzi chcących osiągnąć wspólny cel ale mając inną motywację.

- Kolektywana

    Jednorodna grupa ludzi którzy mają podobny cel i podobne interesy. Jest to podgrupa kolaboracji.

### Semantyczne wiki

Problem ze zwykłmy wiki jest taki że nie pozwalają one nam w prosty sposób wyciągać z nich informacji lub podają nam sprzeczne i niespójne między sobą informacje.

Informacje na wiki możemy łączyć z tagami przez co będzie to tworzyło proste trójki a użytkownik będzie to widział w sposób naturalny. W ten sposób powstają semantyczne wiki.

### Połącznie między OWL

- każda strona to instancja
- kategorie to klasy
- własności to własności OWL
- wartości własności to literały lub instancje

### Typy ontologii

1. Ontologia Fundamentalna - jest to generalna ontologia, używana między różnymi domenami, reprezentuje generalna koncepty niezalażne od problemu
2. Ontologia dziedzinowa - fundamenty wewnątrz jakiejś dziedziny 
3. Ontologia aplikacyjna - zajmuje się wyspecjalizowanymi zadaniami i dziedzinami 
4. Ontolgia zadań - fundamentalne koncepty głównych aktywności

### Rodzaje wiki semantycznych 

- Proste semantyczne wiki

    Jest to rozszerzenie markupa o trójki. Jedna strona to jeden temat.

- Wiki danych 

    Wykorzystują dedykowane edytory do przechowywania semantycznych danych zamiast czystego tekstu. Brak powielania danych ale struktura jest ograniczona.

- Semantyczne wiki wiedzy

    Poza trójkami znajdują się inne metody reprezentacji i weryfikacji wiedzy.


## Wykład nr 8

---

### Wielkość danych 

Procesowanie plików tekstowych nie jest skalowalne. A ręczne zbieranie danych z różnych źródeł jest ciężki i czasochłonne.

### Wymagania aplikacji oparte o grafy wiedzy

- Integracja danych 

    Pobiera dane bezpśrednio z grafów lub wczytywać dane i w momencie wczytywania przetwarzać je na dane semantyczne.

- Przechowywanie RDF

    Istnieją specjalne silniki bazodanowe zoptymalizowane pod zapisywanie i odpytywanie trójek.

    Podstawowymi struktorami danych są trójki i grafy. 

- Logika i UI
- Publikowanie danych

    Czasem chcemy aby nasza aplikacja mogła publikowac gdzieś dane. Opcją jest wrzucenie plików RDF gdzieś do internetu i odczytywanie ich albo umieszczenie danych w treści stron HTML. Innym rozwiązaniem są endpointy SPARQL.

### Frameworki

- wspierają RDF, RDFS, OWL
- wnioskowanie dla RDFS i OWL
- posiadają wspacie dla enspointów SPARQL
- obsługa i przechowywanie danych 
- często używane zadania zaimplementowane jako moduły
