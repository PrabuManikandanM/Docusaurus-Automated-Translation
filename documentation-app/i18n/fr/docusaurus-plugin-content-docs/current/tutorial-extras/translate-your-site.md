---
sidebar_position: 2
---

# Traduire votre site

Traduisons `docs/intro.md` en français.

## Configurer i18n

Modifiez `docusaurus.config.js` pour ajouter le support de la locale `fr`:

```js title="docusaurus.config.js"
module.exports = {
  i18n: {
    defaultLocale: 'en',
    locales: ['en', 'fr'],
  },
};
```

## Traduire un doc

Copiez le fichier `docs/intro.md` dans le dossier `i18n/fr`:

```bash
mkdir -p i18n/fr/docusaurus-plugin-content-docs/current/

cp docs/intro.md i18n/fr/docusaurus-plugin-content-docs/current/intro.md
```

Traduire `i18n/fr/docusaurus-plugin-content-docs/current/intro.md` en français.

## Démarrez votre site localisé

Démarrez votre site dans la langue française :

```bash
npm run start -- --locale fr
```

Votre site localisé est accessible à [http://localhost:3000/fr/](http://localhost:3000/fr/) et la page `Getting Started` est traduite.

:::prudence

En développement, vous ne pouvez utiliser qu'une seule locale à la fois.

:::

## Ajouter une liste déroulante des locales

Pour naviguer de façon transparente dans les langues, ajoutez une liste déroulante de locales.

Modifier le fichier `docusaurus.config.js`:

```js title="docusaurus.config.js"
module. xports = {
  themeConfig: {
    navbar: {
      items: [
        // highlight-start
        {
          type: 'localeDropdown',
        },
        // surligne-fin
      ],
    },
  },
};
```

La liste déroulante locale apparaît maintenant dans votre barre de navigation :

![Liste déroulante des locales](./img/localeDropdown.png)

## Construisez votre site localisé

Construisez votre site pour une locale spécifique :

```bash
npm run build -- --locale fr
```

Ou construisez votre site pour inclure toutes les locales en même temps:

```bash
npm run build
```
