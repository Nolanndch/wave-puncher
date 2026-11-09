# The Wave Puncher

Jeu de survie au tour par tour en Python et Pygame, réalisé pour le projet de Terminale NSI
(lycée Charlotte Perriand, 2025-2026). Il s'inspire des anciens Pokémon : on explore une grille,
on ramasse des objets et on affronte des vagues de monstres.

## Qui a fait quoi

- **Code du jeu** : Nolann Duchaussoy. Il a écrit la logique du jeu : déplacements, tours de jeu,
  combats, vagues, objets, progression du joueur, modes solo et joueur contre joueur.
- **Interface** : faite avec l'aide de Claude (IA d'Anthropic), surtout dans `UI.py`.
- Projet de groupe mené avec Riley Huriere, qui a participé aux idées de jeu.

## Modes de jeu

- **Solo** : survivre à toutes les vagues d'ennemis. Le nombre de vagues dépend de la difficulté
  choisie (facile, moyen ou difficile). Entre deux vagues, on choisit une amélioration : plus de
  déplacements, plus de vie ou plus de force.
- **Joueur contre joueur** : les deux joueurs ramassent le plus d'objets possible sur la carte avant
  la fin du décompte. Ensuite le combat commence au tour par tour, et le premier joueur à attaquer
  est tiré au sort.

Pendant un combat, on peut **attaquer** ou **se soigner** avec les objets de l'inventaire : soin,
épée (dégâts) et plastron (protection).

## Lancer le jeu

```bash
pip install pygame
python main.py
```

Le jeu s'ouvre en plein écran.

| Touche | Action |
|--------|--------|
| Flèches | Se déplacer sur la grille |
| Souris | Menus, actions de combat, choix des améliorations |
| Échap | Revenir à l'écran précédent |
| E | Quitter |

## Organisation du code

| Fichier | Rôle |
|---------|------|
| `main.py` | Boucle de jeu et gestion des états (menu, partie, combat, niveau, JcJ…) |
| `fonction.py` | Logique du jeu : déplacements, combats, vagues, grille |
| `entities.py` | Classes `Player`, `Mob` et `Objet` |
| `parametres.py` | Réglages : taille de la grille, délais, difficulté, couleurs |
| `bouton.py` | Zones cliquables des boutons |
| `UI.py` | Affichage des écrans et de l'interface |

On peut ajouter facilement de nouveaux objets dans `entities.py` et de nouveaux réglages dans
`parametres.py`.
