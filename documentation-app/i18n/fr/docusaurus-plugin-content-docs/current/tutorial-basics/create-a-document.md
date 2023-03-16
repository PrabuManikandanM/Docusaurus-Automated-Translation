---
sidebar_position: 2
---

# Créer un document

Les documents sont **groupes de pages** connectés à travers :

- a **sidebar**
- **navigation précédente/suivante**
- **versioning**

## Créez votre premier doc

Créer un fichier Markdown sur `docs/hello.md`:

```md title="docs/hello.md"
# Bonjour

Ceci est mon **premier document Docusaurus**!
```

Un nouveau document est maintenant disponible sur [http://localhost:3000/docs/bonjour](http://localhost:3000/docs/hello).

## Configurer la barre latérale

Docusaurus automatiquement **crée une barre latérale** à partir du dossier `docs`.

Ajouter des métadonnées pour personnaliser le libellé et la position de la barre latérale :

```md title="docs/hello.md" {1-4}
---
sidebar_label: 'Bonjour !'
sidebar_position: 3
---

# Bonjour

Ceci est mon **premier document Docusaurus** !
```

Il est également possible de créer explicitement votre barre latérale dans `sidebars.js`:

```js title="sidebars.js"
module. xports = {
  tutorialSidebar: [
    'intro',
    // surligne-next-line
    'bonjour',
    {
      type: 'category',
      étiquette : 'Tutoriel',
      éléments : ['tutorial-basics/create-a-document'],
    },
  ],
};
```
