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
