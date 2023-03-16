---
sidebar_position: 3
---

# Créer un billet de blog

Docusaurus crée une page **pour chaque post de blog**, mais aussi une **page d'index de blog**, un système de balises ****, un fil **RSS**...

## Créer votre premier message

Créez un fichier sur `blog/2021-02-28-greetings.md`:

```md title="blog/2021-02-28-greetings.md"
---
slug: salutations
title: Salutations !
auteurs:
  - nom: Joel Marcey
    title: Co-créateur de Docusaurus 1
    url: https://github. om/JoelMarcey
    image_url: https://github.com/JoelMarcey. ng
  - nom: Sébastien Lorber
    title: Mainteneur Docusaurus
    url: https://sebastienlorber. om
    image_url: tags https://github.com/slorber.png
: [greetings]
---

Félicitations, vous avez fait votre premier post !

N'hésitez pas à jouer et à éditer ce message autant que vous le souhaitez.
```

Un nouveau billet de blog est maintenant disponible sur [http://localhost:3000/blog/greetings](http://localhost:3000/blog/greetings).
