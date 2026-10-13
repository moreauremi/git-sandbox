# Aide-mémoire Git

## Branches

| Commande | Rôle |
|---|---|
| `git switch -c ma-branche` | Créer une branche et s'y placer |
| `git switch main` | Revenir sur `main` |
| `git branch` | Lister les branches locales |
| `git merge ma-branche` | Fusionner `ma-branche` dans la branche courante |
| `git branch -d ma-branche` | Supprimer une branche déjà fusionnée |
| `git log --oneline --graph --all` | Voir l'historique sous forme d'arbre |

## Pull requests (GitHub CLI)

| Commande | Rôle |
|---|---|
| `gh pr create` | Ouvrir une PR depuis la branche courante |
| `gh pr list` | Lister les PR ouvertes |
| `gh pr checkout 12` | Récupérer la PR n°12 en local |
| `gh pr merge --squash` | Merger la PR en un seul commit |

## Lier une PR à une issue

Écrire `Closes #12` dans la description de la PR : l'issue n°12 se ferme automatiquement au merge.

## Les 3 façons de merger une PR

- **Merge commit** : garde tous les commits de la branche, plus un commit de fusion
- **Squash and merge** : regroupe tous les commits de la branche en un seul
- **Rebase and merge** : rejoue les commits sur `main`, sans commit de fusion
