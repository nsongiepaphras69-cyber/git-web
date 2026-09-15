# Mon application web

## Présentation

Ce projet pédagogique consiste à créer une petite page web en HTML5
et CSS3 tout en pratiquant le workflow Git et GitHub.

La page comprend un titre, un bouton et une zone d’affichage statique.
Elle n’utilise pas JavaScript : le bouton ne déclenche aucune action.

## Technologies

- HTML5 : structure de la page.
- CSS3 : mise en forme et adaptation aux différentes tailles d’écran.
- Git : gestion des versions.
- GitHub : hébergement du dépôt et revue des modifications.

## Structure du projet

```text
.
├── docs/
│   └── guide-git.md
├── src/
│   ├── css/
│   │   └── style.css
│   └── index.html
├── .gitignore
└── README.md
```

## Lancer l’application

1. Cloner le dépôt en remplaçant l’adresse ci-dessous par son URL réelle :

   ```bash
   git clone https://github.com/nsongiepaphras69-cyber/git-web.git
   ```

2. Ouvrir le dossier cloné.
3. Ouvrir `src/index.html` dans un navigateur.

Aucune installation de dépendances n’est nécessaire.

Tant que la branche `feature-app` n’est pas fusionnée dans `main`,
le code de l’application est disponible sur `feature-app` :

```bash
git switch feature-app
```

Avant de changer de branche, enregistrer les modifications en cours.

## Organisation des branches

- `main` : branche principale destinée à recevoir les modifications validées.
- `feature-app` : développement de la page web.
- `docs-setup` : rédaction de la documentation.

## Guide des commandes

Consulter le [guide Terminal et Git](docs/guide-git.md).
