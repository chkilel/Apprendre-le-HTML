# HTML
## Document HTML
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Titre de la page</title>
  </head>

  <body>
    <h1>Premier titre</h1>
    <p>Mon premier paragraphe</p>
  </body>
</html>
```


<div class="text-sm ml-2">

- `<!DOCTYPE html>` définit que ce document est un document HTML5
- `<html>` est l’élément racine d’une page HTML
- `<head>` contient des méta-informations sur la page HTML
- `<title>` spécifie un titre pour la page HTML (qui est affiché dans la barre de titre du navigateur ou dans l’onglet de la page)
- `<body>` définit le corps du document, c'est le conteneur pour tous les contenus visibles, tels que  les paragraphes, les images, les liens hypertexte, les tableaux, leslistes, etc.
- `<h1>` définit un grand titre
- `<p>` définit un paragraphe

<hr>

## Élément HTML ?

Un élément HTML est défini par une balise de début, du contenu et une balise de fin :

```html
<h1> Mon premier titre</h1>
```

> Certains éléments HTML n’ont pas de contenu **(comme le `<br>` et `<hr>`)**.
> Ces éléments n’ont pas de balise de fin !

<hr>

## Commentaires HTML

Les commentaires HTML ne sont pas affichés dans le navigateur, mais ils peuvent aider à documenter votre code source HTML.
  ```html
  <!-- This is a comment -->
  <p>This is a paragraph.</p>
  <!-- Remember to add more information here -->
  ```

<hr>

## Balises HTML

Balise | Definition | Exemple
---------|----------|---------
 `<p>` | Paragraphe |     <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry</p>
 `<hr>` | Ligne horizontale | <hr>
 `<br>` | Sauts de ligne | <p>Lorem Ipsum <br>is simply dummy text</p>
 `<h1>` | Titre le plus important | <h1>Heading 1</h1>
 `<h2>` `<h3>`  `<h4>` `<h5>`    | ... | ...
 `<h6>` | Titre le moins important. | <h6>Heading 6</h6>
 `<b>` | Texte en gras|   <b>This text is bold</b>
 `<strong>` | Texte important|  <strong>This text is important!</strong>
 `<i>` | Texte en italique|  <i>This text is italic</i>
 `<em>` | Texte qui souligne un propos, une ideé, ...| <em>This text is emphasized</em>
 `<mark>` | Texte marqué| <small>This is some smaller text.</small>
 `<small>` | Texte plus petit| <p>Do not forget to buy <mark>milk</mark> today.</p>
 `<del>` | Texte supprimé| <del>I'm a deleted text</del>
 `<ins>` | Texte inséré| <ins>I'm am inserted text</ins>
 `<sub>` | Texte en indice| H<sub>2</sub>O
 `<sup>` | Texte en exposant| m<sup>2</sup>