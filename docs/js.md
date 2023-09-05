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

**Fonctions déclarées**

```javascript
function sayHello(name) {
  console.log(`Hello ${name}`);
}
```

**Fonctions anonymes**

```javascript
const sayHello = function(name) {
  console.log(`Hello ${name}`);
}
```

**Fonctions fléchées**

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

**Objets littéraux**

```javascript
const person = {
  name: 'John',
  age: 30,
  sayHello: function() {
    console.log(`Hello ${this.name}`);
  }
}
```

**Objets instanciés**

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

**document.getElementById()**

```html
<h1 id="title">Titre</h1>
```

```javascript
const title = document.getElementById('title');
```

**document.getElementsByClassName()**

```html
<h1 class="title">Titre</h1>
```

```javascript
const title = document.getElementsByClassName('title');
```

**document.getElementsByTagName()**

```html
<h1>Titre</h1>
```

```javascript
const title = document.getElementsByTagName('h1');
```

**document.querySelector()**

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

**innerHTML**

```html
<h1 id="title">Titre</h1>
```

```javascript
const title = document.getElementById('title');
title.innerHTML = '<span>Nouveau titre</span>';
title.innerHTML += '<span>Titre 2</span>';
```

**innerText**

```html
<h1 id="title">Titre</h1>
```

```javascript
const title = document.getElementById('title');
title.innerText = 'Nouveau titre';
```

**textContent**

```html
<h1 id="title">Titre</h1>
```

```javascript
const title = document.getElementById('title');
title.textContent = 'Nouveau titre';
```

La différence entre `innerText` et `textContent` est que `innerText` ne prend pas en compte les styles css.

**style**

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

Par exemple, si on souhaite ajouter un titre dans une div :

```html
<div id="container"></div>
```

```javascript
const container = document.getElementById('container');
const title = document.createElement('h1');
title.innerText = 'Titre';
container.appendChild(title);
```

### Supprimer un élément

Il existe plusieurs méthodes pour supprimer un élément html :

- `document.removeChild()`
- `document.remove()`

Par exemple, si on souhaite supprimer un titre dans une div :

```html
<div id="container">
  <h1 id="title">Titre</h1>
</div>
```

```javascript
const container = document.getElementById('container');
const title = document.getElementById('title');
container.removeChild(title);
```

## Evénements

Les événements permettent d'exécuter une fonction lorsqu'une action est effectuée. Il existe plusieurs types d'événements :

- Les événements de souris
- Les événements de clavier
- Les événements de formulaire
- Les événements de document
- Les événements de fenêtre

### Les événements de souris

- `click`
- `dblclick`
- `mousedown`
- `mouseup`
- `mouseover`
- `mouseout`
- `mousemove`

### Les événements de clavier

- `keydown`
- `keyup`
- `keypress`

### Les événements de formulaire

- `submit`
- `change`
- `focus`
- `blur`

### Les événements de document

- `load`
- `scroll`
- `resize`
- `unload`

### Les événements de fenêtre

- `load`
- `scroll`
- `resize`
- `unload`

### Ajouter un événement

La fonction element.addEventListener() permet d'ajouter un événement à un élément html.

```html
<button id="button">Cliquez ici</button>
```

```javascript
const button = document.getElementById('button');
button.addEventListener('click', function() {
  console.log('Cliquez');
});
```

## Quelques fonctions natives utiles

### Les fonctions de chaîne de caractères

- `charAt()`: retourne le caractère à l'index spécifié
- `concat()`: concatène deux chaînes de caractères
- `includes()`: vérifie si une chaîne de caractères contient une autre chaîne de caractères
- `indexOf()`: retourne l'index de la première occurence d'une chaîne de caractères

**Exemple**

Une fonction qui retourne le caractère à l'index spécifié :

```javascript
const name = 'John';

const character = name.charAt(0);

console.log(character); // Output: J
```

Une fonction qui concatène deux chaînes de caractères :

```javascript
const firstName = 'John';
const lastName = 'Doe';

const fullName = firstName.concat(lastName);

console.log(fullName); // Output: JohnDoe
```

### Les fonctions de date

- `getDate()`: retourne le jour du mois
- `getDay()`: retourne le jour de la semaine

### Les fonctions mathématiques

- `ceil()`: arrondit un nombre à l'entier supérieur
- `floor()`: arrondit un nombre à l'entier inférieur
- `round()`: arrondit un nombre à l'entier le plus proche
- `random()`: retourne un nombre aléatoire entre 0 et 1

**Exemple**

Une fonction qui retourne un nombre aléatoire entre 0 et 10 :

```javascript
const randomNumber = Math.random() * 10;

console.log(randomNumber); // Output: 5.123456789
```

Une fonction qui retourne un nombre aléatoire entre 0 et 10 arrondi à l'entier supérieur :

```javascript
const randomNumber = Math.ceil(Math.random() * 10);

console.log(randomNumber); // Output: 6
```

### Les fonctions de tableau

- `concat()`: concatène deux tableaux
- `filter()`: filtre les éléments d'un tableau
- `find()`: retourne le premier élément d'un tableau qui satisfait une condition
- `forEach()`: exécute une fonction sur chaque élément d'un tableau
- `includes()`: vérifie si un tableau contient une valeur

**Exemple**

Une fonction qui retourne les nombres pairs d'un tableau :

```javascript
const numbers = [1, 2, 3, 4, 5];

const evenNumbers = numbers.filter(function(number) {
  return number % 2 === 0;
});

console.log(evenNumbers); // Output: [2, 4]
```

Une fonction qui retourne le premier nombre pair d'un tableau :

```javascript
const numbers = [1, 2, 3, 4, 5];

const evenNumber = numbers.find(function(number) {
  return number % 2 === 0;
});

console.log(evenNumber); // Output: 2
```

Une fonction qui affiche chaque élément d'un tableau :

```javascript
const numbers = [1, 2, 3, 4, 5];

numbers.forEach(function(number) {
  console.log(number);
});
```

Une fonction qui vérifie si un tableau contient une valeur :

```javascript
const numbers = [1, 2, 3, 4, 5];

const hasNumber = numbers.includes(3);

console.log(hasNumber); // Output: true
```

## Try / Catch

Le try / catch permet de gérer les erreurs. Il permet d'exécuter une instruction et de gérer les erreurs qui peuvent survenir.

```javascript
function callFunction(simulateError = false) {
  if (simulateError){
    throw new Error('Erreur');
  }  
}

try {
  console.log('Hello');
  // Traitement pouvant générant une erreur
  callFunction(false);
  console.log('World');
  callFunction(true);
  console.log('!')
} catch(error) {
  console.log(error);
}
```

## Async / Await

L'async / await permet d'exécuter des instructions de manière asynchrone. Il permet d'attendre le résultat d'une promesse avant d'exécuter une instruction.

Dans l'exemple ci-dessous, la fonction getData() permet de récupérer des données à l'aide de l'API fetch. L'API fetch permet de faire des requêtes HTTP. La fonction getData() est une fonction asynchrone. Elle est composée du mot clé async. Elle permet d'attendre le résultat de la promesse avant d'exécuter la fonction suivante. La fonction getData() est composée du mot clé await. La fonction getData() attend le résultat de la promesse avant d'exécuter la fonction suivante.

```javascript
async function getData() {
  const response = await fetch('https://jsonplaceholder.typicode.com/todos/1');
  const data = await response.json();
  console.log(data);
}

getData();
```

Il est possible de faire la même chose avec la syntaxe suivante :

```javascript
function getData() {
  fetch('https://jsonplaceholder.typicode.com/todos/1')
    .then(function(response) {
      return response.json();
    })
    .then(function(data) {
      console.log(data);
    });
}

getData();
```