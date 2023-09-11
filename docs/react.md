# Introduction à React

## Introduction

React est une librairie JavaScript développée par Facebook et Instagram. Elle permet de créer des interfaces utilisateurs interactives et dynamiques. Elle est utilisée par de nombreux sites web et applications, comme Facebook, Instagram, Netflix, Airbnb, Uber, etc.

React est une librairie JavaScript, et non un framework. Cela signifie qu'elle ne fournit pas de structure ou de méthodologie pour organiser votre code. Elle ne fournit pas non plus de fonctionnalités pour gérer les requêtes HTTP, les routes, etc. Elle se concentre uniquement sur la création d'interfaces utilisateurs.

React est une librairie open source, et est donc gratuite. Elle est distribuée sous licence MIT.

## Pourquoi utiliser React ?

React est une librairie très populaire, et est utilisée par de nombreux sites web et applications. Elle est très appréciée par les développeurs, et est donc un atout pour votre CV.

React est également très performant. Il est conçu pour être rapide, et pour gérer efficacement les mises à jour de l'interface utilisateur. Il est également très flexible, et peut être utilisé pour créer des interfaces utilisateurs simples ou complexes.

React est également très populaire auprès des développeurs, et dispose donc d'une grande communauté. Il existe de nombreux tutoriels, articles, vidéos, etc. pour vous aider à apprendre React.

## Comment fonctionne React ?

React utilise un DOM virtuel pour gérer les mises à jour de l'interface utilisateur. Le DOM virtuel est une représentation du DOM dans la mémoire. Il est plus rapide que le DOM réel, car il n'est pas directement lié au navigateur. Lorsqu'une mise à jour de l'interface utilisateur est effectuée, React compare le DOM virtuel et le DOM réel, et met à jour le DOM réel uniquement lorsque cela est nécessaire.

React utilise également un système de composants. Un composant est une partie de l'interface utilisateur qui peut être réutilisée. Il peut s'agir d'un bouton, d'un champ de saisie, d'une liste, etc. Un composant peut être composé d'autres composants. Par exemple, un composant de liste peut être composé de composants de ligne.

## Comment apprendre React ?

React est une librairie JavaScript, et il est donc nécessaire d'avoir des connaissances de base en JavaScript pour l'utiliser. Si vous ne connaissez pas JavaScript, vous pouvez apprendre les bases de JavaScript sur [Codecademy](https://www.codecademy.com/learn/introduction-to-javascript).

Une fois que vous avez des connaissances de base en JavaScript, vous pouvez apprendre React sur [Codecademy](https://www.codecademy.com/learn/react-101). Vous pouvez également consulter la [documentation officielle](https://reactjs.org/docs/getting-started.html) de React.

## JSX

JSX est une extension de syntaxe pour JavaScript. Il permet d'écrire du code HTML dans des fichiers JavaScript. Il est utilisé par React pour décrire l'interface utilisateur.

Voici un exemple de JSX :

```jsx
const element = <h1>Hello, world!</h1>;
```

JSX est facultatif, et vous pouvez utiliser JavaScript pur pour décrire l'interface utilisateur. Cependant, JSX est très populaire, et est donc utilisé par la plupart des développeurs React.

## Composants

Un composant est une partie de l'interface utilisateur qui peut être réutilisée. Il peut s'agir d'un bouton, d'un champ de saisie, d'une liste, etc. Un composant peut être composé d'autres composants. Par exemple, un composant de liste peut être composé de composants de ligne.

Voici un exemple de composant :

```jsx
function Button(props) {
  return <button>{props.label}</button>;
}
```

Ce composant est une fonction qui renvoie un bouton. Il prend un objet `props` en paramètre, qui contient les propriétés du composant. Dans cet exemple, le composant prend une propriété `label`, qui est utilisée comme étiquette du bouton.

Voici un exemple d'utilisation de ce composant :

```jsx
<Button label="Click me" />
```

Ce composant est utilisé comme une balise HTML. Il prend une propriété `label`, qui est utilisée comme étiquette du bouton.

Les composants peuvent également être définis comme des classes. Voici un exemple de composant défini comme une classe :

```jsx
class Button extends React.Component {
  render() {
    return <button>{this.props.label}</button>;
  }
}
``` 

Ce composant est une classe qui étend la classe `React.Component`. Il définit une méthode `render()` qui renvoie un bouton. Il utilise la propriété `label` de la classe pour définir l'étiquette du bouton.

Voici un exemple d'utilisation de ce composant :

```jsx
<Button label="Click me" />
```

Ce composant est utilisé comme une balise HTML. Il prend une propriété `label`, qui est utilisée comme étiquette du bouton.
Un composant peut être composé d'autres composants. Voici un exemple de composant composé d'autres composants :

```jsx
function List(props) {
  return (
    <ul>
      <ListItem label="Item 1" />
      <ListItem label="Item 2" />
      <ListItem label="Item 3" />
    </ul>
  );
}
```

Ce composant est une fonction qui renvoie une liste. Il utilise le composant `ListItem` pour définir les éléments de la liste.

Voici un exemple d'utilisation de ce composant :

```jsx
<List />
```

Ce composant est utilisé comme une balise HTML. Il ne prend pas de propriété. Il utilise le composant `ListItem` pour définir les éléments de la liste. Les composants React commencent par une lettre majuscule, ce qui permet de les distinguer des balises HTML.

**Classes ou fonctions ?**

Les composants peuvent être définis comme des classes ou des fonctions. Les classes sont plus flexibles, et peuvent être utilisées pour créer des composants plus complexes. Les fonctions sont plus simples, et peuvent être utilisées pour créer des composants plus simples.

## État

L'état est un objet qui contient les données d'un composant. Il peut être utilisé pour stocker des données qui changent au fil du temps.

Voici un exemple d'état :

```jsx
class Counter extends React.Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
  }

  render() {
    return <p>{this.state.count}</p>;
  }
}
```

Cet état est un objet qui contient une propriété `count`. Cette propriété est utilisée pour stocker le nombre d'éléments de la liste. Elle est initialisée à `0` dans le constructeur du composant.

Voici un exemple d'utilisation de cet état :

```jsx
<Counter />
```

Cet état est utilisé comme une balise HTML. Il ne prend pas de propriété. Il utilise la propriété `count` de l'état pour afficher le nombre d'éléments de la liste.

L'état peut être mis à jour à l'aide de la méthode `setState()`. Voici un exemple de mise à jour de l'état :

```jsx
class Counter extends React.Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
  }

  render() {
    return (
      <div>
        <p>{this.state.count}</p>
        <button onClick={() => this.setState({ count: this.state.count + 1 })}>+</button>
        <button onClick={() => this.setState({ count: this.state.count - 1 })}>-</button>
      </div>
    );
  }
}
```

## Cycle de vie

Le cycle de vie est une série d'étapes qui se produisent lorsqu'un composant est créé, mis à jour ou supprimé. Il peut être utilisé pour exécuter du code à des moments précis du cycle de vie d'un composant.

Voici un exemple de cycle de vie :

```jsx
class Counter extends React.Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
  }

  componentDidMount() {
    console.log('Component did mount');
  }

  componentDidUpdate() {
    console.log('Component did update');
  }

  componentWillUnmount() {
    console.log('Component will unmount');
  }

  render() {
    return <p>{this.state.count}</p>;
  }
}
```

## Affichage conditionnel

L'affichage conditionnel est une technique qui permet d'afficher un élément uniquement si une condition est remplie. Il peut être utilisé pour afficher un élément uniquement si un état est rempli.

Voici un exemple d'affichage conditionnel :

```jsx
class Counter extends React.Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
  }

  render() {
    return (
      <div>
        {this.state.count > 0 && <p>{this.state.count}</p>}
        <button onClick={() => this.setState({ count: this.state.count + 1 })}>+</button>
        <button onClick={() => this.setState({ count: this.state.count - 1 })}>-</button>
      </div>
    );
  }
}
```

Dans cet exemple, le composant `Counter` affiche un élément `<p>` uniquement si l'état `count` est supérieur à `0`. La balise `<p>` est affichée uniquement si la condition `this.state.count > 0` est remplie.

Il est aussi possible d'utiliser une condition pour afficher un composant ou un autre. Voici un exemple d'affichage conditionnel :

```jsx
function IsLogged(props) {
  if (props.isLogged) {
    return <p>Welcome back!</p>;
  } else {
    return <p>Please log in.</p>;
  }
}
```

## Listes

Une liste est un ensemble d'éléments. Elle peut être utilisée pour afficher une liste d'éléments.

Voici un exemple de liste :

```jsx
class List extends React.Component {
  constructor(props) {
    super(props);
    this.state = { items: ['Item 1', 'Item 2', 'Item 3'] };
  }

  render() {
    return (
      <ul>
        {this.state.items.map(item => <li>{item}</li>)}
      </ul>
    );
  }
}
```

Dans cet exemple, le composant `List` affiche une liste d'éléments. La liste est affichée à l'aide de la méthode `map()`. La méthode `map()` prend une fonction en paramètre, qui est appelée pour chaque élément de la liste. La fonction prend un élément en paramètre, et renvoie un élément de la liste.

La fonction map est une fonction JavaScript standard, et peut être utilisée pour afficher une liste d'éléments.