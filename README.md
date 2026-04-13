# Gżegżółka, czyli podstawy gita w oparciu o GitHub

Kiedy ostatnio przygotowywaliście jakąś pracę w grupie? Może jakaś prezentacja na lekcję historii, albo plansze z anatomią żaby na biologię?

Jakieś pomysły na wspólna edycję plików?

* Współdzielony dokument na Google Drive, Sharepoint, Office365
* Dołączanie plików do czatu na Teams
* Wysyłanie plików mailem bądź przenoszenie ich na pendrive (ktoś to jeszcze robi?)

## Wyzwania wspólnej pracy na plikach

* Która wersja jest najnowsza?
* Konflikt edycyjny
* Problemy ze scalaniem zmian
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

* Śledzenie zmian (kto, kiedy, dlaczego i co zmienił)
* Możliwość cofnięcia się w czasie do dowolnego momentu
* Wskazywanie najbardziej aktualnej wersji
* Porównywanie ze sobą różnych wersji tego samego pliku
* ...
* ...
* ...

Dodatkowo, `git` dostarcza następujące ułatwienia:

* Łatwe scalanie kilku zmian w jednym pliku
* Rozwiązywanie konfliktów edycyjnych
* Łatwą izolację wersji rozwojowych od działających
* ...
* ...
* ...

## Czego `git` nie załatwi

Systemy kontroli wersji (czyli np. `git`) są zaprojektowane do pracy z danymi tekstowymi. Niestety, prezentacja w PowerPoincie kiepsko śledzi się w gicie... Słyszał ktoś kiedyś o LaTeX-u?

KTO UMIESZCZA W REPOZYTORIUM GIT ZMIENNE DANE BINARNE, A W SZCZEGÓLNOŚCI:
* SKOMPILOWANE PLIKI BINARNE
* PLIKI .APK, .IPK, DOWOLNE INNE APLIKACJE MOBILNE
* DUŻE PLIKI MULTIMEDIALNE EDYTOWANE W PROJEKCIE

PODLEGA KARZE POZBAWIENIA WYPŁATY NIE NIŻSZEJ NIŻ TRZY MIESIĄCE, KARZE NAGANY, BĄDŹ KARZE ZMIANY ZESPOŁU NA PIERWSZĄ LINIĘ WSPARCIA ORANGE.

(Czysty `git` nie da rady, ale np. rozwiązania `SoftwareForge`, takie jak `Github`, albo `gitea`/[`forgejo`](https://forgejo.org/) czy `GitLab` - jak najbardziej potrafią trzymać pliki wynikowe kompilacji i zbudowane projekty.)

## Dzielimy się na grupy

## Zakładamy pierwsze repozytorium

![Nowe repozytorium](/ilustracje/nowe_repo.jpg)

![Nowe repozytorium](/ilustracje/nowe_repo_ustawienia.jpg)

## Dodajemy pliki

## Zapraszamy kolegę/koleżankę

![Nowe repozytorium](/ilustracje/collaborators.jpg)

## Pracujemy na branchu

## Robimy pull request