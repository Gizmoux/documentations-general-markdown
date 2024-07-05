# Tailwind CSS - Commandes et Concepts Principaux

## Installation et Configuration

- `npm install -D tailwindcss`

  - Installe Tailwind CSS comme dépendance de développement

- `npx tailwindcss init`

  - Génère un fichier de configuration Tailwind (tailwind.config.js)

- `npx tailwindcss init -p`
  - Génère à la fois tailwind.config.js et postcss.config.js

## Fichier de Configuration (tailwind.config.js)

```javascript
module.exports = {
	content: ['./src/**/*.{html,js}'],
	theme: {
		extend: {},
	},
	plugins: [],
};
```

# Directives dans le CSS

@tailwind base;
@tailwind components;
@tailwind utilities;

# Classes Utilitaires Courantes

## Layout

- container : Conteneur responsive
- flex, grid : Systèmes de mise en page
- hidden, block, inline : Contrôle de l'affichage

## Flexbox & Grid

- flex-row, flex-col : Direction flex
- justify-center, items-center : Alignement flex
- grid-cols-3, col-span-2 : Configuration de grille

## Espacement

- p-4, px-2, py-3 : Padding
- m-4, mx-auto, my-2 : Margin

## Taille

- w-full, w-1/2, h-screen : Largeur et hauteur
- max-w-sm, min-h-0 : Tailles max et min

## Typographie

- text-sm, text-xl : Taille du texte
- font-bold, font-light : Poids de la police
- text-center, text-right : Alignement du texte
- text-blue-500 : Couleur du texte

## Arrière-plan et Bordures

- bg-red-500, bg-opacity-50 : Couleur et opacité de l'arrière-plan
- border, border-2, border-blue-500 : Bordures
- rounded, rounded-full : Coins arrondis

## Effets

- shadow-md, shadow-lg : Ombres
- opacity-50 : Opacité
- transition, hover: : Effets de transition et survol

## Responsive Design

- sm:, md:, lg:, xl:, 2xl: : Préfixes pour le design responsive

# Commandes CLI

- npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
  Compile et surveille les changements

- npx tailwindcss -i ./src/input.css -o ./dist/output.css --minify
  Compile et minifie le CSS pour la production

# Plugins Populaires

- @tailwindcss/forms
- @tailwindcss/typography
- @tailwindcss/aspect-ratio

# Personnalisation

- Étendre le thème dans tailwind.config.js
- Créer des composants personnalisés avec @apply
