# Guide des commandes Terminal et Git

## 5 commandes du Terminal

| Commande   | Utilité                                                                | Exemple             |
| ---------- | ---------------------------------------------------------------------- | ------------------- |
| `pwd`      | Afficher le chemin du dossier actuel                                   | `pwd`               |
| `ls -la`   | Lister les fichiers, y compris les fichiers cachés, avec leurs détails | `ls -la`            |
| `cd`       | Changer de dossier ; `..` désigne le dossier parent                    | `cd src` ou `cd ..` |
| `mkdir -p` | Créer des dossiers et leurs parents si nécessaire                      | `mkdir -p src/css`  |
| `touch`    | Créer un fichier vide s’il n’existe pas, sinon actualiser ses dates    | `touch README.md`   |

## 5 commandes Git

### 1. git clone

Copier un dépôt distant sur son ordinateur.

```bash
git clone https://github.com/TON-PSEUDO/tp-git-web.git
```

L’option `--branch` permet de sélectionner la branche à récupérer.

### 2. git switch

Changer de branche. L’option `-c` crée une nouvelle branche.

```bash
git switch main
git switch -c feature-app
```

### 3. git add

Préparer les modifications pour le prochain commit.

```bash
git add src/index.html
```

`git add .` prépare les modifications du dossier courant et de ses
sous-dossiers. `git add -A` prépare toutes les modifications du dépôt,
y compris les suppressions.

### 4. git commit

Enregistrer les modifications préparées dans l’historique local.
L’option `-m` permet de préciser le message.

```bash
git commit -m "feat(html): ajout de la structure de base"
```

Un commit atomique correspond à une modification cohérente et ciblée.

### 5. git push

Envoyer les commits locaux vers le dépôt distant.
L’option `-u` configure le suivi de la branche distante.

```bash
git push -u origin docs-setup
```
