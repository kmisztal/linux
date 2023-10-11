##  `cat` 
najprostszy filtr, nie wprowadzający zmian do przetwarzanych danych. Użyteczne przełączniki:

- `-s` z paru pustych linii robi jedna
- `-n` numeruje wszystkie linie
- `-b` numeruje niepuste linie
- `-A` pokazuje znaki specjalne

## `head` 
wyświetla początkową część pliku o podanej nazwie lub danych wejściowych otrzymanych z potoku gdy nazwa pliku nie jest podana. Standardowo wyświetlanych jest pierwszych 10 linii odczytanych danych. Używając przełączników liczbę tą można zmienić:

- `-c` pozwala określić liczbę wyświetlanych znaków
- `-n` pozwala określić liczbę wyświetlanych linii

## `tail` 
wyświetla końcową część pliku o podanej nazwie lub danych wejściowych otrzymanych z potoku, gdy nazwa pliku nie jest podana,. Standardowo wyświetlanych jest ostatnich 10 linii danych. Używając przełączników liczbę tą można zmienić:

- `-c` pozwala określić liczbę wyświetlanych znaków
- `-n` pozwala określić liczbę wyświetlanych linii
- `-f` powoduje, że dane po zapisaniu ich do pliku są wyświetlane na standardowym wyjściu

## `sort`
służy do sortowania danych wejściowych, które domyślnie sortowane są leksykograficznie. Sortowanie danych odbywa się liniami. Najważniejsze przełączniki:

- `-n` pozwala sortować numerycznie
- `-b` ignoruje przy sortowaniu spacje znajdujące się na początku linii
- `-t` pozwala zmienić domyślny separator kolumn, którym są znaki tabulacji lub spacji
- `-f` pozwala ignorować przy sortowaniu wielkość liter
- `-r` odwraca kolejność sortowania
- `+liczba` pozwala by sortowanie odbywało się względem dowolnej kolumny (a nie początku linii). Liczba określa liczbę kolumn pominiętych przy sortowaniu
- `-o` nazwa_pliku zapisuje rezultat sortowania do pliku o podanej nazwie

## `uniq`
umożliwia usunięcie powtarzających się, sąsiadujących linii danych wejściowych.

- `-d` wyświetla z danych wejściowych tylko linie powtarzające się
- `-u` wyświetla z danych wejściowych tylko linie unikalne
- `-c` zlicza liczbę powtórzeń
- `wc` - zlicza znaki, słowa i linie w podanych danych wejściowych. Standardowo wyświetlane są wszystkie trzy wartości, ale można to zmienić:
- `-l` pozwala zliczać tylko linie
- `-w` pozwala zliczać tylko słowa
- `-c` pozwala zliczać tylko znaki
- `tr` - pozwala zamienić łańcuchy tekstowe, które podawane są jako argumenty wejściowe. Znaki z pierwszego łańcuch zamieniane są na znaki z drugiego łańcucha. Dodatkowo, dzięki przełącznikom możliwe jest następujące przetwarzanie:
- `-d` usuwa podane po przełączniku znaki
- `-s` usuwa powtarzające się sąsiednie znaki

## `cut`
pozwala wyświetlić fragmenty wierszy danych wejściowych. Zwykle jest to wycinanie odpowiednich kolumn.- pozwala wyświetlić fragmenty wierszy danych wejściowych. Zwykle jest to wycinanie odpowiednich kolumn.

- `-c` pozwala określić pozycję znakowe wycinanych fragmentów wierszy, np. -c 1-72 wyświetla pierwsze 72 znaki każdego wiersza
- `-f` pozwala określić numery wycinanych kolumn, np. -f1,3-5,10 wyświetla pierwszą kolumnę, kolumny od 3 do 5 oraz kolumnę 10.
- `-d` pozwala zmienić domyślny separator kolumn, którym jest znak tabulacji

## `grep [opcje] wyrażenie [lista_plików]`
przeszukuje dane pochodzące ze standardowego wejścia lub pliki wyszczególnione na liście plików, wypisując tylko linie zawierające szukane wyrażenie. Szukane wyrażenie zapisywane jest za pomocą wyrażenia regularnego. Najważniejsze przełączniki:

- `-v` wyszukuje linie nie zawierające szukanego wzorca
- `-c` podaje liczbę odszukanych wyrażeń
- `-i` ignoruje wielkość liter przy wyszukiwaniu
- `-n` wyświetla numery linii zawierających dany wzorzec
- `-h` przy wyświetlaniu linii zawierających szukany wzorzec pomija nazwy plików
- `-r` pozwala na przeszukiwanie rekurencyjne, np. grep wzorzec -r katalog
- `-l` pokazuje nazwy plików zawierających określony wzorzec
- `-L` pokazuje nazwy plików nie zawierających określonego wzorca

## Zasady konstrukcji podstawowych wyrażeń regularnych opisujących szukany wzorzec są następujące:
- `.` - reprezentuje dowolny znak
- `[abc]` - oznacza jeden ze znaków a, b lub c
- `[a-z]` - oznacza jeden ze znaków z podanego zbioru
- `[^0-9]` - oznacza dopełnienie podanego zbioru
- `.*` - oznacza dowolny ciąg znaków
- `*` - reprezentuje powtórzenie dowolną liczbę razy wyrażenia znajdującego się bezpośrednio po lewej stronie np. A[a]* określa A, Aa, Aaa, Aaaaaaaaa, itd.
- `^` - reprezentuje początek linii
- `$` - reprezentuje koniec linii
- `a\{n\}` - oznacza n-krotne wystąpienie znaku występującego bezpośrednio po lewej stronie nawiasów
- `a\{n, \}` - oznacza co najmniej n-krotne wystąpienie znaku występującego bezpośrednio po lewej stronie nawiasów
- `a\{, m\}` - oznacza co najwyżej m-krotne wystąpienie znaku występującego po lewej stronie nawiasów
- `a\{n,m\}` - oznacza co najmniej n-krotne i co najwyżej m-krotne wystąpienie znaku występującego po lewej stronie nawiasów
