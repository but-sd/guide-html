## Validation du code HTML

Afin de valider le code HTML, il est possible d'utiliser le validateur du W3C. Il suffit de se rendre sur le site [https://validator.w3.org/](https://validator.w3.org/) et de coller le code HTML à valider dans le champ de texte.

Il est également possible d'ajouter une extension à visual studio code pour valider le code HTML. L'extension s'appelle [W3C Validation](https://marketplace.visualstudio.com/items?itemName=Umoxfo.vscode-w3cvalidation) et est disponible sur le marketplace de visual studio code.

## Live-reload / hot-reload

Afin de faciliter le développement, il est possible d'utiliser des outils qui permettent de recharger automatiquement la page web lorsqu'un fichier est modifié. Cela permet de ne pas avoir à recharger manuellement la page web à chaque modification.

Ces outils sont appelés des *live-reload* ou *hot-reload*. Il s'appuie sur node.js et sont donc à installer via le gestionnaire de paquet npm.

**browser-sync**

Afin d'utiliser browser-sync, il faut installer le paquet npm `browser-sync` en tant que dépendance de développement.

```bash
npm install browser-sync --save-dev
```

Cela va installer le paquet dans le dossier `node_modules` et ajouter une entrée dans le fichier `package.json` pour indiquer que le paquet est une dépendance de développement. 

Nous allons ensuite créer un fichier de configuration pour browser-sync. Ce fichier doit être nommé `bs-config.js` et doit être placé à la racine du projet. Il contient les informations suivantes :

```javascript
module.exports = {
  files: ["**/*.{html,css,js}"],
  server: {
    baseDir: "."
  }
};
```

Enfin, nous allons ajouter une entrée dans le fichier `package.json` pour lancer browser-sync. Il suffit d'ajouter une entrée dans la section `scripts` du fichier `package.json`:

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

Il est ensuite possible de lancer browser-sync en exécutant la commande suivante :

```bash
npm run start
```

