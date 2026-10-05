# ADR 0001 : Python sans bibliothèque externe

- Statut : accepté
- Date : 2026-10-05
- Décideurs : @Hika-li

## Contexte
Biblio est installé par des bénévoles de l'association, sur leurs propres ordinateurs.
Chaque installation supplémentaire (pip install, version de bibliothèque) est une source
d'erreur et d'appels à l'aide.

## Options envisagées
1. Bibliothèque standard seule (sqlite3, unittest, datetime).
   Pour : rien à installer en plus de Python.
   Contre : un peu plus de code à écrire nous-mêmes.
2. Bibliothèques externes (click, SQLAlchemy, pytest).
   Pour : code plus court et plus confortable.
   Contre : pip install obligatoire, versions à suivre, installation plus fragile
   chez les bénévoles.

## Décision
Biblio n'utilise que la bibliothèque standard de Python.

## Conséquences
Plus facile : installer Biblio et le faire tourner sur n'importe quel ordinateur avec Python.
Plus difficile : certaines fonctions sont à écrire nous-mêmes, et les tests utilisent
unittest plutôt que pytest.
À surveiller : si une bibliothèque externe devient indispensable, écrire un nouvel ADR
qui remplace celui-ci.
