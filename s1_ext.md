### `history`:
Polecenie służy do wyświetlania i zmiany historii wykonanych poleceń w terminalu. Dostępne opcje to:

- **history [n]** wyświetla n ostatnich poleceń
- **history -c** usuwa historię poleceń
- **history - d [n]** usuwa z historii polecenie o numerze n, w przypadku gdy n jest ujemne usuwa polecenie n-te od końca 
- **history -anwr [nazwa pliku]** zapisuje historię poleceń do pliku o nazwie *nazwa pliku*

### `mkdir`:
Polecenie służy do tworzenia katalgów. Dostępne opcje to:
- **mkdir [nazwa katalogu]** w obecnym katalogu tworzy nowy katalog o nazwie *nazwa pliku*
- **mkdir -p [ścieżka katalogu]** tworzy nowy katalog oraz nadrzędne katalogi jeżeli jest to potrzebne 
- **mkdir -v [nazwa katalogu] ** tworzy nowy katalog/nowe katalogi oraz wypisuje wiadomość po stworzeniu każdego z nich
- **mkdir -m** tworzy nowy katalog oraz pozwala ustawić prawa dostępu do niego jak w poleceniu *chmod*

### `cd`:
Polecenie służy do zmiany katalogu roboczego. Możliwe zastosowania to:
- **cd [ścieżka katalogu]** przenosi do katalogu znajdującego się po podaną ścieżką. Ścieżka ta może zaczynać się zarówno w roocie jak i w katalogu w którym obecnie jesteśmy
- **cd .** przenosi nas do katalogu w którym obecnie jesteśmy
- **cd ..** przenosi nas do katalogu nadrzędnego
- **cd ~** przenosi do katalogu domowego
- **cd -** przenosi do poprzednio odwiedzonego katalogu 
