### `history`
Polecenie służy do wyświetlania i zmiany historii wykonanych poleceń w terminalu. Dostępne opcje to:

- `history [n]` wyświetla n ostatnich poleceń
- `history -c` usuwa historię poleceń
- `history - d [n]` usuwa z historii polecenie o numerze n, w przypadku gdy n jest ujemne usuwa polecenie n-te od końca 
- `history -anwr [nazwa pliku]` zapisuje historię poleceń do pliku o nazwie *nazwa pliku*

### `mkdir`
Polecenie służy do tworzenia katalgów. Dostępne opcje to:
- `mkdir [nazwa katalogu]` w obecnym katalogu tworzy nowy katalog o nazwie *nazwa pliku*
- `mkdir -p [ścieżka katalogu]` tworzy nowy katalog oraz nadrzędne katalogi jeżeli jest to potrzebne 
- `mkdir -v [nazwa katalogu] ` tworzy nowy katalog/nowe katalogi oraz wypisuje wiadomość po stworzeniu każdego z nich
- `mkdir -m` tworzy nowy katalog oraz pozwala ustawić prawa dostępu do niego jak w poleceniu *chmod*

### `cd`
Polecenie służy do zmiany katalogu roboczego. Możliwe zastosowania to:
- `cd [ścieżka katalogu]` przenosi do katalogu znajdującego się po podaną ścieżką. Ścieżka ta może zaczynać się zarówno w roocie jak i w katalogu w którym obecnie jesteśmy
- `cd .` przenosi nas do katalogu w którym obecnie jesteśmy
- `cd ..` przenosi nas do katalogu nadrzędnego
- `cd ~` przenosi do katalogu domowego
- `cd -` przenosi do poprzednio odwiedzonego katalogu

## `passwd`
Jest to komenda, która pozwala na ustawienie lub zmienienie hasła do konta użytkownika. 
Dla administratora pozwala również zmianę hasła dla innych kont

```
passwd [*opcja*] [*login*]
```
Przykładowe opcje:
* -d - usuwa hasło


## `pwd`
skrót od *print working directory*.
Wyświetla ścieżkę do folderu w jakim się znajdujemy

```
pwd [*opcja*]
```


## `ls`
skrótowo *ang. list*
Wpisane pokazuję nam listę plików jakie znajdują się w aktualnie używanym folderze
```
ls [*opcja*] [*plik*]
```

Przykładowe opcje:
* -l - pokazuje nam bardziej szczegółową liste plików
* -lt - szczegółowa lista zostanie dodatkowo posortowana od ostatnio używanych plików


## `find` 
The `find` command can be used in a Linux terminal to search for files or directories within a specified path. [The Linux manual page](https://linux.die.net/man/1/find) provides the following format for using the `find` command:

```sh
find [-H] [-L] [-P] [-D debugopts] [-Olevel] [path...] [expression]
```

For our purposes, the `[-H]`, `[-L]`, `[-P]`, `[-D debugopts]`, and `[-Olevel]` options shall be omitted. These affect the way the `find` command treats symbolic links as well as reordering tests conducted by the command to speed up execution.

#### Searching for a file

The following format can be used when searching for a file, starting the search at a certain path (directory):

```sh
find [path] -name [filename] -type f
```

Here is an example use case:

```sh
find ./ -name "*.page" -type f
```

This command will start searching in the current working directory (`./`) for a file (specified with the `-type f` argument) of the exact name `*.page`, where the asterisk here can be replaced with any permissible string of symbols. The word "exact" here refers to the other symbols specified without the asterisk, that is `.page`. In other words, the `file` command will search for any file that ends with `.page`.

In the case that we would like the command to search for files while remaining case-insensitive, that is, to also output the path of files that in the above case would have a file ending of `.Page`, `.PAGE`, etc., we should use the -iname argument.

#### Searching for a directory

A very similar format to the one used when searching for a file is used when searching for a directory:

```sh
find [path] -name [directoryname] -type d
```

The main difference here is that we specify the argument `-type` to look for directories, `d`.

Example use case:

```sh
find ./ -name "pictures" -type d
```
