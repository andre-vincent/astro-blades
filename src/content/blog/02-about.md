---
title: À propos de ce modèle
description: Cette fiche de référence Markdown donne un aperçu rapide de tous les éléments de la syntaxe Markdown.
pubDate: 2025-01-17
tags:
  - astro
  - template
---

Ce modèle repose sur quelques principes clés pour mon propre site :

- Je voulais un site Web basique avec un blog à auteur unique.
- Le site devait inclure des éléments accessibles et utilisables.
- Les systèmes complexes devaient être évités au profit de solutions plus simples.
- Je devais pouvoir comprendre facilement ce que je vois.

Le résultat est un modèle Astro qui limite fortement l'utilisation des classes CSS et qui maximise l'utilisation du HTML sémantique.

## Fonctionnalités

### Pico CSS

Le modèle utilise Pico CSS pour bénéficier de paramètres par défaut agréables avec des mises en page réactives. Il a besoin de presque aucune classe pour bien fonctionner, ce qui est l'objectif.

J'utilise la version SASS de Pico CSS pour supprimer les styles inutiles et réduire la taille finale du CSS.

### HTML sémantique

Ce modèle cherche à maximiser l'utilisation des balises HTML sémantiques plutôt que des éléments génériques comme `<div>`. Le HTML sémantique présente des avantages importants :

1. Le code source HTML est plus facile à lire et à écrire.
2. Le HTML sémantique est recommandé par rapport aux attributs ARIA pour l'accessibilité.
3. Le style sémantique fonctionne bien avec Pico CSS.

### Résultat statique

Le modèle essaie de ne pas aller au-delà du HTML statique. Pas de JavaScript côté client, pas de cookies.

### Packages NPM limités

Le modèle limite le nombre de packages NPM à ceux que j'ai trouvés utiles, tels que :

- Prettier, pour la lisibilité du code
- SASS et Pico CSS, pour éviter de se préoccuper du CSS
- L'intégration RSS d'Astro

### Fonctionnalités de confort

Le modèle inclut quelques fonctionnalités qui semblaient une bonne idée, même si elles ne sont pas aussi minimales :

- Un flux RSS stylisé
- Une image Open Graph pour les réseaux sociaux
- Des étiquettes de publication et des pages de tags
- Un modèle de publication et de page
- Des imports absolus dans `tsconfig.json`

## Développements futurs

Il y a d'autres choses que j'aimerais implémenter :

- [] Déterminer où placer la page des tags.
- [] Ajouter une collection de contenu `pages`.
- [] Ajouter un composant de lien de navigation
- [] Mieux organiser les composants Astro
- [] Intégrer des icônes
- [] Plus... ?

## Remerciements

- Le modèle [Astro Pico](https://github.com/san-ghun/astro-pico), pour m'avoir fait découvrir Pico CSS.
- Le modèle [Astronaut](https://github.com/stevefrenzel/astro-naut), pour m'avoir aidé à apprendre de meilleurs principes de réactivité.
