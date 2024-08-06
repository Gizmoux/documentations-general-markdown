# setTimeout

La fonction setTimeout() permet d'appeler une fonction après X millisecondes.

```js
const showSomething = () => {
	console.log('Ce message a été affiché après 3 secondes');
};

setTimeout(showSomething, 3000);
console.log('Avant les 3 secondes');
```

# setInterval()

La méthode setInterval() appelle une fonction ou évalue une expression à des intervalles déterminés (en millisecondes).

```js
const say = str => {
	console.log(str);
};

setInterval(() => {
	say('Hello');
}, 1000); // 1000 ms = 1 seconde
```

La méthode setInterval() continuera d'appeler la fonction jusqu'à ce que clearInterval() soit appelée ou que la fenêtre soit fermée (si la fonction est exécutée depuis une page Web).

Pour utiliser clearInterval(), il faut assigner la méthode setInterval() à une variable.

let counter = 0;
const say = str => {
console.log(str);
if (counter === 5) {
clearInterval(repeat);
} else {
counter++;
}
};
let repeat = setInterval(() => {
say("Hello");
}, 1000);
