---
title: Fiche de référence Markdown
description: Cette fiche de référence Markdown donne un aperçu rapide de tous les éléments de la syntaxe Markdown.
pubDate: 2025-01-18
tags:
  - astro
  - markdown
---

Cette fiche de référence Markdown donne un aperçu rapide de tous les éléments de la syntaxe Markdown. Elle ne peut pas couvrir tous les cas particuliers, donc si vous avez besoin de plus d'informations sur l'un de ces éléments, reportez-vous aux guides de référence pour la [syntaxe de base](https://www.markdownguide.org/basic-syntax/) et la [syntaxe étendue](https://www.markdownguide.org/extended-syntax/).

## Syntaxe de base

Ce sont les éléments décrits dans le document de conception original de John Gruber. Toutes les applications Markdown prennent en charge ces éléments.

### Titre

# H1

## H2

### H3

### Gras

**bold text**

### Italique

_italicized text_

### Bloc de citation

> blockquote

### Liste ordonnée

1. First item
2. Second item
3. Third item

### Liste non ordonnée

- First item
- Second item
- Third item

### Code

`code`

### Règle horizontale

---

### Lien

[Markdown Guide](https://www.markdownguide.org)

### Image

![alt text](https://www.markdownguide.org/assets/images/tux.png)

## Syntaxe étendue

Ces éléments étendent la syntaxe de base en ajoutant des fonctionnalités supplémentaires. Toutes les applications Markdown ne prennent pas en charge ces éléments.

### Tableau

| Syntaxe   | Description |
| --------- | ----------- |
| Header    | Title       |
| Paragraph | Text        |

### Bloc de code encadré

```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

### Note de bas de page

Voici une phrase avec une note de bas de page. [^1]

[^1]: Ceci est la note de bas de page.

### Barré

~~The world is flat.~~

### Liste de tâches

- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media
