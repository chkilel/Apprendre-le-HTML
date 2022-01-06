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
- `<body>` définit le corps du document, c'est le conteneur pour tous les contenus visibles, tels que  les paragraphes, les images, les liens hypertexte, les tableaux, les listes, etc.
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
<br><hr>

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
 `<mark>` | Texte marqué| <p>Do not forget to buy <mark>milk</mark> today.</p>
 `<small>` | Texte plus petit| <small>This is some smaller text.</small>
 `<del>` | Texte supprimé| <del>I'm a deleted text</del>
 `<ins>` | Texte inséré| <ins>I'm am inserted text</ins>
 `<sub>` | Texte en indice| H<sub>2</sub>O
 `<sup>` | Texte en exposant| m<sup>2</sup>

<br><hr>

 ## Images HTML
 La balise `<img>` possède deux attributs obligatoires :
  - **src** - Spécifie le chemin d’accès à l’image
  - **alt** - Spécifie un texte de remplacement pour l’image

Exemple : `<img src="animal.jpg" alt="animal">`

>Les attributs `width` et `height` servent pour definir la taille d'affichage des images, exemple:
> `<img src="/public/animal.jpg" alt="animal" width="100" height="100">`

Si vous avez vos images dans un sous-dossier, vous devez inclure le nom du dossier dans l’attribut `src`, exemple : `<img src="/public/images/animal.jpg" alt="animal">`

Si vous avez vos images dans un dossier parent, vous devez inclure `../` dans l’attribut `src`, exemple :
`<img src="../animal.jpg" alt="animal">`

Pour pointer vers une image sur un autre site web, ous devez spécifier une URL absolue (lien complet) dans l’attribut `src`, exemple : `<img src="http://www.google.com/images/logo.png" alt="logo google">`

<br><hr>

## Liens HTML

La balise HTML `<a>` définit un lien hypertexte, elle a la syntaxe suivante :
>`<a href="http://www.google.com">Google</a>`

Un lien vers un autre site utilisent une **URL absolue** (une adresse Web complète) dans l’attribut **href**. expl : `<a href="http://www.google.com">Google</a>`

Un lien local (un lien vers une page du même site Web) est spécifié avec une **URL relative** (sans la partie **https://www** ): exemple : `<a href="pages/nature.html">Nature</a>`

**On ajoute `../` pour remonter si on se retrouve dans un sous répertoire :**

> `<a href="../index.html">Retour à la page principale</a>`

Pour utiliser une image comme lien, il suffit de mettre la balise `<img>` à l’intérieur de la balise `<a>` :
```html
<a href="http://www.google.com">
  <img src="http://www.google.com/images/logo.png" alt="logo google">
</a>
```

L’attribut `target="_blank"` permet d’ouvrir un lien dans une nouvelle fenêtre/onglet du navigateur: exemple : `<a href="http://www.google.com" target="_blank">Google</a>`

***Des liens « internes » ou ancres internes***

Le lien interne permet de renvoyer l’utilisateur à l’intérieur de la même page, a cible est définie par un `id="ancre_du_lien"`

On utilise `<a href="#ancre_du_lien">` pour créer le lien.

<br><hr>

## Favicon

Un favicon est une petite image affichée à côté du titre de la page dans l’onglet du navigateur.

Pour ajouter un favicon à votre site Web, ajouter un élément `<link>` à votre fichier « html », après l’élément `<title>`, comme ceci:

```html
<head>
  <title>My Page Title</title>
  <link rel="icon" type="image/x-icon" href="/images/favicon.png">
</head>
```

<br><hr>

## Listes HTML

Les listes HTML permettent de regrouper un ensemble d'éléments associés dans des listes.

***Liste HTML non ordonnée***

```html
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
```

***Liste HTML ordonnée***

```html
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

<br><hr>

## Tableaux HTML
Un tableau sert à organiser des informations structurées sous forme tabulaire, il se compose de lignes organisées elles-mêmes en cellules.
- La balise `<table> </table>` permet d’indiquer le début et la fin du tableau.
- La balise `<tr> </tr>` caractérise une nouvelle ligne dans le tableau.
- La balise `<td> </td>` marque le contenu d’une cellule dans une ligne

exemple :
```html
<table>
    <tr>
      <th>Team</th>            //th = titre
      <th>Ranking</th>
    </tr>
    <tr>
      <td>South Africa</td>    //td = cellule
      <td>2</td>
    </tr>
    <tr>
      <td>Australia</td>
      <td>3</td>
    </tr>
</table>
```

### Fusion de cellules
- Il est possible de fusionner certaines cellules entre elles avec l’attribut `colspan=" nombredecellules"` qui se place sur la cellule (th ou td)
- La valeur numérique de cet attribut précise le nombre de colonnes du tableau que couvre la cellule.

```html
<table style="width:100%">
  <tr>
    <th colspan="2">Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>43</td>
  </tr>
</table>
```
<br>

### Fusion de lignes
Il est possible de fusionner des lignes avec l’attribut `rowspan=" nombredelignes"` qui se place sur la cellule (th ou td)
```html
<table>
  <tr>
    <th>Name</th>
    <td>Jill</td>
  </tr>
  <tr>
    <th rowspan="2">Phone</th>
    <td>555-1234</td>
  </tr>
  <tr>
    <td>555-8745</td>
  </tr>
</table>
```
