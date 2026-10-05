# Biblio
## Prérequis
## Installation
## Utilisation
## Tests
## Structure du projet
## Contribuer
## Auteurs


# Biblio

Une application en ligne de commande permettant de gérer la bibliothèque d'une association, destinée aux bénévoles.

## Prérequis

- Python 3.10 ou supérieur
- Git / GitHub Desktop

*Note : Selon votre système d'exploitation, utilisez `python`, `python3` ou `py`.*

## Installation

1. Cloner le dépôt avec GitHub Desktop :
   `File` > `Clone repository` > onglet `URL`.
2. Ouvrir le terminal dans le dossier du projet :
   `Repository` > `Open in Command Prompt`.
3. Initialiser la base de démonstration (à faire une seule fois) :
```bash
python biblio.py init


Sous macOS / Linux, utilisez python3 biblio.py init. Sous Windows, si python ne fonctionne pas, utilisez py biblio.py init.

Résultat attendu :

Plaintext
Base initialisee : 6 livres, 3 membres.
Utilisation
Initialiser la base
Bash
python biblio.py init
Résultat attendu :

Plaintext
Base initialisee : 6 livres, 3 membres.
Lister tous les livres
Bash
python biblio.py livres
Résultat attendu :

Plaintext
[1] 1984 - George Orwell (Disponible)
[2] Le Petit Prince - Antoine de Saint-Exupéry (Disponible)
[3] Fondations - Isaac Asimov (Emprunté)
Emprunter un livre
Bash
python biblio.py emprunter --livre 1 --membre 2
Résultat attendu :

Plaintext
Livre '1984' emprunté avec succès par le membre 2.
Rendre un livre
Bash
python biblio.py rendre --livre 1
Résultat attendu :

Plaintext
Livre '1984' rendu avec succès.
Tests
Pour exécuter la suite de tests automatisés :

Bash
python -m unittest discover tests
Variantes selon l'OS : python3 -m unittest discover tests ou py -m unittest discover tests.

Résultat attendu :

Plaintext
......
----------------------------------------------------------------------
Ran 6 tests in 0.012s

OK