# Gżegżółka, czyli podstawy gita w oparciu o GitHub

Kiedy ostatnio przygotowywaliście jakąś pracę w grupie? Może jakaś prezentacja na lekcję historii, albo plansze z anatomią żaby na biologię?

Jakieś pomysły na wspólna edycję plików?

* Współdzielony dokument na Google Drive, Sharepoint, Office365.
* Dołączanie plików do czatu na Teams.
* Wysyłanie plików mailem bądź przenoszenie ich na pendrive. (Ktoś to jeszcze robi?)

## Wyzwania wspólnej pracy na plikach

* Która wersja jest najnowsza?
* Konflikt edycyjny.
* Problemy ze scalaniem zmian.
* Kto to zmienił?
* Dlaczego to zmieniono?
* Czy można wycofać tę konkretną zmianę?
* ...
* ...
* ...

Jakie są najczęstsze skutki użycia "naiwnych" sposobów pracy w grupie?

* `Ej, gdzie się podziały moje zmiany?`
* `Który cymbał to pozmieniał?!`
* `Prezentacja.ppt`, `Prezentacja poniedziałek.ppt`, `Prezentacja gotowa.ppt`, `Prezentacja skończona.ppt`, `Prezentacja z poprawkami.ppt`... I jeszcze z dziesięć podobnych.
* `A mess a mess a mess a mess. Dirty. Dirty. Dirty. Why room so messy question?`

![Niespodzianka!](/ilustracje/I_sit_on_the_toilet.jpg)

## Jakie rozwiązania dostarczają systemy kontroli wersji (takie jak git)

* Śledzenie zmian (kto, kiedy, dlaczego i co zmienił).
* Możliwość cofnięcia się w czasie do dowolnego momentu.
* Wskazywanie najbardziej aktualnej wersji.
* Porównywanie ze sobą różnych wersji tego samego pliku.
* ...
* ...
* ...

Dodatkowo, `git` dostarcza następujące ułatwienia:

* Łatwe scalanie kilku zmian w jednym pliku.
* Rozwiązywanie konfliktów edycyjnych.
* Łatwą izolację wersji rozwojowych od działających.
* ...
* ...
* ...

## Czego `git` nie załatwi

Systemy kontroli wersji (czyli np. `git`) są zaprojektowane do pracy z danymi tekstowymi. Niestety, prezentacja w PowerPoincie kiepsko śledzi się w gicie... Słyszał ktoś kiedyś o LaTeX-u?

KTO UMIESZCZA W REPOZYTORIUM GIT ZMIENNE DANE BINARNE, A W SZCZEGÓLNOŚCI:
* SKOMPILOWANE PLIKI BINARNE,
* PLIKI .APK, .IPK, DOWOLNE INNE APLIKACJE MOBILNE,
* DUŻE PLIKI MULTIMEDIALNE EDYTOWANE W PROJEKCIE

PODLEGA KARZE POZBAWIENIA WYPŁATY NIE NIŻSZEJ NIŻ TRZY MIESIĄCE, KARZE NAGANY, BĄDŹ KARZE ZMIANY ZESPOŁU NA PIERWSZĄ LINIĘ WSPARCIA ORANGE.

(Czysty `git` nie da rady, ale np. rozwiązania `SoftwareForge`, takie jak `Github`, albo `gitea`/[`forgejo`](https://forgejo.org/) czy `GitLab` - jak najbardziej potrafią trzymać pliki wynikowe kompilacji i zbudowane projekty.)

## Dzielimy się na grupy

## Zakładamy pierwsze repozytorium

![Nowe repozytorium](/ilustracje/nowe_repo.jpg)

![Nowe repozytorium](/ilustracje/nowe_repo_ustawienia.jpg)

## Dodajemy pliki

* Co to jest `repozytorium`?
* Co to znaczy, że `git` jest `rozproszonym systemem kontroli wersji`?
* Co to jest `klonowanie`?

![Pierwsze klonowanie](/ilustracje/firstclone.jpg)

`git clone https://itakdalej`

* Dlaczego `https` a nie `ssh`? 
* Dokąd sklonował?

`git checkout -b main`

* Opcja `-b` powoduje utworzenie brancha.
* Co to w ogóle jest `branch`?

Zbiór commitów opatrzonych wspólną etykietą.

Jak się to rozrysowuje? W określoną strukturę - historia.

* Teraz utwórz plik `README.md`...

`git add .`

* Wskazanie `.` oznacza: `dodaj wszystko w tym katalogu`. Możesz też zamiast kropki napisać `README.md`
* Co to jest commit (po polsku: migawka)? Może lepiej snapshot...
* Czy to już teraz mam się przedstawić?

`git commit -m "Mój pierwszy commit"`

* Co to znaczy `wypchnąć`/`push` pliki?
* Co to jest `upstream`?
* Jeśli do tej pory się nie przedstawiłem, to teraz na pewno będę musiał.

`git push -u origin main`

## Zapraszamy kolegę/koleżankę

![Nowe repozytorium](/ilustracje/collaborators.jpg)

## Pracujemy na branchu - najpierw właściciel

* Wybierz jeden z tekstów w tym repozytorium - bądź opracuj własny, jeśli potrafisz zrobic to szybko.
* Utwórz branch, na przykład o nazwie `challenge`, `task` - cokolwiek Ci odpowiada.
* Dodaj na niego tekst w formie wyzwania, i poinformuj, na czym to wyzwanie polega.

## Pracujemy na branchu - teraz collaborator

* Sklonuj repozytorium kolegi.
* Przełącz się na branch z testami.
* Na tej podstawie utwórz własny branch o nazwie `response`, `answer` itp.
* Popraw załączomy plik, udzielając odpowiedzi (dyktando).

## Robimy pull request

* Co to jest `pull request`? (To wcale nie jest termin z `gita`!)

![Compare and pull request](/ilustracje/compare_and_pull_request.jpg)

* Co to jest `merge` (i to jak najbardziej jest termin z `gita`)?
* Co to jest `squash` i `rebase`?

(Rebase przenosi commity na docelowy branch, zmieniając ich ID).

![Merge](/ilustracje/merge.jpg)

## Ustawienia

![Ustawienia](/ilustracje/ustawienia.jpg)

## Jak stoimy z czasem?

## Pipeline - GitHub Actions

* Testy wymagane do przejścia, zanim będzie można zmergować kod.
* Budowanie aplikacji po mergu.
* Automatyczne deploymenty.
* ...
* ...
* ...

Runner - automatyzacja musi się gdzieś wykonać.

* Jeśli runnery z GitHuba nie mają dostępu do Twojej infrastruktury - stawiasz własny w odpowiednim miejscu.
* Jeśli masz specjalne wymagania co do runnera (na przykład określony sprzęt) - stawiasz własny runner.

Pipeline.yml - skrypt automatyzujący.

* Triggers - w odpowiedzi na jakie zdarzenia należy odpalić pipeline?
* Jobs - sposoby na równoległe wykonywanie zadań w pipeline.
* Tasks - zadania cząstkowe.

## GitFlow

Model pracy z branchami:
* Branch główny - na nim "ma zawsze działać"
* Branch dev - stąd zaczynamy konkretne zadania, tutaj je mergujemy
* Wydanie nowej wersji - tworzymy branch release-candidate, po testach mergujemy go do main

Oczywiście możecie sobie ustalić dowolny sposób, jaki Wam odpowiada.

## GitOps

Idea mówiąca, że stan repozytorium `git` odzwierciedla całość systemu informatycznego. Zmiany w repozytorium skutkują np zmianami na infrastrukturze... Ale to nieco bardziej złożone :)