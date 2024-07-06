1. **Qu'est-ce que React ?**

   React est une bibliothèque JavaScript gratuite et open source pour le développement d'interfaces utilisateur, qui utilise des composants pour créer des sorties pour des applications monopages. React a été développé par Facebook (Meta) et est maintenu par une communauté de développeurs.

2. **Énumérez les fonctionnalités importantes de React**

   Les fonctionnalités les plus importantes de React incluent :

   - Facilité d'utilisation
   - Développement rapide
   - Utilisation des composants
   - JSX
   - DOM virtuel
   - Haute performance
   - Liaison de données unidirectionnelle

3. **Où se trouve le référentiel du projet React ?**

   React est un mono-dépôt qui se trouve à l'adresse [https://github.com/facebook/react](https://github.com/facebook/react). Être un mono-dépôt signifie que tout son code et ses autres sources sont stockés au même endroit pour faciliter le développement et la gestion.

4. **Quelle est la version stable actuelle de React ?**

   La version stable la plus récente de React du 14 juin 2022 est la 18.2.0.

5. **Indiquez les différences entre React Native et ReactJS**

   React et ReactJS sont identiques, tandis que React Native est basé sur React. En raison de leurs différences, React est utilisé pour créer des interfaces utilisateur dynamiques et réactives pour les applications Web, tandis que React Native est conçu pour créer des applications mobiles.

6. **Quelle est la différence entre un élément et un composant ?**

   Un élément React est un objet simple et immuable créé pour représenter un nœud DOM. Être immuable signifie qu'il ne peut pas être modifié une fois qu'il a été créé, car il est rendu dans le DOM. Un composant React, en revanche, est mutable et produit une sortie JSX une fois rendu.

7. **Comment créer un composant ?**

   Il existe deux façons de créer un composant dans React :

   - **Composants de fonction**
   - **Composants de classe**

   Comme leur nom l'indique, un composant de fonction est créé à l'aide d'une déclaration de fonction, tandis qu'un composant de classe est créé à l'aide d'une déclaration de classe.

   ```javascript
   // Function component
   function Hello({ message }) {
   	return <h1>{`Function hello, ${message}`}</h1>;
   }

   // Class component
   class Hello extends React.Component {
   	render() {
   		return <h1>{`Class hello, ${this.props.message}`}</h1>;
   	}
   }
   ```

8. **Énumérez les 4 étapes d'un composant React**

   Un composant React subit les 4 étapes suivantes dans son cycle de vie :

   - **Étape initiale** : Construction du composant dans l’état par défaut avec les accessoires initiaux
   - **Phase de montage** : Rendu JSX du composant
   - **Phase de mise à jour** : Modifications de l’état des composants et redessin de l’application
   - **Phase de démontage** : Suppression des composants du DOM

9. **Expliquez ce que signifie un composant d'ordre supérieur**

   Un composant d'ordre supérieur (HOC) est une méthodologie React permettant de créer des composants. Il utilise un composant existant pour en créer un nouveau doté de fonctionnalités supplémentaires. En d'autres termes, un HOC est une fonction qui prend un composant comme argument et renvoie un nouveau composant avec des fonctionnalités supplémentaires.

10. **Quels sont les composants contrôlés et non contrôlés ?**

    - Un composant contrôlé est un composant React qui prend sa valeur via des props et notifie le système de tout changement via des rappels. Il est contrôlé par un composant parent qui gère son état et transmet les valeurs sous forme de props au composant contrôlé.
    - Un composant non contrôlé, en revanche, gère son état et vous devrez interroger le DOM à l'aide de `ref` pour obtenir sa valeur.

11. **Que sont les props dans React ?**

    Les props dans React ne sont qu'une manière simple de dire propriétés, et par cela, vous faites référence aux propriétés d'un composant. Les props sont utilisées pour transmettre des données d'un composant parent à un ou plusieurs composants enfants, et elles sont en lecture seule pour le composant enfant.

12. **Que sont les props.children ?**

    L'attribut `props.children` contient des informations sur tout le contenu d'un composant qui possède une balise d'ouverture et une balise de fermeture. Ces enfants font référence à tous les éléments définis dans le composant actuel et peuvent être un, plusieurs ou aucun.

13. **Pouvez-vous mettre à jour les props dans React ?**

    Non, les props dans React sont descendantes et immuables. Cela signifie qu'un composant peut envoyer toutes les propriétés qu'il souhaite à ses enfants, mais il ne peut pas mettre à jour ses props. Seul son parent peut mettre à jour ses props.

14. **Qu'est-ce que JSX ?**

    JSX signifie JavaScript XML. Il s'agit d'une extension de syntaxe JavaScript qui permet d'écrire du HTML dans le code React. Le navigateur ne comprend pas JSX de toute façon, donc React doit le restituer en code HTML lisible.

15. **Quelle est la différence entre un composant et un élément**

    Un élément est une définition sans état et immuable d'un nœud DOM virtuel. Il contient à la fois un type et une propriété, mais aucune méthode comme un composant. Ce manque de méthodes le rend rapide.

16. **Qu'est-ce qu'un état dans React ?**

    Un état dans React fait référence à un objet intégré dans un composant qui est utilisé pour contenir et gérer les informations sur ce composant. Un état peut changer au fil du temps et déclenchera donc un nouveau rendu de ce composant. Vous devez définir l'état dans la méthode constructeur du composant, sinon le composant devient sans état.

17. **Qu’est-ce qu’un composant sans état ?**

    Un composant React sans état n'a pas d'état. Cela signifie que vous ne pouvez ni définir son état avec la méthode `this.setState()` ni le faire afficher. Un composant sans état peut cependant avoir des propriétés.

18. **Comment mettre à jour un état dans React**

    Vous mettez à jour l'état d'un composant en appelant sa méthode `this.setState()`.

19. **Expliquez le mode strict de React**

    Le mode strict de React est un outil qui aide le développeur à découvrir les problèmes potentiels de l'application en activant des contrôles de niveau plus profond sur les composants et en mettant en évidence davantage d'avertissements. Le mode strict n'est disponible qu'en mode développement.

20. **Que signifie augmenter l'état dans React ?**

    Cela signifie permettre aux composants enfants de partager un état commun de leur parent, car cela rend les choses plus faciles à gérer que si chaque composant enfant gérait individuellement l'état commun.

21. **Comment transmettre des données dans React ?**

    Vous transmettez des données dans React à l'aide de props et de callbacks. Les props de React sont unidirectionnels, ce qui permet aux propriétés de passer uniquement des composants parents à leurs enfants. Pour transmettre des données d'un composant enfant à un parent, vous devez utiliser une fonction de rappel.

22. **Définir Flux dans React**

    Flux est un concept unidirectionnel permettant de diriger le flux de données dans une application. Le fait qu'il soit unidirectionnel signifie que les données ne peuvent passer que des composants parents aux composants enfants. Flux peut également inclure plusieurs magasins de données par application.

23. **Définir Redux dans React**

    Redux est une bibliothèque JavaScript open source utile pour gérer les états complexes d'une application. Elle est indépendante et peut être utilisée dans d'autres frameworks tels qu'Angular. Contrairement à Flux, Redux centralise la gestion des états d'une application, facilitant ainsi la création d'interfaces utilisateur complexes.

24. **Quand faut-il utiliser Redux ?**

    Toutes les applications n'ont pas besoin de Redux. Mais il peut être utile dans les cas suivants :

    - Lorsque vous avez un grand nombre d'états d'application dans votre application
    - Lorsque la logique de votre application est complexe
    - Lorsque votre application dispose d'une base de code volumineuse
    - Lorsque vous devez mettre à jour l'application fréquemment
    - Lorsque de nombreuses personnes travaillent sur l'application

25. **Quelle est la principale différence entre Redux et Flux ?**

    La principale différence entre les deux est que Redux gère toutes les données d'application à partir d'un seul magasin, tandis que vous pouvez avoir plusieurs magasins sous Flux.

26. **Lister les composants de Redux**

    Redux comprend 4 parties principales :

    - **Magasin** : C’est ici que vous stockez l’état de l’application.
    - **Action** : Il s’agit d’événements qui amènent l’application à envoyer des données à la boutique Redux.
    - **Réducteur** : Il s’agit d’une fonction qui accepte l’état actuel de l’application et une action comme arguments, puis renvoie un nouvel état comme résultat.
    - **Middleware** : Cette fonctionnalité permet à un développeur de capturer toutes les actions d’un composant avant qu’elles n’atteignent la fonction de réduction.

27. **Que sont les hooks React ?**

    Les hooks React sont une fonctionnalité des composants de fonction qui vous permettent d'accéder à différentes fonctionnalités de React, telles que les données d'état et les mises à jour de rendu. Il a été introduit dans React 16.8.

28. **Lister les types de Hooks dans React**

    Il existe plus de 15 hooks dans React, à partir des hooks de base comme `useState`, `useEffect` et `useContext` jusqu'aux hooks supplémentaires comme `useCallback`, `useReducer`, `useMemo`, `useRef`, etc.

29. **Que sont les fragments ?**

    Un fragment React est un moyen pratique de regrouper plusieurs éléments enfants dans un composant, sans les ajouter au DOM. Il vous suffit de définir la balise à l'aide de :

    - `<> </>`
    - ou `<Fragment> </>`

    et chargez tous les éléments enfants que vous souhaitez à l'intérieur. La seule différence est que la version abrégée `<>` n'accepte pas les clés et les attributs, alors que la version longue le fait.

30. **Lister les principales méthodes du package react-dom**

    Il s'agit de `createPortal()` pour le rendu des enfants dans un DOM externe et de `flushSync()` pour le vidage des mises à jour. Il existe également les méthodes `render()` et `hydrate()`, qui ont été remplacées par `createRoot()` et `hydrateRoot()` depuis React 18.

31. **Que sont les clés React ?**

    Les clés sont des identifiants uniques qui sont particulièrement utiles pour gérer les listes. Les clés permettent d'identifier facilement les éléments individuels d'une liste et de savoir quand chaque élément a été mis à jour, supprimé ou modifié de quelque manière que ce soit.

32. **Pourquoi les clés React sont-elles importantes ?**

    Les clés sont importantes dans React car elles contribuent au rendu efficace du DOM réel. React est bon car il essaie de minimiser les composants qu'il restitue après un événement, et l'utilisation de clés sur une liste évite à React d'avoir à restituer des listes entières, ce qui peut être un problème avec les grandes listes.

33. **Qu'est-ce qu'un événement dans React ?**

    Un événement est une action dans une application qui provient soit de l'utilisateur, soit du système. Un événement peut aller d'un clic ou d'un appui de souris sur un appareil mobile à un redimensionnement de fenêtre, une pression sur une touche, un glissement, une mise au point, etc.

34. **Expliquez ce que signifie un événement synthétique**

    Un événement synthétique est un wrapper autour des événements natifs d'un navigateur, le problème étant que les différents navigateurs nomment leurs événements différemment. React utilise des événements synthétiques pour éviter le problème de devoir créer plusieurs implémentations et méthodes pour tous les différents navigateurs. De cette façon, React conserve des noms communs pour tous les différents événements du navigateur sous forme d'API unifiée.

35. **Qu'est-ce que Webpack ?**

    Webpack est un système de regroupement de modules utilisé pour combiner et minimiser les fichiers JavaScript et CSS. Il est basé sur Node.js et est utile lorsque vous travaillez avec un grand nombre de fichiers ou d'éléments non codés tels que des images et des polices.

36. **Qu'est-ce que create-react-app ?**

    `Create-react-app` est un outil qui vous aide à créer une application React monopage dans votre environnement Node.js. Il génère tous les fichiers et dossiers dont vous avez besoin pour démarrer une application de base et vous vous en chargez à partir de là. Il nécessite Node version 14.0.0 et npm à partir de la version 5.6.

    L'utilisation est simple :

    ```bash
    npx créer-react-app maNouvelleApp

    cd maNouvelleApp

    démarrage npm
    ```

37. **Pouvez-vous effectuer un rendu côté serveur avec React ?**

    Oui, vous pouvez, même si cela peut demander beaucoup de ressources pour les projets de grande envergure. Le rendu côté serveur est utile car il améliore l'expérience utilisateur et le référencement. Vous aurez besoin d'un environnement Node.js, d'un bundler comme Webpack et d'un framework comme Next.js et Remix pour restituer les applications React au moment de l'exécution. Une solution à l'utilisation intensive des ressources consiste à utiliser un générateur de site statique, tel que Gatsby basé sur Next.js.

38. **Expliquez ce que fait une fonction fléchée**

    Une fonction fléchée est simplement une manière plus courte de définir des fonctions. Il s'agit d'un raccourci ES6 qui remplace :

    ```javascript
    = fonction() avec ()=> .
    ```

    Par exemple :

    ```javascript
    test = fonction(){
      retourner « Ceci est un test » ;
    }
    ```

    alors devient :

    ```javascript
    test = () => {
      retourner « Ceci est un test » ;
    }
    ```

    ou pour les instructions sur une seule ligne :

    ```javascript
    test = () => « Ceci est un test »;
    ```

39. **Qu'est-ce qu'un routeur React ?**

    React Router est une bibliothèque qui fournit des fonctionnalités de routage dans une application React. Elle facilite l'inclusion et l'utilisation de composants de navigation riches, qui peuvent être très utiles pour les projets de grande envergure ou complexes.

40. **Quels sont les principaux avantages de l’utilisation de React Router ?**

    Il crée différents chemins d'URL pour votre application et fournit des valeurs `window.location` et un objet d'historique.

41. **Qu'est-ce que ComponentWillUnmount() ?**

    Il s'agit d'une méthode de composant qui est appelée chaque fois que React est sur le point de détruire le composant. C'est un bon endroit pour nettoyer les éléments, effacer les minuteurs, annuler les requêtes réseau et gérer d'autres problèmes de désinitialisation importants.

42. **Qu'est-ce que The Constructor() ?**

    Le constructeur est la méthode du composant qui est appelée lors de l'initialisation du composant. Il est généralement utilisé pour initialiser les états locaux et pour lier les méthodes de gestion des événements.

43. **Qu'est-ce que le DOM virtuel ?**

    Le DOM virtuel de React est une copie légère du DOM du document HTML réel. Il est utilisé pour une gestion et une mise à jour efficaces des modifications sur le DOM réel.

44. **Quels sont les avantages du DOM virtuel par rapport au DOM réel ?**

    Le DOM virtuel est léger et plus rapide à restituer que le DOM réel, ce qui rend plus efficace le rendu sur le DOM virtuel en premier et ne modifie le DOM réel que lorsque cela est nécessaire. Chaque nœud du DOM réel possède un composant correspondant sur le DOM virtuel, et une fois que des modifications sont apportées à un composant virtuel après le rendu, React sait alors exactement quel nœud HTML réel mettre à jour ou supprimer.

45. **Expliquez le terme « réconciliation » dans React**

    La réconciliation est la méthode de React pour mettre à jour le DOM réel uniquement lorsque cela est nécessaire, en vérifiant les versions mises à jour du DOM virtuel via la comparaison et en mettant à jour uniquement les nœuds exacts qui ont changé sur le DOM réel.

46. **Expliquez le terme Profiler dans React**

    Profiler est un outil React qui permet d'optimiser une application en mesurant le nombre de fois qu'une application s'affiche et le temps nécessaire à chaque composant pour s'afficher. Cela aide le développeur à identifier les parties de l'application qui peuvent nécessiter une optimisation.

47. **Expliquez le terme Contexte dans React**

    Context est une méthode de transmission de données entre composants React à plusieurs niveaux sans avoir à transmettre les données à travers chaque niveau d'imbrication à l'aide de props. Il est préférable de l'utiliser pour un partage facile des données avec de nombreux composants qui n'ont pas besoin de mises à jour constantes, comme les informations sur les thèmes et les données utilisateur. Son inconvénient est qu'il peut rendre la réutilisation des composants difficile.

48. **Expliquez le terme Montage dans React**

    Le montage dans React est le processus consistant à attacher un composant en tant que nœud au DOM. Le démontage est l'inverse.

49. **Expliquez le terme rendu dans React**

    Le rendu est le processus de dessin d'un composant. Il se produit généralement lorsque l'état du composant change et que React doit redessiner l'interface utilisateur. Si un composant est redessiné pendant le rendu, ses composants enfants sont également redessinés.

50. **Expliquez le terme « limite d'erreur » dans React**

    La limite d'erreur fait référence à un composant React qui détecte les erreurs JavaScript de ses composants enfants, enregistre les erreurs et affiche une interface utilisateur de secours à la place des nœuds qui se sont plantés. Les limites d'erreur ont été introduites dans React 16.
