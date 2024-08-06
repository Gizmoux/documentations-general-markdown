# L'objet Date

Pour créer et manipuler des dates en JavaScript, on utilise l'objet Date.

### new Date()

<!-- Le code suivant permet d'obtenir un objet "date" qui indique l'heure (heure UTC) et la date actuelle : -->

```js
const date = new Date();

console.log(date); // 2020-04-08T09:29:50.947Z
Pour obtenir un objet "date" à une date donnée :

// const date = new Date(year, month, day, hours, minutes, seconds, milliseconds)

const date = new Date(2019, 0, 15, 9, 30);
// ⚠️ 0 est le mois de janvier, 11 est le mois de décembre
// Si certaines données sont manquantes, elles sont considérées comme étant à 0

console.log(date); // 2019-01-15T08:30:00.000Z
//  ⚠️ on obtient l'heure UTC
// 📌 L'objet Date accepte plusieurs formats, notamment :

const date1 = new Date("July 17, 2019 16:30:00");
const date2 = new Date("2019-07-17T16:30:00");
const date3 = new Date(2019, 6, 17);
const date4 = new Date(2019, 6, 17, 16, 30, 0);
Date()
// Le code suivant renvoie l'heure et la date actuelle sous forme d'une chaîne de caractères (on remarque l'absence du constructeur "new") :

const date = Date();

console.log(date); // Wed Apr 08 2020 11:31:57 GMT+0200 (GMT+02:00)
Date.now()
// La méthode Date.now() retourne le nombre de millisecondes depuis le 1 janvier 1970, 00:00:00 UTC :

const date = Date.now();

console.log(date); // 1586338534130
// Pour savoir à quelle date et quelle heure correspond un nombre de millisecondes :

const date = new Date(1586338534130);

console.log(date); // 2020-04-08T09:35:34.130Z
// 📌 L'heure UTC (Coordinated Universal Time)
// L'heure UTC est une heure de référence internationale. En France métropolitaine, à l'heure d'hiver, on ajoute +1h00 à l'heure UTC, et +2h00 lorsque nous sommes à l'heure d'été.

getDate()
// La méthode getDate() retourne le jour du mois pour la date spécifiée. La valeur de retour sera comprise entre 1 et 31.

const birthday = new Date("April 08, 2020");

const date = birthday.getDate();

console.log(date); // 8
getDay()
// La méthode getDay() retourne le jour de la semaine pour la date spécifiée. La valeur de retour sera comprise entre 0 (pour dimanche) et 6 (pour samedi).

const birthday = new Date("April 08, 2020");

const day = birthday.getDay();

console.log(day); // 3
// Le 8 avril 2020 était donc un mercredi
getFullYear()
// La méthode getFullYear() retourne l'année pour la date spécifiée.

const birthday = new Date("April 08, 2020");

const year = birthday.getFullYear();

console.log(year); // 2020
getMonth()
// La méthode getMonth() retourne le mois pour la date spécifiée. La valeur de retour sera comprise entre 0 (pour janvier) et 11 (pour décembre).

const birthday = new Date("April 08, 2020");

const month = birthday.getMonth();

console.log(month); // 3
getTime()
// La méthode getTime() renvoie le nombre de millisecondes écoulées depuis le 1 janvier 1970, 00:00:00 UTC, pour une date donnée :

const date = new Date("July, 14, 2000");

const time = date.getTime();
console.log(time); // 963525600000
```
