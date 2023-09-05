# Javascript

Le javascript est un langage de programmation qui permet de rendre les pages web dynamiques. Il permet d'ajouter des fonctionnalités aux pages web.

## Syntaxe

Le javascript est composé de variables, de fonctions et d'objets.

```javascript
// Variable
let name = 'John';

// Fonction
function sayHello(name) {
  console.log(`Hello ${name}`);
}

// Objet
const person = {
  name: 'John',
  age: 30,
  sayHello: function() {
    console.log(`Hello ${this.name}`);
  }
}
```

### Variables

Les variables permettent de stocker des valeurs. Il existe plusieurs types de variables :

- Les variables de type string
- Les variables de type number
- Les variables de type boolean
- Les variables de type array
- Les variables de type object

### Fonctions

Les fonctions permettent d'exécuter des instructions. Il existe plusieurs types de fonctions :

- Les fonctions déclarées
- Les fonctions anonymes
- Les fonctions fléchées

#### Fonctions déclarées

```javascript
function sayHello(name) {
  console.log(`Hello ${name}`);
}
```

#### Fonctions anonymes

```javascript
const sayHello = function(name) {
  console.log(`Hello ${name}`);
}
```

#### Fonctions fléchées


```javascript
const sayHello = (name) => {
  console.log(`Hello ${name}`);
}
```

Les trois syntaxes ci-dessus sont équivalentes. Elles permettent d'afficher "Hello John" dans la console. 

```javascript
sayHello('John');
```

Il est possible de retourner une valeur avec le mot clé `return`.

```javascript
function add(a, b) {
  return a + b;
}

const result = add(1, 2);
console.log(result); // 3
```

### Objets

Les objets permettent de stocker des données. Il existe plusieurs types d'objets :

- Les objets littéraux
- Les objets instanciés

#### Objets littéraux

```javascript
const person = {
  name: 'John',
  age: 30,
  sayHello: function() {
    console.log(`Hello ${this.name}`);
  }
}
```

#### Objets instanciés

```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  sayHello() {
    console.log(`Hello ${this.name}`);
  }
}

const person = new Person('John', 30);
```

## DOM

Le DOM (Document Object Model) est une interface de programmation qui permet de manipuler les éléments html. Il permet d'ajouter, de modifier et de supprimer des éléments html.

### Sélectionner un élément

Il existe plusieurs méthodes pour sélectionner un élément html :

- `document.getElementById()`
- `document.getElementsByClassName()`
- `document.getElementsByTagName()`
- `document.querySelector()`

#### document.getElementById()

```html
<h1 id="title">Titre</h1>
```

```javascript
const title = document.getElementById('title');
```

#### document.getElementsByClassName()

```html
<h1 class="title">Titre</h1>
```

```javascript
const title = document.getElementsByClassName('title');
```

#### document.getElementsByTagName()

```html
<h1>Titre</h1>
```

```javascript
const title = document.getElementsByTagName('h1');
```

#### document.querySelector()

```html
<h1 id="title">Titre</h1>
```

```javascript
const title = document.querySelector('#title');
```

### Modifier un élément

Il existe plusieurs propriétés pour modifier un élément html :

- `innerHTML`
- `innerText`
- `textContent`
- `style`

#### innerHTML

```html
<h1 id="title">Titre</h1>
```

```javascript
const title = document.getElementById('title');
title.innerHTML = 'Nouveau titre';
```

#### innerText

```html
<h1 id="title">Titre</h1>
```

```javascript
const title = document.getElementById('title');
title.innerText = 'Nouveau titre';
```

#### textContent

```html
<h1 id="title">Titre</h1>
```

```javascript
const title = document.getElementById('title');
title.textContent = 'Nouveau titre';
```

La différence entre `innerText` et `textContent` est que `innerText` ne prend pas en compte les styles css.

#### style

On accède à l'ensemble des propriétés css avec la propriété `style`. On peut modifier les propriétés css avec cette propriété.

```html
<h1 id="title">Titre</h1>
```

```javascript
const title = document.getElementById('title');
title.style.color = 'red';
```

### Ajouter un élément

Il existe plusieurs méthodes pour ajouter un élément html :

- `document.createElement()`
- `document.createTextNode()`
- `document.appendChild()`
- `document.insertBefore()`






