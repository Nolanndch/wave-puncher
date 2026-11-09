# The Wave Puncher

C'est le jeu que j'ai fait pour le projet de Terminale NSI (lycée Charlotte Perriand,
2025-2026). C'est un jeu de survie au tour par tour en Python avec Pygame, un peu inspiré des
anciens Pokémon : on se balade sur une grille, on ramasse des objets et on affronte des vagues
de monstres.

## Qui a fait quoi

- **Le code du jeu, c'est moi** : les déplacements, les tours de jeu, les combats, les vagues,
  les objets, la progression du joueur et les deux modes de jeu.
- **Pour l'interface**, je me suis aidé de Claude, l'IA d'Anthropic, surtout pour `UI.py`.
- On était en groupe avec Riley Huriere ([@Leyz0xx](https://github.com/Leyz0xx)), qui a
  participé aux idées du jeu.

## Les modes de jeu

- **Solo** : il faut survivre à toutes les vagues d'ennemis. Leur nombre dépend de la difficulté
  choisie (facile, moyen ou difficile). Entre deux vagues, on choisit une amélioration : plus de
  déplacements, plus de vie ou plus de force.
- **Joueur contre joueur** : les deux joueurs ramassent le plus d'objets possible avant la fin du
  décompte, puis le combat commence au tour par tour. Celui qui attaque en premier est tiré au sort.

En combat, on peut attaquer ou se soigner avec les objets ramassés : soin, épée (plus de dégâts)
et plastron (plus de protection).

## Lancer le jeu

```bash
pip install pygame
python main.py
```

Le jeu s'ouvre en plein écran.

- **Flèches** : se déplacer
- **Souris** : menus, actions de combat, choix des améliorations
- **Échap** : revenir à l'écran précédent
- **E** : quitter

## Comment le code est organisé

- `main.py` : la boucle de jeu et les différents états (menu, partie, combat, JcJ…)
- `fonction.py` : la logique du jeu (déplacements, combats, vagues, grille)
- `entities.py` : les classes `Player`, `Mob` et `Objet`
- `parametres.py` : les réglages (taille de la grille, délais, difficulté, couleurs)
- `bouton.py` : les zones cliquables des boutons
- `UI.py` : l'affichage des écrans

J'ai organisé le code pour qu'on puisse facilement ajouter des objets dans `entities.py` ou
changer les réglages dans `parametres.py`.
