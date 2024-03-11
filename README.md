# Projet TresJS

Ce projet utilise TresJS, une bibliothèque pour créer des applications 3D avec Vue.js.

## Installation du projet

Pour installer les dépendances du projet, exécutez la commande suivante :

```sh
npm install
```

## Compilation et rechargement à chaud pour le développement

Pour compiler et recharger l'application en mode développement, exécutez la commande suivante :

```sh
npm run dev
```

## Compilation et minification pour la production

Pour compiler et minifier l'application pour la production, exécutez la commande suivante :

```sh
npm run build
```

## Structure du projet

Le projet contient deux fichiers principaux : `App.vue` et `Astronaut.vue`.

### App.vue

`App.vue` est le composant principal de l'application. Il importe `TresCanvas` de `@tresjs/core`, `OrbitControls` de `@tresjs/cientos` et `Astronaut` de `./components/Astronaut.vue`.

Il utilise `TresCanvas` pour créer un canvas 3D, `TresPerspectiveCamera` pour définir la caméra, `OrbitControls` pour permettre à l'utilisateur de contrôler la caméra, et `Astronaut` pour afficher un modèle 3D d'un astronaute.

### Astronaut.vue

`Astronaut.vue` est un composant qui affiche un modèle 3D d'un astronaute. Il utilise `useGLTF` de `@tresjs/cientos` pour charger le modèle 3D à partir d'un fichier `.gltf`, et `useAnimations` pour utiliser les animations incluses dans le fichier `.gltf`.

Il utilise une `ref` pour stocker l'action actuelle et la jouer.

## Styles

Les styles sont définis dans `App.vue`. Ils définissent la taille de l'application pour qu'elle occupe toute la fenêtre du navigateur.

## Note

Veuillez noter que les chemins vers les fichiers de modèles 3D et les animations peuvent varier en fonction de la structure de votre projet. Assurez-vous de les mettre à jour en conséquence.