---
sidebar_position: 1
---

# Créer une page

Ajouter des fichiers **Markdown ou React** à `src/pages` pour créer une page **autonome**:

- `src/pages/index.js` → `localhost:3000/`
- `src/pages/foo.md` → `localhost:3000/foo`
- `src/pages/foo/bar.js` → `localhost:3000/foo/bar`

## Créez votre première page React

Créer un fichier à `src/pages/my-react-page.js`:

```jsx title="src/pages/my-react-page.js"
importer React depuis 'react';
importer la mise en page depuis '@theme/Layout';

export fonction par défaut MyReactPage() {
  return (
    <Layout>
      <h1>Ma page React</h1>
      <p>Ceci est une page React</p>
    </Layout>
  ) ;
}
```

Une nouvelle page est maintenant disponible sur [http://localhost:3000/my-react-page](http://localhost:3000/my-react-page).

## Créez votre première page Markdown

Créer un fichier à `src/pages/my-markdown-page.md`:

```mdx title="src/pages/my-markdown-page.md"
# Ma page Markdown

Ceci est une page Markdown
```

Une nouvelle page est maintenant disponible sur [http://localhost:3000/my-markdown-page](http://localhost:3000/my-markdown-page).
