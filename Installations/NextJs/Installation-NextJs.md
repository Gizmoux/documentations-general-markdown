# Documentation et Installation de Next.js

## Qu'est-ce que Next.js ?

Next.js est un framework React qui permet de créer des applications web full-stack. Il offre :

- Rendu côté serveur (SSR) et génération de sites statiques (SSG)
- Support TypeScript intégré
- Routage intelligent basé sur le système de fichiers
- Optimisation automatique du code
- Support des API Routes pour créer des API

## Prérequis

- Node.js (version 12.22.0 ou ultérieure)
- npm (généralement installé avec Node.js)

## Installation

### Création d'un nouveau projet

- Utilisez la commande create-next-app :

npx create-next-app@latest mon-projet-next

- Ou avec Yarn :

yarn create next-app mon-projet-next

### Configuration

- Répondez aux questions de configuration :
  - Voulez-vous utiliser TypeScript ?
  - Voulez-vous utiliser ESLint ?
  - Voulez-vous utiliser Tailwind CSS ?
  - Voulez-vous utiliser le répertoire `src/` ?
  - Voulez-vous utiliser App Router ? (recommandé)
  - Voulez-vous personnaliser l'alias d'importation par défaut (@/\*) ?

## Structure du projet

Après l'installation, votre projet aura la structure suivante :

mon-projet-next/
├── pages/
├── public/
├── styles/
├── .gitignore
├── next.config.js
├── package.json
└── README.md

## Démarrage du serveur de développement

- Naviguez dans le répertoire du projet :

cd mon-projet-next

- Démarrez le serveur de développement :

npm run dev

- Ou avec Yarn :

yarn dev

- Ouvrez http://localhost:3000 dans votre navigateur

## Concepts clés

- Pages : Fichiers dans le répertoire `pages/` deviennent des routes automatiquement
- API Routes : Fichiers dans `pages/api/` deviennent des endpoints API
- `_app.js` : Pour initialiser les pages
- `_document.js` : Pour personnaliser le document HTML

## Déploiement

- Build de production :

npm run build

- Démarrage en mode production :

npm start

## Ressources supplémentaires

- [Documentation officielle Next.js](https://nextjs.org/docs)
- [Apprendre Next.js](https://nextjs.org/learn)
- [Exemples Next.js](https://github.com/vercel/next.js/tree/canary/examples)
