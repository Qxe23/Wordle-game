# Wordle Game — Version Python avec interface Tkinter

## Description du projet

Ce projet est une **implémentation du jeu Wordle en Python**, avec une interface graphique construite à l’aide de **Tkinter**.  
L’objectif du jeu est de **deviner un mot de 5 lettres en un maximum de 6 essais**.  
Après chaque tentative, les lettres sont colorées pour indiquer leur exactitude :

- 🟩 **Vert** : la lettre est correcte et bien placée.  
- 🟨 **Jaune** : la lettre est présente dans le mot mais mal placée.  
- ⬜️ **Gris** : la lettre n’existe pas dans le mot cible.

Le mot à deviner est choisi **aléatoirement** à partir d’un fichier `Lexique383.tsv`, qui contient une liste de mots français.

---

## Fonctionnalités principales

- Interface graphique intuitive avec **grille et clavier virtuel AZERTY**.  
- Gestion du **clavier physique** (vous pouvez taper directement les lettres).  
- **Coloration automatique** des lettres selon leur justesse.  
- Vérification que le mot saisi existe bien dans le lexique fourni.  
- **Suppression des accents** pour éviter les erreurs de comparaison.  
- Messages d’**erreur**, de **victoire** ou de **défaite** via des pop-ups.  
- Fin de partie automatique en cas de victoire ou d’échec.

---

## Structure du code

Le jeu est construit autour de la classe `WordleGame`, qui regroupe toutes les fonctionnalités principales.

| Méthode | Description |
|----------|--------------|
| `__init__()` | Initialise le jeu (grille, clavier, mot cible aléatoire) |
| `load_words()` | Charge les mots depuis un fichier `.tsv` |
| `normalize_word()` | Supprime les accents et met les mots en minuscules |
| `create_grid()` | Crée la grille où s’affichent les tentatives |
| `create_keyboard()` | Crée le clavier virtuel (AZERTY) |
| `on_key_press()` | Ajoute une lettre à la ligne courante |
| `on_delete_press()` | Supprime la dernière lettre saisie |
| `on_enter_press()` | Valide la tentative |
| `check_word()` | Compare le mot saisi avec le mot cible |
| `color_cells()` | Colore les lettres selon leur justesse |
| `run()` | Lance la boucle principale Tkinter |

---

## Données utilisées

Le jeu s’appuie sur un fichier `Lexique383.tsv` contenant une liste de mots français.  
Chaque mot doit apparaître dans la **première colonne** du fichier.

---

## Améliorations possibles

- Ajouter un mode sombre ou un thème personnalisable.
- Permettre des mots de longueurs variables (4, 6, 7 lettres...).
- Sauvegarder les statistiques de jeu (taux de réussite, tentatives, etc.).
- Ajouter une option “mot du jour” fixe selon la date.
- Traduire l’interface pour d’autres langues.
