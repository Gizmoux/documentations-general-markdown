# Installation avec FTP

- Acheter un hébergement (perso)
- Aller dans Hébergements / nomdusite."fr/com"
- Cliquer sur FTP Explorer
- Dans l'application (ici Next.js) mettre la config suivante dans next.cfg

```js
/** @type {import('next').NextConfig} */
const nextConfig = {
	images: { unoptimized: true },
	output: 'export',
};

export default nextConfig;
```

- build l'application et faire un zip du code à l'intérieur du .out !
- Upload sur net2ftp et recharger la page du site => Site en ligne

# Installation avec VPS
