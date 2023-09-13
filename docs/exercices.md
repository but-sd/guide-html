# Exercices

## Exercices Js

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">

    <title>Hello World in HTML</title>
    <link rel="stylesheet" href="./styles.css">
</head>
<body>
    <h1>Hello world 🤖</h1>
    <p>
        This is a basic HTML page, with a few elements. For instance, this is a paragraph. With a link to
        <a href="https://www.w3schools.com/html/" target="_blank">W3Schools</a>.
        Another link for css explanation<a href="https://www.w3schools.com/css/" target="_blank">W3Schools CSS</a>.
    </p>
    <p>
        And a random image with style: <img src="https://picsum.photos/200" alt="Random image" class="circle">
    </p>
    A list of items:

    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
    </ul>

    A table with some data:

    <table>
        <caption>People</caption>
        <thead>
            <tr>
                <th>Name</th>
                <th>User name</th>
                <th>Email</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Leanne Graham</td>
                <td>Bret</td>
                <td>
                    <a href="mailto:leanne.graham@google.com">
                        leanne.graham@google.com
                    </a>
                </td>
            </tr>
            <tr>
                <td>Ervin Howell</td>
                <td>Antonette</td>
                <td>
                    <a href="mailto:ervin.howell@google.com">
                        ervin.howell@google.com
                    </a>
                </td>
            </tr>
        </tbody>
    </table>

    <p>
        We can check that the html is well formed using the <a href="https://validator.w3.org/#validate_by_upload"
            target="_blank">W3C validator</a>.
    </p>

    <script src="./script.js"></script>
</body>
```

1. Ajouter du texte à l'élément h1
2. Changer la couleur de l'élément h1
3. Ajouter un élément h2 juste après l'élément h1
4. Ajouter un élément h3 avec l'heure actuelle juste aprés l'élément h2
5. Supprimer le premier élément de la liste et en ajouter un nouveau à la fin
6. Changer la couleur de l'élément caption du tableau lorsque la souris passe dessus
7. Ajouter des boutons pour faire boujer l'image et le tableau
8. Récupérer des données depuis un serveur et les afficher dans le tableau


<!-- **Solution**

<details>

<summary>Cliquez ici pour voir la solution</summary>

1. Ajouter du texte à l'élément h1

```html
<h1 id='title'>Hello world 🤖</h1>
```

```js
document.querySelector("h1").innerText += " from JS";
// ou
document.querySelector('#title').innerText += ' from JS';
// ou
document.getElementById('title').innerText += ' from JS';
```

2. Changer la couleur de l'élément h1

```html
<h1 id='title'>Hello world 🤖</h1>
```

```js
document.querySelector("h1").style.color = "red";
// ou
document.querySelector('#title').style.color = 'red';
// ou
document.getElementById('title').style.color = 'red';
```

3. Ajouter un élément h2 juste après l'élément h1

```js
// Add a h2 element under the h1
const h2 = document.createElement("h2");
h2.id = "sous-titre";
h2.innerText = "Welcome to the javascript world";
document.querySelector("h1").after(h2);
```

4. Ajouter un élément h3 avec l'heure actuelle juste aprés l'élément h2

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

5. Supprimer le premier élément de la liste et en ajouter un nouveau à la fin

```js
// Remove the first element of the list and add a new one at the end
const list = document.querySelector("ul");
list.firstElementChild.remove();
const newLi = document.createElement("li");
newLi.innerText = "Item 3";
list.append(newLi);
```

6. Changer la couleur de l'élément caption du tableau lorsque la souris passe dessus

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

7. Ajouter des boutons pour faire boujer l'image et le tableau

=== "Javascript"

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
```

```js
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

8. Récupérer des données depuis un serveur et les afficher dans le tableau

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
</details> -->