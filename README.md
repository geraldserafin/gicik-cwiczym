# Zadanie grupowe - Wspólna praca nad repozytorium

## Cel zadania

Celem zadania jest przećwiczenie współpracy z wykorzystaniem GIT , z zastosowaniem
poleceń:

- Tworzenie gałęzi.
- Wysyłanie pull requestów.
- Rozwiązywanie konfliktów.
- Tworzenie odwrotnych commitów.
- Rebase i zarządzanie historią.
- Usuwanie gałęzi i utrzymanie porządku w repozytorium.

## Opis zadania

### 1. Tworzenie gałęzi i dodawanie zmian

- Każdy członek zespołu tworzy swoją gałąź o nazwie `feature/[indeks]`.
- Każdy dodaje plik o nazwie `feature_[indeks].txt` i zapisuje w nim dowolną
  treść.
- Każdy dodaje i zatwierdza swoje zmiany w lokalnym repozytorium.
- Każdy wypycha gałąź na zdalne repozytorium.

### 2. Tworzenie pull requestów

- Każdy członek zespołu tworzy pull request z własnej gałęzi (`feature/[indeks]`)
  do głównej gałęzi main.
- PR powinien zawierać tytuł i krótki opis wprowadzanych zmian.
- Każdy z członków zatwierdza zmiany innego członka (1 dla 2, 2 dla 3, 3 dla 1).

### 3. Wprowadzanie konfliktu

- Każdy członek zespołu tworzy nową gałąź `feature/readme_[indeks]`.
- Każdy wprowadza zmiany w pliku `README.md` w drugiej linijce
- Każdy tworzy pull request z własnej gałęzi (`feature/readme_[indeks]`) do
  głównej gałęzi `main`.

### 4. Merge i rozwiązywanie konfliktów

- Wyznaczany jest lider zespołu, który akceptuje swoje zmiany.
- Każdy, oprócz lidera, dociąga swoją lokalną gałąź `main` do zdalnego
  repozytorium.
- Każdy, oprócz lidera, robi merge gałęzi main do swojej gałęzi.
- Każdy, oprócz lidera, w przypadku konfliktów rozwiązuje je lokalnie, czyli w
  pliku `README.md`, gdzie celowo dodano sprzeczne linie przez różnych
  członków zespołu.
- Każdy, oprócz lidera, wypycha zmiany na swoją gałąź (`feature/readme_[indeks]`).
- Każdy, oprócz lidera, z członków zatwierdza zmiany innego członka (1 dla 2,
  2 dla 3, 3 dla 1).
- Lider zespołu dociąga swoją lokalną gałąź `main` do zdalnego repozytorium.
- Lider zespołu robi merge gałęzi `main` do swojej gałęzi.
- Lider wprowadza u siebie zmiany na swoim branchu, które polegają na
  zmianie kolejności członków w pliku `README.md`. Lider tworzy pull requesta.
- W przypadku konfliktów lider rozwiązuje je lokalnie.
- Jeden z członków zespołu zatwierdza pull requesta lidera.

### 5. Tworzenie odwrotnego commita za pomocą revert

- Każdy z członków zespołu przechodzi na gałąź `feature/[indeks]` i dodaje
  błędny plik, który nie powinien znaleźć się w repozytorium.
- Każdy wykonuje commit tego pliku.
- Każdy korzysta z polecenia git revert, aby odwrócić swoje zmiany.
- Każdy tworzy nową gałąź `feature/[indeks_revert]` na bazie gałęzi
  `feature/[indeks]` i wypycha ją zdalne repozytorium.

### 6. Łączenie commitów za pomocą rebase

- Każdy z członków zespołu przechodzi na gałąź `feature/[indeks]`.
- Każdy dodaje dwa pliki (`file1.txt` i `file2.txt`) i wykonuje po jednym commicie dla
  każdego pliku.
- Każdy łączy commity w taki sposób, aby pozbyć się informacji o złej zmianie,
  revercie i dodaniu plików, zamieniając to w jeden commit przy pomocy
  interaktywnego rebase.
- Po wykonaniu rebase wypycha zmiany na swoją gałąź (`git push --force`, jeśli
  to konieczne).

### 7. Tworzenie i usuwanie niepotrzebnych gałęzi

- Każdy członek tworzy nową gałąź `feature/[indeks]_toDelete`.
- Każdy tworzy plik `[indeks]_PR.txt`.
- Każdy commituje zmiany, wypycha na zdalne repozytorium i tworzy pull
  requesta.
- Lider zespołu zatwierdza zmiany każdego członka.
- Każdy usuwa swoją lokalną gałąź, która została zmergowana do main.
- Lider zespołu usuwa zdalne gałęzie (`feature/[indeks]_toDelete`) po
  zakończeniu scalania pull requestów.
