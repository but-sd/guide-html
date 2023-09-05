# Cascade Style Sheets

Le css est un langage de style qui permet de mettre en forme des pages web. Il est utilisé pour définir les couleurs, les polices, les positions, les tailles, les différents effets, etc.

## Syntaxe

Le css est composé de sélecteurs et de déclarations. Les sélecteurs permettent de cibler les éléments html et les déclarations permettent de définir les propriétés des éléments ciblés.

```css
/* Sélecteur */
h1 {
  /* Déclaration */
  color: red;
}
```

### Sélecteurs

Il existe plusieurs types de sélecteurs :

- Les sélecteurs de type
- Les sélecteurs de classe
- Les sélecteurs d'id
- Les sélecteurs d'attributs
- Les sélecteurs de pseudo-classes
- Les sélecteurs de pseudo-éléments

**Sélecteurs de type**

Les sélecteurs de type permettent de cibler les éléments html.

```css
/* Cible tous les éléments h1 */
h1 {
  color: red;
}
```

Ici, tous les éléments h1 auront une couleur rouge.

**Sélecteurs de classe**

Les sélecteurs de classe permettent de cibler les éléments html qui ont une classe.

```css
/* Cible tous les éléments qui ont la classe "title" */
.title {
  color: red;
}
```

Ici, tous les éléments qui ont la classe "title" auront une couleur rouge. La classe est définie dans le fichier html.

```html 
<h1 class="title">Titre</h1>
```

**Sélecteurs d'id**

Les sélecteurs d'id permettent de cibler les éléments html qui ont un id.

```css
/* Cible l'élément qui a l'id "title" */
#title {
  color: red;
}
```

L'id est défini dans le fichier html.

```html
<h1 id="title">Titre</h1>
```

**Sélecteurs d'attributs**

Les sélecteurs d'attributs permettent de cibler les éléments html qui ont un attribut.

```css
/* Cible l'élément qui a l'attribut "href" */
[href] {
  color: red;
}
```

L'attribut est défini dans le fichier html.

```html
<a href="https://google.com">Lien</a>
```

**Sélecteurs de pseudo-classes**

Les sélecteurs de pseudo-classes permettent de cibler les éléments html qui ont un état particulier.

```css
/* Cible l'élément qui est survolé */
a:hover {
  color: red;
}
```

Les états possibles sont : hover, active, focus, etc... Voir la liste des états possibles [ici](https://developer.mozilla.org/fr/docs/Web/CSS/Pseudo-classes).


Ici, l'élément a aura une couleur rouge lorsqu'il sera survolé.

**Sélecteurs de pseudo-éléments**

Les sélecteurs de pseudo-éléments permettent de cibler des parties d'éléments html.

```css
/* Cible la première ligne de l'élément */
p::first-line {
  color: red;
}
```

Les parties possibles sont : first-line, first-letter, etc... Voir la liste des parties possibles [ici](https://developer.mozilla.org/fr/docs/Web/CSS/Pseudo-%C3%A9l%C3%A9ments).

Ici, la première ligne de l'élément p aura une couleur rouge.

### Déclarations

Il existe plusieurs façons d'ajouter du css à une page web. Selon la méthode utilisée, le css sera plus ou moins prioritaire.

L'ordre de priorité est le suivant :

1. Les styles inline (attribut style)
2. Les styles internes (balise style)
3. Les styles externes (fichier css)

En fonction du besoin, il est possible d'utiliser une méthode plutôt qu'une autre. 

L'avantage d'utiliser un fichier css est que le code est séparé du code html. Cela permet de mieux organiser son code et de le rendre plus lisible. Il est également possible de réutiliser le même fichier css pour plusieurs pages web. Le fichier css sera alors lié à chaque page web. Cela permet de ne pas avoir à réécrire le même code css pour chaque page web. De plus le fichier css sera mis en cache par le navigateur. Cela permettra d'améliorer les performances du site web. 

Il est possible d'utiliser le navigateur pour tester du css. Il suffit d'ouvrir la console du navigateur et de cliquer sur l'onglet "Elements". Il est ensuite possible de modifier le css directement dans le navigateur. Cela permet de tester rapidement du css sans avoir à modifier le code html ou le code css.

#### Dans le fichier html

Il est possible d'ajouter du css directement dans le fichier html.

```html
<style>
  h1 {
    color: red;
  }
</style>

<h1>Titre</h1>
```

#### Dans un fichier css

Il est possible d'ajouter du css dans un fichier css.

```css
h1 {
  color: red;
}
```

Il faut ensuite lier le fichier css au fichier html.

```html
<link rel="stylesheet" href="style.css">
```

#### Dans un attribut style

Il est possible d'ajouter du css dans un attribut style.

```html
<h1 style="color: red;">Titre</h1>
```

## Couleurs

Il existe plusieurs façons de définir une couleur en css.

**Couleurs nommées**

```css
h1 {
  color: red;
}
```

**Couleurs hexadécimales**

```css
h1 {
  color: #ff0000;
}
```

**Couleurs rgb**

```css
h1 {
  color: rgb(255, 0, 0);
}
```

**Couleurs hsl**

```css
h1 {
  color: hsl(0, 100%, 50%);
}
```

## Unités

Il existe plusieurs unités en css. Relative ou absolue, chaque unité a ses avantages et ses inconvénients.

Les unités relatives sont dynamiques. Elles sont relatives à un autre élément. Elles permettent de créer des interfaces fluides et responsives. Elles sont donc à privilégier. Les types d'unités relatives sont : em, rem, %, vw, vh, vmin, vmax.

Les unités absolues sont fixes. Les types d'unités absolues sont : px, cm, in, pt.

## Media queries

Les media queries permettent de définir des règles css en fonction de la taille de l'écran. Cela permet de créer des interfaces fluides et responsives.

```css
/* Définit la couleur du titre en fonction de la taille de l'écran */
@media (max-width: 600px) {
  h1 {
    color: red;
  }
}
```

## Frameworks

Les frameworks permettent de créer des interfaces fluides et responsives. Ils sont composés de composants qui peuvent être réutilisés. Ils permettent de gagner du temps. Ils permettent également de créer des interfaces fluides et responsives en réduisant le nombre de lignes de code css.

Il existe plusieurs frameworks. Les plus connus sont : Bootstrap, Tailwind, Material UI, etc. Dans le cadre du développement de l'application marvel, le framework Material UI sera utilisé. C'est aussi ce framework qui est utilisé pour ce site web.

Material UI est un framework proposé par Google. Il est basé sur le [Material Design](https://material.io/design). 
