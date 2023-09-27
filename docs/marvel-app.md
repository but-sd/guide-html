## Outillage du projet

Sur la branche develop configurer le projet pour permettre le live reload avec browser-sync. [Voir la documentation](../outils).

## Développement de 2 fonctionnalités

### Gestion du style

Créer une branche feature pour le développement de la fonctionnalité style, `feature/style`

Ajouter un fichier `style.css` et ajouter le lien vers ce fichier dans le fichier `index.html`.

=== "index.html"
    ```html
    <link rel="stylesheet" href="style.css" />
    ```
=== "style.css"
    ```css
    body{
        background-color: #f0f0f0;
        font-family: monospace;
        font-size: 1.5em;
    }
    ```

### Gestion du contenu

Créer une branche feature pour le développement de la fonctionnalité contenu, `feature/characters`

Ajouter un fichier `characters.js` et ajouter le lien vers ce fichier dans le fichier `index.html`.

=== "index.html"
    ```html
    <script src="characters.js"></script>
    ```

=== "characters.js"
    ```js
    console.log('Chargement de la liste des personnages...');

    // retrieve data from json file
    fetch('../data/characters.json')
    .then((response) => {
        console.log(response);
        return response.json();
    })
    .then((characters) => {
        console.log(characters);
        // add a ul element to the body after the h1 element
        let ul = document.createElement('ul');
        document.querySelector("h1").after(ul);

        // loop through the characters array
        characters.forEach((character) => {
            console.log(character);
            // create a li element
            let li = document.createElement('li');
            // set the text of the li element to the name of the character
            li.innerText = character.name;
            // append the li element to the ul element
            ul.append(li);
        });

        // add a h2 element to the body after the ul element with the number of characters
        let h2 = document.createElement('h2');
        h2.innerText = `Number of characters: ${characters.length}`;
        ul.after(h2);

    }).catch((err) => {
        console.log(err);
    });
    ```

=== "characters.json"

    ```json
    [
        {
            "id": "1009175",
            "name": "Beast"
        },
        {
            "id": "1009220",
            "name": "Captain America"
        },
        {
            "id": "1009268",
            "name": "Deadpool"
        },
        {
            "id": "1010743",
            "name": "Groot"
        },
        {
            "id": "1009351",
            "name": "Hulk"
        },
        {
            "id": "1009368",
            "name": "Iron Man"
        },
        {
            "id": "1009664",
            "name": "Rocket Raccoon"
        },
        {
            "id": "1009662",
            "name": "Silver Surfer"
        },
        {
            "id": "1009697",
            "name": "Thanos"
        },
        {
            "id": "1009663",
            "name": "Thor"
        },
        {
            "id": "1009718",
            "name": "Wolverine"
        }
    ]
    ```
## Merge des 2 fonctionnalités

Merger les 2 branches feature dans la branche develop. Pour cela on peut utiliser la commande `git merge`, ou utiliser github pour créer une pull request.

Une pull request permet de demander à un autre développeur de vérifier le code avant de le merger dans la branche develop. La pull request permet de discuter du code, de demander des modifications, etc. On peut également utiliser une pull request pour vérifier que le code est conforme aux règles de développement de l'entreprise, exécuter des tests automatiques, etc.

Générer un conflit lors du merge des 2 branches. Résoudre le conflit en gardant le code des 2 branches.



