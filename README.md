# Turbo Ville

Un jeu de conduite en ville ouverte, en 3D, pour apprendre à coder : récupère un colis, réponds à une question de programmation en fonçant vers la bonne balise, sème la police et améliore ta voiture.

**Jouer en ligne :** https://dedeee2.itch.io/turbo-ville

## Fonctionnalités

- Ville 3D ouverte avec circulation, piétons, cycle jour/nuit et pluie
- Missions racontées par trois personnages (Lola, Max, l'inspecteur Roux), chacun lié à une famille de langages
- 17 langages : Python, JavaScript, TypeScript, HTML, CSS, SQL, C, C++, Java, Rust, Go, PHP, Bash, Swift, Kotlin, Ruby, Lua
- Questions à choix et questions « à compléter », avec difficulté croissante
- Les questions ratées reviennent plus tard ; bilan de fin de partie
- Drift, nitro, courses éclair, police, garage (moteur, pneus, nitro, peinture)
- Sauvegarde locale (argent, améliorations, maîtrise, statistiques) : aucune donnée n'est envoyée

## Lancer en local

Le jeu tient dans un seul fichier. Ouvre `index.html` dans un navigateur (connexion internet requise pour charger three.js depuis un CDN).

## Héberger avec GitHub Pages

1. Dépose le projet dans un dépôt GitHub.
2. Dans **Settings → Pages**, choisis la branche `main` et le dossier `/ (root)`.
3. Le jeu sera disponible à `https://tahiadz00.github.io/turbo-ville/`.

## Ajouter des questions

Les questions sont dans l'objet `QB` de `index.html`. Chaque question suit ce format :

```js
['énoncé', ['réponse A', 'réponse B', 'réponse C'], indexDeLaBonneRéponse, 'explication']
```

Ajoute un cinquième élément `1` pour marquer une question difficile. Les questions « à compléter » (avec `___`) sont dans l'objet `QC`.

## Statistiques (optionnel)

La variable `TRACK_URL` est vide par défaut. Si tu utilises un service d'analyse respectueux de la vie privée, tu peux y mettre son adresse pour compter les parties lancées.

## Crédits et licence

Le code du jeu est sous licence MIT (voir `LICENSE`). Le rendu 3D utilise [three.js](https://threejs.org/) (licence MIT), chargé depuis cdnjs.
