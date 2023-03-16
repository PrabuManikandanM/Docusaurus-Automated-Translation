---
sidebar_position: 1
---

# Gérer les versions de la documentation

Docusaurus peut gérer plusieurs versions de votre documentation.

## Créer une version docs

Publiez une version 1.0 de votre projet :

```bash
npm exécute docusaurus docs:version 1.0
```

Le dossier `docs` est copié dans `versioned_docs/version-1.0` et `versions.json` est créé.

Vos docs ont maintenant 2 versions:

- `1.0` à `http://localhost:3000/docs/` pour la version 1.0 docs
- `courant` à `http://localhost:3000/docs/next/` pour les **docs à venir non publiés**

## Ajouter une liste déroulante de version

Pour naviguer de façon transparente entre les versions, ajoutez une liste déroulante.

Modifier le fichier `docusaurus.config.js`:

```js title="docusaurus.config.js"
module. xports = {
  themeConfig: {
    navbar: {
      items: [
        // highlight-start
        {
          type: 'docsVersionDropdown',
        },
        // surligne-fin
      ],
    },
  },
};
```

La liste déroulante de la version docs apparaît dans votre barre de navigation :

![Liste déroulante de la version des documents](./img/docsVersionDropdown.png)

## Mettre à jour une version existante

Il est possible de modifier les docs versionnés dans leur dossier respectif:

- `versioned_docs/version-1.0/hello.md` mise à jour `http://localhost:3000/docs/bonjour`
- `docs/hello.md` met à jour `http://localhost:3000/docs/next/bonjour`
