

# HTML

Le HTML (HyperText Markup Language) est un langage de balisage utilisé pour créer des pages web. Il permet de structurer et de mettre en forme le contenu d'une page web.

## Structure d'une page web

La structure minimale d'une page web est composée de 3 balises et d'un doctype:

- `<!DOCTYPE html>` : définit le type de document comme étant un document HTML.
- `<html>` : définit le document comme étant un document HTML.
- `<head>` : définit un ensemble d'informations sur le document.
- `<body>` : définit le corps du document.

```html
<!DOCTYPE html>
<html lang="fr">
  <head>
    <title>Titre</title>
  </head>
  <body>
    <h1>Titre</h1>
    <p>Paragraphe</p>
  </body>
</html>
```

## Balises

Une balise est un élément qui permet de structurer et de mettre en forme le contenu d'une page web. Elle est composée d'un nom et de deux chevrons.

```html
<balise></balise>
```

Une balise peut être :

- une balise ouvrante : `<balise>`
- une balise fermante : `</balise>`
- une balise auto-fermante : `<balise />`

Une balise peut contenir :

- du texte
- d'autres balises

## Attributs

Un attribut est un élément qui permet de modifier le comportement ou l'apparence d'une balise. Il est composé d'un nom et d'une valeur.

```html
<balise attribut="valeur"></balise>
```

Par exemple la balise `<a>` permet de créer un lien hypertexte. Elle possède un attribut `href` qui permet de définir l'URL de destination du lien.

```html
<a href="https://google.com">Lien vers Google</a>
```

## Commentaires

Un commentaire permet d'ajouter un texte qui ne sera pas interprété par le navigateur. Il est composé de `<!--` et de `-->`. Ainsi, on peut ajouter des commentaires dans le code HTML pour le rendre plus lisible. Attention toute fois, ces commentaires seront visibles dans le code source de la page web. Il ne faut donc pas y ajouter d'informations sensibles.

```html
<!-- Commentaire -->
```

## Quelques balises

**HEAD**

La balise `<head>` permet de définir un ensemble d'informations sur le document. Elle contient généralement :

- `<title>` : définit le titre du document.
- `<meta>` : définit des métadonnées sur le document.
- `<link>` : définit un lien vers une ressource externe.
- `<style>` : définit des styles CSS.

La balise <meta> permet de définir des métadonnées sur le document. Elle est composée d'un attribut `name` et d'un attribut `content`. Elle peut être utilisée pour définir l'encodage du document, la description du document, les mots-clés du document, l'auteur du document, le viewport du document... Et son contenu peut être utilisé par les moteurs de recherche pour référencer le document.

La bamise <meta> permet aussi de définir le viewport du document. Le viewport permet de définir la largeur et l'échelle d'un document. Il est utilisé pour rendre un document responsive. Il est composé d'un attribut `name` et d'un attribut `content`. L'attribut `name` doit avoir la valeur `viewport`. L'attribut `content` doit avoir la valeur `width=device-width, initial-scale=1.0`.

Un document Responsive Web Design est un document qui s'adapte à la taille de l'écran de l'appareil sur lequel il est affiché ( ordinateur, tablette, téléphone...). Il est composé de plusieurs points de rupture. Un point de rupture est une taille d'écran à partir de laquelle le document change de mise en page. 

Les outils de développement des navigateurs permettent de simuler un appareil mobile. Par exemple, dans Google Chrome, on peut simuler un appareil mobile en cliquant sur `Toggle device toolbar` dans le menu des outils de développement.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

**BODY**

La balise `<body>` permet de définir le corps du document. Elle peut contenir par exemple :

- `<h1>` : définit un titre de niveau 1.
- `<p>` : définit un paragraphe.
- `<a>` : définit un lien hypertexte.
- `<img>` : définit une image.
- `<ul>` : définit une liste non ordonnée.
- `<ol>` : définit une liste ordonnée.
- `<li>` : définit un élément de liste.
- `<div>` : définit une division ou un conteneur générique.
- `<span>` : définit une section générique.
- `<table>` : définit un tableau.
- [...](https://developer.mozilla.org/fr/docs/Web/HTML/Element)

**Balises sémantiques**

Les balises sémantiques permettent de définir le rôle d'un élément. Elles permettent de structurer le contenu d'une page web. Elles sont utilisées par les moteurs de recherche pour référencer le contenu d'une page web. Elles permettent également d'améliorer l'accessibilité d'une page web.

- `<header>` : définit un en-tête.
- `<nav>` : définit une barre de navigation.
- `<main>` : définit le contenu principal.
- `<section>` : définit une section.
- `<article>` : définit un article.
- `<aside>` : définit un contenu à part.
- `<details>` : définit des détails supplémentaires.
- `<summary>` : définit un résumé.
- `<footer>` : définit un pied de page.