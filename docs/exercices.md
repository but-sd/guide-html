# Exercices

## Fichiers de base pour les exercices

- [index.html](./exercices-js/index.html)
- [style.css](./exercices-js/style.css)

## Exercices Js

### Ajouter du texte à l'élément h1

Afin de récupérer l'élément h1, on peut utiliser la méthode `document.querySelector` qui permet de récupérer un élément en fonction de son sélecteur CSS. Dans notre cas, on peut utiliser le sélecteur `h1` pour récupérer l'élément h1.

Il est aussi possible d'utiliser la méthode `document.getElementById` qui permet de récupérer un élément en fonction de son id. Dans notre cas, on peut utiliser l'id `title` pour récupérer l'élément h1. La méthode `document.getElementById` est plus rapide que la méthode `document.querySelector`, car elle ne parcourt pas tout le document. On peut aussie utiliser la méthode `document.querySelector` avec le sélecteur `#title` pour récupérer l'élément h1.

Une fois l'élément récupéré, on peut modifier son contenu avec la propriété `innerText`. Le signe `+=` permet d'ajouter du texte à la fin du contenu de l'élément.

=== "JS"

    ```js
    document.querySelector("h1").innerText += " from JS";
    // ou
    document.querySelector('#title').innerText += ' from JS';
    // ou
    document.getElementById('title').innerText += ' from JS';
    ```

=== "HTML"

    ```html
    <h1 id='title'>Hello world 🤖</h1>
    ```

### Changer la couleur de l'élément h1

De la même manière que pour ajouter du texte à l'élément h1, on peut utiliser la propriété `style.color` pour changer la couleur de l'élément h1.
On a accès à toutes les propriétés CSS de l'élément via la propriété `style`. 

On peut donc modifier toutes les propriétés CSS de l'élément. Il suffit de remplacer le tiret `-` par la majuscule suivante. Par exemple, la propriété `background-color` devient `backgroundColor`. 

=== "JS"

    ```js
    document.getElementById('title').style.color = 'red';
    ```

### Ajouter un élément h2 juste après l'élément h1

Pour créer un élément, on peut utiliser la méthode `document.createElement` qui permet de créer un élément en fonction de son nom. Dans notre cas, on peut utiliser le nom `h2` pour créer un élément h2. On a ensuite accès à toutes les propriétés de l'élément via la variable `h2`.

Pour ajouter un élément à la suite d'un autre élément, on peut utiliser la méthode `after` qui permet d'ajouter un élément après un autre élément. Dans notre cas, on peut utiliser la méthode `after` sur l'élément h1 pour ajouter l'élément h2 après l'élément h1.

=== "JS"

    ```js
    // Add a h2 element under the h1
    const h2 = document.createElement("h2");
    h2.id = "sous-titre";
    h2.innerText = "Welcome to the javascript world";
    document.querySelector("h1").after(h2);
    ```
### Ajouter un élément h3 avec l'heure actuelle juste aprés l'élément h2

L'objet Date permet de récupérer la date et l'heure actuelle. La méthode `toLocaleTimeString` permet de récupérer l'heure au format local.

Pour mettre à jour l'heure toutes les secondes, on peut utiliser la méthode `setInterval` qui permet d'exécuter une fonction toutes les secondes. Dans notre cas, on peut utiliser la méthode `setInterval` pour mettre à jour le contenu de l'élément h3 toutes les secondes. 

Le premier paramètre de la méthode `setInterval` est une fonction qui sera exécutée toutes les secondes. Le deuxième paramètre est le nombre de millisecondes entre chaque exécution de la fonction.

=== "JS"

    ```js
    // Add a h3 element with the current time just after the h2
    const h3 = document.createElement("h3");
    h3.innerText = new Date().toLocaleTimeString();
    document.querySelector("#sous-titre").after(h3);

    // Change the time every second
    setInterval(() => {
        document.querySelector("h3").innerText = new Date().toLocaleTimeString();
    }, 1000);
    ```

### Supprimer le premier élément de la liste et en ajouter un nouveau à la fin

La balise ul contient deux balises li. Pour supprimer le premier élément de la liste, on peut utiliser la méthode `remove` sur le premier élément de la liste. Pour ajouter un élément à la fin de la liste, on peut utiliser la méthode `append` sur la liste.

=== "JS"

    ```js
    // Remove the first element of the list and add a new one at the end
    const list = document.querySelector("ul");
    list.firstElementChild.remove();
    const newLi = document.createElement("li");
    newLi.innerText = "Item 3";
    list.append(newLi);
    ```

=== "HTML"

    ```html
    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
    </ul>
    ```

### Changer la couleur de l'élément caption du tableau lorsque la souris passe dessus

Il est possible d'ajouter des écouteurs d'événements sur les éléments du DOM. Dans notre cas, on peut ajouter un écouteur d'événement sur l'élément caption du tableau pour détecter lorsque la souris passe dessus, et changer la couleur de l'élément caption.

De la même manière, on peut ajouter un écouteur d'événement pour détecter lorsque la souris sort de l'élément caption, et changer la couleur de l'élément caption.

=== "JS"

    ```js
    const caption = document.querySelector("caption");
    // Change the color of the caption element when the mouse is over it
    caption.addEventListener("mouseover", () => {
        caption.style.color = "red";
    });

    // Change the color of the caption element when the mouse is out of it
    caption.addEventListener("mouseout", () => {
        caption.style.color = "black";
    });
    ```

### Ajouter des boutons pour faire bouger l'image et le tableau

Afin de faire bouger l'image et le tableau, on peut ajouter des classes CSS à un élément. Pour cela, on peut utiliser la méthode `classList.add` qui permet d'ajouter une classe à un élément, et la méthode `classList.remove` qui permet de supprimer une classe d'un élément.

Le comportement étant le même quelque soit l'élément, on peut créer une fonction qui permet de faire bouger un élément, et une fonction qui permet d'arrêter de faire bouger un élément. Il suffit de passer l'élément en paramètre de la fonction.

On ajoute ensuite des écouteurs d'événements sur les boutons pour faire bouger l'image et le tableau.

=== "JS"

    ```js
    /**
     * Shake an element
     * @param {*} element 
     */
    const shake = (element) => {
        // only shake if the element is not already shaking
        if (!element.classList.contains("shake")) {
            console.log("Shake the element", element);
            element.classList.add("shake");
        }
    }

    // Unshake an element
    const unshake = (element) => {
        // only unshake if the element is shaking
        if (element.classList.contains("shake")) {
            console.log("Unshake the element", element);
            element.classList.remove("shake");
        }
    }

    // add a button to shake the image after the image
    const buttonShakeImage = document.createElement("button");
    buttonShakeImage.innerText = "Shake the image";
    document.querySelector("img").after(buttonShakeImage);
    buttonShakeImage.addEventListener("click", () => {
        shake(document.querySelector("img"));
    });

    // add a button to remove the shake class after the new button
    const buttonUnShakeImage = document.createElement("button");
    buttonUnShakeImage.innerText = "Stop shaking the image";
    buttonShakeImage.after(buttonUnShakeImage);
    buttonUnShakeImage.addEventListener("click", () => {
        unshake(document.querySelector("img"));
    });

    // add a button to shake the table
    const buttonShakeTable = document.createElement("button");
    buttonShakeTable.innerText = "Shake the table";
    document.querySelector("table").after(buttonShakeTable);
    buttonShakeTable.addEventListener("click", () => {
        shake(document.querySelector("table"));
    });

    // add a button to remove the shake class
    const buttonUnshakeTable = document.createElement("button");
    buttonUnshakeTable.innerText = "Stop shaking the table";
    buttonShakeTable.after(buttonUnshakeTable);
    buttonUnshakeTable.addEventListener("click", () => {
        unshake(document.querySelector("table"));
    });
    ```

=== "CSS"
    
    ```css
    .shake {
        animation: shake 0.5s;
    }

    @keyframes shake {
        0% {
            transform: translate(0, 0);
        }

        25% {
            transform: translate(5px, 5px);
        }

        50% {
            transform: translate(0, 0);
        }

        75% {
            transform: translate(-5px, -5px);
        }

        100% {
            transform: translate(0, 0);
        }
    }
    ```

### Récupérer des données depuis un serveur et les afficher dans le tableau

Pour récupérer des données depuis un serveur, on peut utiliser la méthode `fetch` qui permet de faire une requête HTTP. La méthode `fetch` renvoie une promesse qui contient la réponse du serveur. 

Une fois la réponse récupérée, on peut vérifier si la réponse est valide. Si la réponse n'est pas valide, on peut afficher un message d'erreur. Si la réponse est valide, on peut récupérer les données de la réponse avec la méthode `json` qui renvoie une promesse qui contient les données de la réponse.

Dans le cas où la promesse est rejetée, on peut afficher un message d'erreur, dans cet exemple on affiche le message d'erreur dans le tableau.

Les données récupérées étant une liste d'utilisateurs, on peut ajouter une ligne dans le tableau pour chaque utilisateur. Pour cela, on peut utiliser la méthode `forEach` qui permet d'exécuter une fonction pour chaque élément d'un tableau. Dans notre cas, on peut utiliser la méthode `forEach` pour ajouter une ligne dans le tableau pour chaque utilisateur.

=== "JS"

    ```js
    // fetch the data from the server
    fetch("https://jsonplaceholder.typicode.com/users").then((response) => {
        console.log("Response", response);

        if(!response.ok) {
            if(response.status === 404)
                throw new Error("The server responded with a 404 error");
            else
                throw new Error("The server responded with an error");

        }else {
            return response.json();
        }
    }).then((users) => {
        console.log("Users", users);
        // add a new row for each user
        users.forEach((user) => {
            const tr = document.createElement("tr");
            const td1 = document.createElement("td");
            td1.innerText = user.name;
            const td2 = document.createElement("td");
            td2.innerText = user.username;
            const td3 = document.createElement("td");
            td3.innerHTML = '<a href="mailto:' + user.email + '">' + user.email + '</a>';
            // td3.innerHTML = `<a href="mailto:${user.email}">${user.email}</a>`;
            tr.appendChild(td1);
            tr.appendChild(td2);
            tr.appendChild(td3);
            document.querySelector("tbody").appendChild(tr);
        });
    }).catch((error) => {
        console.log("Error", error);
        // add a row with error message
        const tr = document.createElement("tr");
        const td = document.createElement("td");
        td.innerText = error.message;
        tr.appendChild(td);
        document.querySelector("tbody").appendChild(tr);

    });
    ```