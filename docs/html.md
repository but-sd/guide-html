

# HTML

Le HTML (**H**yper**T**ext **M**arkup **L**anguage) est un langage de balisage. Il permet de structurer et de mettre en forme le contenu d'une page web. 

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

Une balise est un élément qui permet de structurer et de mettre en forme le contenu d'une page web. Elle est composée d'un nom et de deux chevrons. Le HTML n'est pas case sensitive. Cela signifie que les balises peuvent être écrites en majuscules ou en minuscules.

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

```html
<p>Paragraphe 1</p>
<div>
  <p>
    Paragraphe 2
    <span>Span</span>
    <br/> <!-- Saut de ligne -->
  </p>
</div>
```

Un commentaire permet d'ajouter un texte qui ne sera pas interprété par le navigateur. Il est composé de `<!--` et de `-->`. Ainsi, on peut ajouter des commentaires dans le code HTML pour le rendre plus lisible. Attention toute fois, ces commentaires seront visibles dans le code source de la page web. Il ne faut donc pas y ajouter d'informations sensibles.

## Attributs

Un attribut est un élément qui permet de modifier le comportement ou l'apparence d'une balise. Il est composé d'un nom et d'une valeur.

```html
<balise attribut="valeur"></balise>
```

Par exemple la balise `<a>` permet de créer un lien hypertexte. Elle possède un attribut `href` qui permet de définir l'URL de destination du lien.

```html
<a href="https://google.com">Lien vers Google</a>
```

Certains attributs sont obligatoires. Par exemple, l'attribut `href` est obligatoire pour la balise `<a>`. D'autres attributs sont optionnels. Par exemple, l'attribut `alt` est optionnel pour la balise `<img>`.

```html
<img src="image.jpg" alt="Image">
```

Certains attributs sont booléens. Cela signifie qu'ils n'ont pas de valeur. Ils sont utilisés pour activer ou désactiver une fonctionnalité. Par exemple, l'attribut `disabled` permet de désactiver un élément. L'attribut `checked` permet de cocher une case à cocher.

```html
<input type="text" disabled>
<input type="checkbox" checked>
```
## Attributs d'accessibilité

- `alt` : définit un texte alternatif pour une image.
- `tabindex` : définit l'ordre de tabulation.
- `aria-*` : définit un attribut ARIA.
- role : définit le rôle d'un élément.

ARIA (**A**ccessible **R**ich **I**nternet **A**pplications) est un ensemble d'attributs qui permettent d'améliorer l'accessibilité d'une page web. Ils permettent de décrire le contenu d'une page web. Ils sont utilisés par les technologies d'assistance comme les lecteurs d'écran. Ils permettent également d'améliorer le référencement d'une page web.

De la même façon le `rôle` d'un élément permet lui aussi d'améliorer l'accessibilité d'une page web. Il permet de décrire le rôle d'un élément (bouton, lien, liste, etc...).

```html
    
```html
<img src="image.jpg" alt="Image">
<input type="text" tabindex="1">
<input type="text" tabindex="2">

<div role="button" aria-pressed="false">Bouton</div>
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

Ce site web est responsive. Vous constaterez que la mise en page change en fonction de la taille de l'écran. Par exemple la table des matières est affichée en permanence sur un écran large. Elle est cachée par défaut sur un écran plus petit. Elle peut être affichée en cliquant sur le bouton `Table des matières`.

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
- [et bien d'autres](https://developer.mozilla.org/fr/docs/Web/HTML/Element)

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

**Balises de texte**

Les balises de texte permettent de définir le style d'un texte.

- `<strong>` : définit un texte important.
- `<em>` : définit un texte mis en emphase.
- `<mark>` : définit un texte marqué.
- `<small>` : définit un texte de taille réduite.
- `<del>` : définit un texte supprimé.

**Balises de formulaire**

Les balises de formulaire permettent de créer des formulaires.

- `<form>` : définit un formulaire.
- `<input>` : définit un champ de saisie.
- `<textarea>` : définit une zone de texte multiligne.
- `<button>` : définit un bouton.
- `<select>` : définit une liste déroulante.
- `<option>` : définit une option dans une liste déroulante.
- `<label>` : définit un label pour un champ de saisie.
- `<fieldset>` : définit un groupe de champs de saisie.
- `<legend>` : définit une légende pour un groupe de champs de saisie.

**Balises multimédia**

Les balises multimédia permettent d'ajouter des médias à une page web.

- `<img>` : définit une image.
- `<audio>` : définit un fichier audio.
- `<video>` : définit un fichier vidéo.
- `<source>` : définit une source externe pour un fichier audio ou vidéo.

**Balises de programmation**

Les balises de programmation permettent d'ajouter du code à une page web.

- `<script>` : définit un script.
- `<style>` : définit des styles CSS.
- `<link>` : définit un lien vers une ressource externe.

La balise `<script>` permet d'ajouter du code JavaScript à une page web. Elle est composée d'un attribut `src` qui permet de définir l'URL du fichier JavaScript. Elle peut également contenir du code JavaScript directement dans la balise.

```html
<script src="script.js"></script>
<script>
  console.log('Hello world!');
</script>
```

La balise `<style>` permet d'ajouter du code CSS à une page web. Elle peut contenir du code CSS directement dans la balise.

```html
<style>
  h1 {
    color: red;
  }
</style>

<h1>Titre</h1>
```

La balise `<link>` permet de lier une ressource externe à une page web. Elle est composée d'un attribut `rel` qui permet de définir le type de ressource. Elle est également composée d'un attribut `href` qui permet de définir l'URL de la ressource.

Elle peut être utilisée pour lier une feuille de style CSS à une page web. 
Elle peut également être utilisée pour lier une police de caractère à une page web, lorsque la police de caractère n'est pas disponible sur l'appareil de l'utilisateur. La police de caractère sera alors téléchargée et installée sur l'appareil de l'utilisateur.

Les polices de caractères par défaut sont définies par le navigateur. Elles peuvent être différentes d'un navigateur à l'autre. Il existe tout de même quelques polices de caractères qui sont installées sur la plupart des appareils. Par exemple les polices de caractères `Arial`, `Helvetica`, `Times New Roman`. Il est possible de définir plusieurs polices de caractères dans une règle CSS. La première police de caractère sera utilisée si elle est disponible sur l'appareil de l'utilisateur. Sinon la deuxième police de caractère sera utilisée si elle est disponible sur l'appareil de l'utilisateur. Et ainsi de suite.

Elle est généralement utilisée dans la balise `<head>`.

```html
<head>
    <link rel="stylesheet" href="style.css">
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
</head>
```

```html
<link rel="stylesheet" href="style.css">
```

## Installation browser-sync

```json
module.exports = {
  files: ["**/*.{html,css,js}"],
  server: {
    baseDir: "."
  }
};
```

```json
{
  "scripts": {
    "start": "browser-sync start --config bs-config.js"
  },
  "devDependencies": {
    "browser-sync": "^2.29.3"
  }
}
```
