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

