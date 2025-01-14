# Notatki dla **[Bash for beginners](https://www.youtube.com/playlist?list=PLlrxD0HtieHh9ZhrnEbZKhzk0cetzuX7l)**

## (4) How to Get Help in Bash
- w opisie pomocy np. `help cd` lub `cd --help` pipe (`|`) oznacza wykluczającą się opcję - albo jedno, albo drugie, ale nie oba
- `man` - otwiera plik pomocy - nie jesteś już w bash-u tylko w pliku tekstowym
- `man` - nawigacja dostępna po wciśnięciu `H`; `d` - przewijanie w dół, `u` - przewijanie w górę, `/` - pozwala wyszukiwać, `q` - wyjście z man

## (5) How to Navigate the Terminal with Bash
- `pushd`, `popd` - pracują na stosie, nakładają kolejne lokalizacje do jakich się przeszło, szczególnie przydatne w pisaniu skryptów

## (6) How to List Content in the Terminal Bash
- `ls`- można używać _wildcards_ np. `ls S*`, czy `ls [CS]*` - każdy plik, który zaczyna się na 'C' lub 'S'
- `ls [[:upper:]]*` - dowolny wyraz z wielkimi literami lub `ls [[:lower:]]*` małymi literami

## (7) How to Find Files in the Terminal with Bash
> Everyting in Linux is a file somewhere (Dennis Ritchie)
- `whereis` - whereis locates the binary, source and manual files
- `whereis -b` - tylko pliki binarne
- `which` - znajduje tylko pliki wykonywalne
- `find <starting-point> -name "nameOfTheFile.md` np. `find . -name "*.md"`
- jeżeli dla _find_ chce zignorować wielkość znaków to mogę użyć `-iname` zamiast '-name'
- jeżeli chcę przez _find_ wyszukać typ np tylko katalogi to podaje `find . -type d` lub `find . -type f`

## (8) How to Work with Directories in the Terminal with Bash
- katalogi są zaznaczone na zielono w bashu
- można zakładać wiele katalogów poleceniem `mkdir` po spacji
- można robić katalog jeden poziom niżej, dwa poziomy niżej zwróci błąd, żeby to zmienić wystarczy podać parametr `-p`, który spowoduje utworzenie wszystkich folderów w ścieżce
- `touch` jest do tworzenia plików, `mv`, `cp`, `rm`, `rmdir` - usuwanie **pustych** katalogów.

## (9) How to View File Contents in the Terminal with Bash
- `cat`, `head -n 5`, `tail -n 5`, `more` - wyświetlanie pliku w stronach
- `less` - pozwala na więcej operacji - lista po wciśnięciu 'h', np. na wyszukiwanie po slashu '/'
- `grep` - wyszukiwanie wzorca w pliku np. `grep "174" viewing-files/fake002.log`

## (10) What are Environment variables?
- `env` - zmienne środowiskowe
- `echo $SHELL` - jak chcę zobaczyć jedną _env_ to podaje dolar '$' przed jej nazwą
- użyteczne zmienne środowiskowe: `echo $HOME` i `echo $USER`, `echo $PATH`
- tworzenie _env_ dostępnego tylko w tej sesji, jest niedostępne nawet w drugim oknie _bash_: `export newVar=value`
- żeby zmienna środowiskowa istniała pomiędzy sesjami trzeba ją wprowadzić do plików startowych:
    - `/etc/profile` - dla każdego użytkownika zalogowanego na tej maszynie
    - `.profile` w folderze _home_ - dla tego użytkownika
    - `.bashrc` też jest wołany przy uruchamianiu _basha_

## (11) How to Use Redirection and Pipelines in Bash
- przekierowanie '>', dołączania '>>'
- przekierowanie standardowych komunikatów błędów: `ls -l ./non-existing-dir 2> error.txt` - **2** oznacza stanardowe błędy; jest tak bo normalny wynik to strumień nr 1, a błędy to strumień nr 2
- można przekierować strumień na inny strumień, np. zapisanie wyników i błędów do jednego pliku: `ls -l ./non-existing-dir > target.txt 2>&1` lub krótsza wersja w nowych bash-ach: `ls -l &> output2.txt`
- przekierowanie do kolejnej komendy z użyciem `|`: `ls -l /usr/bin/ | grep echo`
> jest komenda **sort** np. `ls -l /usr/bin/ | grep xz | sort`

## (12) How to Modify File Permissions in Bash
- _+x_ w _chmod_ powoduje dodanie wykonywanie do wszystkich 3 części do właściciela, grupy i wszystkich




