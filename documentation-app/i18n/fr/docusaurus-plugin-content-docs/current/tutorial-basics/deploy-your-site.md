---
sidebar_position: 5
---

# Déployer votre site

Docusaurus est un **générateur de site statique** (également appelé **[Jamstack](https://jamstack.org/)**).

Il construit votre site en tant que simple **fichiers statiques HTML, JavaScript et CSS**.

## Construire votre site

Construisez votre site **pour la production**:

```bash
npm run build
```

Les fichiers statiques sont générés dans le dossier `build`.

## Déployer votre site

Testez votre version de production localement:

```bash
service npm run
```

Le dossier `build` est maintenant servi à [http://localhost:3000/](http://localhost:3000/).

You can now deploy the `build` folder **almost anywhere** easily, **for free** or very small cost (read the **[Deployment Guide](https://docusaurus.io/docs/deployment)**).
