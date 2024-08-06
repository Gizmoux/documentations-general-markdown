# Manipulations de chaînes de caractères

## Méthodes

### charAt()

La méthode charAt() renvoie le caractère placé à la position donnée.

const str = "Le Reacteur";
const char = str.charAt(0);

console.log(char); // affichera "L"
Il existe une autre manière d'accéder à un caractère dans une chaîne :

const str = "Le Reacteur";
const char = str[0];

console.log(char); // affichera "L"

// ⚠️ Contrairement aux tableaux, cette méthode ne permet pas de supprimer ou modifier un caractère d'une chaîne.

### indexOf()

La méthode indexOf() renvoie le premier indice pour lequel on trouve un élément donné dans une chaîne de caractères. Si l'élément cherché n'est pas présent dans la chaîne de caractères, la méthode renverra -1.

const str = "Le Reacteur";
const num = str.indexOf("e");

console.log(num); // affichera 1 car le premier "e" est placé en position 1

### replace()

La méthode replace() remplace une partie de la chaîne de caractères et renvoie la nouvelle chaîne. Seule la première occurence est remplacée.

const str = "Le Reacteur";
const newStr = str.replace("Le", "Bienvenue au"); // remplacera "Le" par "Bienvenue au"

console.log(newStr); // affichera "Bienvenue au Reacteur"

### slice()

La méthode slice() extrait une partie d'une chaîne de caractères.

const str = "Le Reacteur";
const newStr = str.slice(3, 8); // extrait du caractère placé en position 3, au 8 exclu
// en l'absence du deuxième indice, les caractères seront extraits jusqu'au dernier

console.log(newStr); // affichera "React"

### substring()

La méthode substring() extrait une partie d'une chaîne de caractères.

let str = "Le Reacteur";
newStr = str.substring(3, 8); //extrait du caractère placé en position 3, au 8 exclu
// en l'absence du deuxième indice, les caractères seront extraits jusqu'au dernier

console.log(newStr); // affichera "React"
📌 Les méthodes slice() et substring() sont équivalentes, mais il existe quelques différences entre elles. Pour en savoir plus : https://stackoverflow.com/questions/2243824/what-is-the-difference-between-string-slice-and-string-substring

### toLowerCase()

La méthode toLowerCase() retourne une chaîne de caractères en minuscules.

let str = "Le Reacteur";
str = str.toLowerCase();

console.log(str); // affichera "le reacteur"

### toUpperCase()

La méthode toUpperCase() retourne une chaîne en caractères en majuscules.

let str = "Le Reacteur";
str = str.toUpperCase();

console.log(str); // affichera "LE REACTEUR"

### trim()

La méthode trim() permet de retirer les blancs (espaces, tabulations) en début et en fin de chaîne.

let str = " Le Reacteur ";
str = str.trim();

console.log(str);

### split()

La méthode split() permet de créer un tableau à partir d'une chaine de caractères.

const str = "How are you doing today?";
const res = str.split(" ");

// res vaut --> ['How', 'are', 'you', 'doing', 'today?']

const name = "Le Reacteur";
const res = str.split("");

// res vaut --> ['L', 'e', ' ', 'R', 'e', 'a', 'c', 't', 'e', 'u', 'r']

# Modifier une chaîne de caractères

En JavaScript, certaines modifications ne sont pas directement possibles sur une chaîne de caractères (remplacer une lettre par une autre par exemple). Cependant, il est possible d'utiliser une chaîne de caractères pour en créer une nouvelle qui sera différente.

let oldStr = "hello";
let newStr = "";

for (let i = 0; i < oldStr.length; i++) {
if (i === 0) {
newStr = newStr + oldStr[i].toUpperCase(); // autre syntaxe : newStr += oldStr[i].toUpperCase();
} else {
newStr = newStr + oldStr[i]; // autre syntaxe : newStr += oldStr[i];
}
}

console.log(newStr); // Hello

# Parcourir une chaîne de caractères

Pour afficher chaque lettre d'un texte, vous pouvez incrémenter un index qui accèdera à chacun des caractères.

const name = "Le Reacteur";
for (let i = 0; i < name.length; i++) {
console.log(name[i]);
// autre manière possible :
// console.log(name.charAt(i));
}
Affichage du terminal :

L
e

R
e
a
c
t
e
u
r
