## Qu’est-ce que l’asynchrone ?

L'asynchrone fait référence à la capacité d'exécuter des opérations sans bloquer l'exécution du programme. En JavaScript, cela permet de lancer des tâches longues (comme des requêtes réseau) et de continuer à exécuter d'autres parties du code pendant que ces tâches sont en cours. Une fois l'opération asynchrone terminée, elle signale son achèvement via des callbacks, des promesses (Promises) ou des mots-clés comme async/await.

## Comment fonctionne l’Event Loop ?

L'Event Loop est un mécanisme qui permet à JavaScript de réaliser des opérations non bloquantes. Elle fonctionne ainsi :

JavaScript exécute le code synchronously sur la pile d'appels (call stack).
Les tâches asynchrones sont déléguées à l'API Web (par exemple, les timers, les requêtes AJAX).
Une fois terminées, ces tâches passent dans la file d'attente (task queue).
L'Event Loop vérifie si la pile d'appels est vide, et si c'est le cas, elle déplace les tâches de la file d'attente vers la pile d'appels pour les exécuter.

## Qu’est-ce que le hissage (hoisting) ?

Le hissage (hoisting) est le comportement par lequel les déclarations de variables et de fonctions sont déplacées en haut de leur contexte d'exécution (portée) lors de la phase de compilation. Cela signifie que vous pouvez utiliser des variables et des fonctions avant de les déclarer dans le code. Toutefois, seules les déclarations sont hissées, pas les initialisations.

## Qu'est ce que le DOM ? Comment ça marche ?

Le DOM (Document Object Model) est une représentation en mémoire de la structure d'un document HTML ou XML. Il permet aux scripts de manipuler le contenu, la structure et le style des pages web. Le DOM organise le document en une hiérarchie d'objets appelés nœuds (nodes), ce qui permet aux développeurs d'accéder et de modifier des éléments individuels de manière programmée.

## Qu'est-ce qui est plus performant entre un map et un forEach ?

En termes de performance brute, forEach peut être légèrement plus performant que map car il n'a pas besoin de créer un nouveau tableau. map est utile lorsque vous souhaitez transformer chaque élément d'un tableau en un nouveau tableau, tandis que forEach est utilisé pour exécuter une fonction sur chaque élément sans produire un nouveau tableau. Le choix entre les deux dépend souvent du besoin du programme plutôt que des performances.

## Qu'est-ce qu'une fonction IIFE ?

Une IIFE (Immediately Invoked Function Expression) est une fonction en JavaScript qui est définie et immédiatement exécutée. Elle est souvent utilisée pour créer une nouvelle portée afin d'isoler des variables et des fonctions du contexte global. La syntaxe ressemble à ceci :

```bash
(function() {
    // code à exécuter immédiatement
})();
```

## Qu'est-ce qu'une pure function ?

Une pure function (fonction pure) est une fonction qui, pour les mêmes entrées, produit toujours les mêmes sorties et n'a pas d'effets de bord (side effects). Cela signifie qu'elle ne modifie pas l'état externe et ne dépend pas de celui-ci. Les fonctions pures sont prévisibles et plus faciles à tester.

## Qu'est-ce que la programmation fonctionnelle ?

La programmation fonctionnelle est un paradigme de programmation qui traite le calcul comme l'évaluation de fonctions mathématiques. Elle met l'accent sur l'utilisation de fonctions pures, l'immutabilité des données et la réduction des effets de bord. Les concepts clés incluent les fonctions d'ordre supérieur, les expressions lambda, les fermetures (closures) et la composition de fonctions. La programmation fonctionnelle permet de créer un code plus prévisible, modulaire et facile à raisonner.

## Quelle est la différence entre la programmation fonctionnelle et la programmation orientée objet ?

Programmation fonctionnelle :
Se concentre sur les fonctions pures et l'évaluation des expressions.
Utilise l'immutabilité et évite les effets de bord.
Les fonctions d'ordre supérieur et la composition de fonctions sont des concepts clés.
Programmation orientée objet :
Se concentre sur les objets qui contiennent des données et des méthodes.
Utilise des concepts comme l'encapsulation, l'héritage et le polymorphisme.
Les objets peuvent avoir un état mutable et des effets de bord.

## Qu'est-ce que la phase de bouillonnement (bubbling) ?

La phase de bouillonnement (bubbling) est un concept en gestion d'événements DOM où un événement se propage du nœud cible initial vers le haut à travers les ancêtres de ce nœud jusqu'à atteindre l'élément document. Cela permet aux ancêtres de capturer et de réagir aux événements déclenchés par leurs descendants.

## Comment React fonctionne “under the hood” ?

React utilise un algorithme de "diffing" et un "virtual DOM" pour optimiser les mises à jour de l'interface utilisateur. Lorsqu'un changement d'état se produit, React crée un nouvel arbre du virtual DOM, le compare avec l'ancien arbre (diffing), et applique efficacement les différences (reconciliation) au DOM réel. Cela minimise les opérations coûteuses sur le DOM et améliore les performances.

## Comment React Native fonctionne “under the hood” ?

React Native permet de créer des applications mobiles en utilisant des composants React qui se traduisent en composants natifs. Le code JavaScript est exécuté sur un moteur JavaScript (comme Hermes ou V8), et les composants UI sont gérés par des "bridges" qui communiquent entre le JavaScript et les composants natifs via un système de messages asynchrones.

## Comment fonctionnent les closures ?

Une closure est une fonction qui capture les variables de son environnement lexical. En d'autres termes, une closure "ferme" les variables de la portée dans laquelle elle a été créée, permettant ainsi à la fonction de se souvenir de ces variables même lorsque la portée extérieure a cessé d'exister.

## Comment fonctionnent les hooks "under the hood" ?

Les hooks en React fonctionnent en utilisant un système d'indexation des appels de hooks pour chaque composant fonctionnel. Lorsqu'un hook est appelé, React utilise l'index pour retrouver l'état ou les effets associés au composant en cours. Les hooks permettent de gérer l'état, les effets et d'autres fonctionnalités dans les composants fonctionnels sans avoir besoin de classes.

## Qu'est-ce qu'une Promesse (Promise) ?

Une promesse (Promise) est un objet qui représente la terminaison (ou l'échec) éventuelle d'une opération asynchrone et sa valeur résultante. Une promesse peut être dans l'un des trois états suivants :

En attente (pending)
Réussie (fulfilled)
Rejetée (rejected)
Les promesses permettent de chaîner des opérations asynchrones de manière plus lisible et de gérer les erreurs plus facilement.

## Expliquez comment fonctionne async/await et à quoi ça sert ?

async/await est une syntaxe de sucre pour travailler avec des promesses en JavaScript. Une fonction déclarée avec async retourne une promesse et peut utiliser le mot-clé await pour attendre la résolution d'une promesse. Cela permet d'écrire du code asynchrone de manière plus synchrone, rendant le code plus lisible et plus facile à comprendre :

```bash
async function fetchData() {
    try {
        let response = await fetch('url');
        let data = await response.json();
        return data;
    } catch (error) {
        console.error(error);
    }
}
```

## Qu'est-ce que ça veut dire XHR ?

XHR signifie XMLHttpRequest, un objet en JavaScript utilisé pour interagir avec des serveurs. Il permet d'envoyer des requêtes HTTP et HTTPS, de récupérer des données à partir d'URL sans avoir à recharger la page entière. XHR est souvent utilisé pour implémenter des fonctionnalités de type AJAX (Asynchronous JavaScript and XML).

## Qu'est-ce que Webpack ?

Webpack est un module bundler pour les applications JavaScript. Il prend les modules avec des dépendances et les compile en un ou plusieurs bundles statiques qui peuvent être chargés par un navigateur. Webpack peut transformer, emballer, et optimiser des fichiers comme JavaScript, CSS, et images grâce à ses loaders et plugins.

## Qu'est-ce qu'un polyfill ?

Un polyfill est un morceau de code (souvent JavaScript) qui fournit la fonctionnalité que vous attendez qu'un navigateur implémente de manière native. Il permet d'utiliser des fonctionnalités modernes sur des navigateurs plus anciens qui ne les supportent pas encore.

## Qu'est-ce que Docker ?

Docker est une plateforme qui permet de créer, déployer et exécuter des applications dans des conteneurs. Les conteneurs encapsulent une application et ses dépendances, offrant ainsi un environnement cohérent et isolé pour l'exécution. Docker simplifie le déploiement et la gestion des applications, indépendamment de l'environnement sous-jacent.

## Qu'est-ce qu'une architecture MicroServices ?

Une architecture microservices est une approche de développement logiciel où une application est structurée comme un ensemble de services faiblement couplés. Chaque service est responsable d'une fonctionnalité spécifique et peut être développé, déployé et mis à l'échelle indépendamment. Cela permet une plus grande flexibilité et scalabilité.

## Comment fonctionne Redux ?

Redux est une bibliothèque de gestion d'état pour les applications JavaScript. Elle utilise un store unique pour gérer l'état de l'application. Les actions décrivent les changements, et les reducers spécifient comment l'état change en réponse aux actions. Redux suit trois principes clés : un seul store, l'état est en lecture seule, et les changements sont effectués via des fonctions pures appelées reducers.

## Quelle est la différence entre Cordova et React Native ?

Cordova : Utilise des technologies web (HTML, CSS, JavaScript) pour créer des applications mobiles. Le code est exécuté dans une WebView, une vue de navigateur intégrée.
React Native : Utilise React et JavaScript pour construire des composants natifs. Le code JavaScript s'exécute via un bridge qui communique avec les composants natifs, offrant de meilleures performances et une expérience utilisateur plus native.

## Qu'est-ce que Next.js ?

Next.js est un framework React pour le rendu côté serveur (SSR) et la génération de sites statiques (SSG). Il simplifie la création d'applications React avec des fonctionnalités comme le routage basé sur les fichiers, le rendu côté serveur, et l'optimisation des performances.

## Qu'est-ce que Gatsby ?

Gatsby est un générateur de sites statiques basé sur React. Il utilise GraphQL pour récupérer les données et construit des sites web rapides et performants. Gatsby est idéal pour les blogs, les portfolios, et les sites de documentation.

## Avez-vous entendu parlé des nouveautés ES2020 ?

ES2020 (ECMAScript 2020) introduit plusieurs nouvelles fonctionnalités, notamment :

Optional chaining (?.)
Nullish coalescing operator (??)
BigInt
Dynamic import
Promise.allSettled
globalThis
Modules import/export dans les scripts
Qu'est-ce que la coercition en JavaScript ?
La coercition en JavaScript est la conversion automatique ou implicite de valeurs d'un type à un autre. Elle peut être explicite (utilisation de fonctions comme Number(), String()) ou implicite (lorsque des opérateurs comme +, == sont utilisés avec différents types de valeurs).

## Quelles sont les différences entre set et array ?

Set :
Une collection de valeurs uniques.
Ne permet pas les doublons.
Les éléments ne sont pas indexés.
Opérations de recherche et d'insertion plus rapides.
Array :
Une collection de valeurs ordonnées.
Permet les doublons.
Les éléments sont indexés.
Offre plus de méthodes pour manipuler les données.

## Connaissez-vous les styled components ?

Oui, Styled Components est une bibliothèque pour React et React Native qui permet d'utiliser des styles CSS au sein des composants JavaScript. Elle utilise des balises de template littérales pour écrire des styles, offrant ainsi un style encapsulé et dynamique.

## Quelles sont les primitives en JavaScript ? (piège : les symboles sont apparus en ES6 !)

Les primitives en JavaScript incluent :

string
number
boolean
null
undefined
symbol (introduit en ES6)
bigint (introduit en ES2020)

## Quelles sont les nouveautés avec React 17 ?

React 17 introduit des améliorations principalement centrées sur la facilitation des mises à niveau et de l'intégration progressive :

Aucune nouvelle fonctionnalité de rupture majeure : Principalement des changements sous le capot.
Meilleure gestion des événements : Délégation des événements au niveau du conteneur racine.
Compatibilité progressive : Permet l'exécution de plusieurs versions de React sur la même page.
Améliorations des outils de développement : Amélioration de la détection des problèmes de compatibilité et des avertissements.
