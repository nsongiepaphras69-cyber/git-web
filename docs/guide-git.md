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

## Justification de mon organisation Git

J’ai initialisé le projet sur la branche `main`, conformément à l’énoncé, puis séparé le travail dans des branches dédiées :

- `feature-app` pour développer la page HTML et son design CSS ;
- `docs-setup` pour rédiger la documentation ;
- `docs-correction` pour actualiser les instructions de lancement ;
- `chore-gitignore` pour compléter les exclusions des fichiers locaux et temporaires.

Cette organisation permet d’examiner les modifications avant leur intégration dans la branche principale.

J’ai séparé les changements en commits ciblés : structure HTML, design CSS, documentation et configuration. Les messages décrivent leur objectif avec des préfixes comme `feat:`, `style:`, `docs:` et `chore:`.

J’ai utilisé les Pull Requests pour présenter les différences et les vérifier avant la fusion dans `main`.

Pour synchroniser `feature-app`, j’ai utilisé `git merge main`. Cette méthode conserve les commits existants et permet de retrouver la fusion dans l’historique.

Aucun conflit de contenu nécessitant une résolution manuelle n’a été constaté pendant cette fusion. L’ouverture de l’éditeur de message de commit était une étape de confirmation de la fusion.

Enfin, le tag `v1.0.0` sert à identifier la version livrée du projet. Il permet de retrouver les fichiers correspondant à cette version.
