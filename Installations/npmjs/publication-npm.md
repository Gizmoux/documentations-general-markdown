# Publier un Composant React sur npm

Pour créer et publier un composant React sur npm, suivez ces étapes :

## 1. Préparez votre composant

- Assurez-vous que votre composant est autonome et réutilisable.
- Séparez-le dans son propre dossier de projet.

## 2. Initialisez un nouveau projet npm

- Créez un nouveau dossier pour votre package.
- Exécutez `npm init` dans ce dossier et remplissez les informations demandées.

## 3. Configurez votre environnement de développement

- Installez les dépendances nécessaires (React, Babel, etc.).
- Configurez Babel pour la transpilation.
- Mettez en place un système de build (webpack, rollup, etc.).

## 4. Structurez votre projet

- Placez votre composant dans un dossier `src`.
- Créez un fichier `index.js` qui exporte votre composant.

## 5. Écrivez votre composant et testez-le localement.

## 6. Configurez le fichier `package.json`

- Ajoutez un script de build.
- Spécifiez les fichiers à inclure dans le package.
- Définissez le point d'entrée principal.

## 7. Construisez votre package

- Exécutez votre script de build pour créer une version distribuable.

## 8. Créez un compte npm si vous n'en avez pas déjà un.

## 9. Publiez votre package

- Connectez-vous à npm via la ligne de commande : `npm login`.
- Publiez votre package : `npm publish`.

## 10. Mettez à jour et maintenez votre package

- Mettez à jour la version dans `package.json` pour chaque nouvelle release.
- Republiez avec `npm publish` après chaque mise à jour.

## Exemple de structure de projet

mon-composant-react/
├── src/
│ └── MonComposant.js
├── .babelrc
├── package.json
├── README.md
└── index.js

## Exemple de `package.json`

```json
{
	"name": "mon-composant-react",
	"version": "1.0.0",
	"description": "Un composant React réutilisable",
	"main": "dist/index.js",
	"scripts": {
		"build": "babel src -d dist"
	},
	"peerDependencies": {
		"react": "^17.0.2"
	},
	"devDependencies": {
		"@babel/cli": "^7.14.5",
		"@babel/core": "^7.14.6",
		"@babel/preset-react": "^7.14.5"
	},
	"files": ["dist"]
}
```
