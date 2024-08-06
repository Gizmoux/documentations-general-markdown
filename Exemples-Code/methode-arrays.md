# Les tableaux (arrays)

Les tableaux permettent de stocker des listes de variables.
Pour manipuler un tableau, nous avons accès à un ensemble de méthodes.

Méthodes (liste non exhaustive)

### push()

La méthode push() ajoute un ou plusieurs éléments à la fin d'un tableau et retourne la nouvelle taille du tableau.

const numbers = [1, 2, 3];
numbers.push(4); // Notez que nous pouvons tout à fait ajouter des éléments dans un tableau déclaré avec `const`.

console.log(numbers); // [1, 2, 3, 4]

numbers.push(5, 6, 7);

console.log(numbers); // [1, 2, 3, 4, 5, 6, 7]

### indexOf()

La méthode indexOf() renvoie le premier indice pour lequel on trouve un élément donné dans un tableau. Si l'élément cherché n'est pas présent dans le tableau, la méthode renverra -1.

const a = [2, 9, 9];
a.indexOf(2); // retournera 0 car 2 est à la position 0 du tableau
a.indexOf(7); // retournera -1 car 7 est introuvable dans le tableau

// Autre exemple avec une condition
const names = ["Farid", "Xavier", "Alexis", "Brice", "Corinne"];
if (names.indexOf("Charlie") === -1) {
// si l'élément "Charlie" n'existe pas dans le tableau, alors...
}

### pop()

La méthode pop() supprime le dernier élément d'un tableau et retourne cet élément. Cette méthode modifie la longueur du tableau.

const mesPoissons = ["riri", "fifi", "loulou", "picsou"];

const popped = mesPoissons.pop();

console.log("mesPoissons après : " + mesPoissons); // mesPoissons après : riri, fifi, loulou
console.log("A retiré cet élément : " + popped); // A retiré cet élément : picsou

### shift()

La méthode shift() permet de retirer le premier élément d'un tableau et de renvoyer cet élément. Cette méthode modifie la longueur du tableau.

const a = [1, 2, 3];
const b = a.shift();

console.log(a); // [2, 3]
console.log(b); // 1

### unshift()

La méthode unshift() ajoute un ou plusieurs éléments au début d'un tableau et renvoie la nouvelle longueur du tableau.

const a = [1, 2, 3];
a.unshift(4, 5);

console.log(a); // [4, 5, 1, 2, 3]

### reverse()

La méthode reverse() transpose les éléments d'un tableau : le premier élément devient le dernier et le dernier devient le premier et ainsi de suite.

const a = ["un", "deux", "trois"];
a.reverse();

console.log(a); // ['trois', 'deux', 'un'];

### sort()

La méthode sort() trie les éléments d'un tableau, dans ce même tableau, et renvoie le tableau. Le tri s'effectue par défaut selon les points de code Unicode de la chaine de caractères.

const fruits = ["pommes", "bananes", "Cerises"];
fruits.sort(); // ["Cerises", "bananes", "pommes"];

const scores = [1, 2, 10, 21];
scores.sort(); // [1, 10, 2, 21]
// Attention 10 vient avant 2
// selon l'ordre Unicode

const choses = ["mot", "Mot", "1 Mot", "2 Mots"];
choses.sort(); // ["1 Mot", "2 Mots", "Mot", "mot"]
// En Unicode, les nombres arrivent avant
// les majuscules, qui elles-mêmes arrivent
// avant les minuscules.
sort() pour trier des nombres
const scores = [1, 10, 53, 61, 90];
scores.sort(function(a, b) {
return a - b;
});

### slice()

La méthode slice() renvoie un tableau, contenant une copie d'une portion du tableau d'origine. La portion est définie par un indice de début et un indice de fin (exclu). Le tableau original ne sera pas modifié.

//arr.slice()
//arr.slice(début)
//arr.slice(début, fin)

const fruits = ["Banane", "Orange", "Citron", "Pomme", "Mangue"];
const agrumes = fruits.slice(1, 3);

// fruits vaut --> ["Banane", "Orange", "Citron", "Pomme", "Mangue"]
// agrumes vaut --> ["Orange", "Citron"]

### split()

La méthode split() permet de créer un tableau à partir d'une chaine de caractères.

const str = "How are you doing today?";
const tab1 = str.split(" ");

// tab1 vaut --> ['How', 'are', 'you', 'doing', 'today?']

const name = "Le Reacteur";
const tab2 = name.split("");

// tab2 vaut --> ['L', 'e', ' ', 'R', 'e', 'a', 'c', 't', 'e', 'u', 'r']

### join()

La méthode join() permet d'assembler les éléments d'un tableau pour constituer une chaine de caractères.

const fruits = ["Banane", "Orange", "Citron", "Pomme", "Mangue"];
const sentence = fruits.join(" - ");

// sentence vaut --> "Banane - Orange - Citron - Pomme - Mangue"
