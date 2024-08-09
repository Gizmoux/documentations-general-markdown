# Installation

- npm install next-auth
- Créer dossier lib à la racine -> Fichier authOptions.ts
- Récupérer GITHUB_ID et GITHUB_SECRET dans settings/developper settings
- Aller sur https://console.cloud.google.com/ -> Créer un projet et aller dans API -> Créer un ID client OAuth
- Remplir Type d'application : Application Web, le nom.
- URI1 : http://localhost:3000
- URI de redirection : http://localhost:3000/api/auth/callback/google puis Créer
- Créer un .env avec GITHUB_ID,GITHUB_SECRET,GOOGLE_CLIENT_ID,GOOGLE_CLIENT_SECRET
- Dans authOptions, remplir le provider comme suit:
  ```js
       GithubProvider({
  		clientId: process.env.GITHUB_ID as string,
  		clientSecret: process.env.GITHUB_SECRET as string,
  	}),
  	GoogleProvider({
  		clientId: process.env.GOOGLE_CLIENT_ID as string,
  		clientSecret: process.env.GOOGLE_CLIENT_SECRET as string,
  	}),
  ```
- Créer dans app api/auth/[...nextauth]/route.ts et y mettre cela:

```js
import NextAuth from 'next-auth';
import { authOptions } from '@/lib/authOptions';

const handler = NextAuth(authOptions);
export { handler as GET, handler as POST };
```

- Créer lib/SessionWrapper.tsx et y mettre:

```js
'use client';
import { SessionProvider } from 'next-auth/react';
const SessionWrapper = ({ children }: { children: React.ReactNode }) => {
	return <SessionProvider>{children}</SessionProvider>;
};
export default SessionWrapper;
```

- Dans layout.tsx, wrapper le tout comme suit:

```js
<SessionWrapper>
	<html lang="en">
		<body className={inter.className}>{children}</body>
	</html>
</SessionWrapper>
```

- Dans page.tsx crée un bouton:

```js
<button
	className="bg-gray-400 hover:bg-gray-500 rounded-md p-3"
	onClick={() => signIn('google')}
>
	Se connecter avec Google
</button>
```
