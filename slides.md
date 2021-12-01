---
# try also 'default' to start simple
# themey: seriph
# theme: apple-basic
theme: default
fonts:
  # basically the text
  sans: 'Robot'
  # use with `font-serif` css class from windicss
  serif: 'Robot Slab'
  # for code blocks, inline code, etc.
  mono: 'Fira Code'
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
---

# Introduction à l'HTML

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer flex justify-center items-center" hover="bg-white bg-opacity-10">
    <vscode-icons:file-type-html class="h-20 w-20" />
    <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---

# Qu’est-ce que le html ?

HTML est le langage de balisage pour la création de pages Web.

<br>

- HTML signifie **Hyper Text Markup Language**
- HTML est language qui décrit la structure d’une page Web
- HTML se compose d’une série de balises
- Les balises HTML indiquent au navigateur comment afficher le contenu
- Les balise HTML étiquettent des éléments de contenu tels que
  - ceci est un titre
  - ceci est un paragraphe
  - ceci est un lien,
  - etc.

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

---
layout: two-cols
---

# Document HTML

```html {all|1|2,13|3,5|7,12|4|9|10}
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
::right::

<div class="text-sm ml-2">

`<!DOCTYPE html>` définit que ce document est un document HTML5

`<html>` est l’élément racine d’une page HTML

`<head>` contient des méta-informations sur la page HTML

`<title>` spécifie un titre pour la page HTML (qui est affiché dans la barre de titre du navigateur ou dans l’onglet de la page)

`<body>` définit le corps du document, c'est le conteneur pour tous les contenus visibles, tels que  les paragraphes, les images, les liens hypertexte, les tableaux, les
listes, etc.

`<h1>` définit un grand titre

`<p>` définit un paragraphe


</div>


---
layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080
---

# Qu’est-ce qu’un élément HTML ?

> Un élément HTML est défini par une balise de début, du contenu et une balise de fin :

```html
<tagname> Le contenu va ici... </tagname>
```

**Exemple:**
```html
<h1> Mon premier titre</h1>
<p> Mon premier paragraphe. </p>
```

**Remarque :**

> Certains éléments HTML n’ont pas de contenu **(comme le `<br>`)**.
>
> Ces éléments sont appelés éléments vides.
>
> Les éléments vides n’ont pas de balise de fin !

---

# Navigateurs Web

<div grid="~ cols-2 gap-4">
  <div>
    <et-browser class="h-90 w-90" />
  </div>

  <div>
Le but d’un navigateur web

- Chrome <logos-chrome />
- Edge <logos-microsoft-edge />
- Firefox <logos-firefox />
- Safari <logos-safari />
- ou autres

est de lire les documents HTML et de les afficher correctement.

> Un navigateur n’affiche pas les balises HTML, mais les utilise pour déterminer comment afficher le document.

  </div>
</div>

---

<div grid="~ cols-2 gap-2" m="-t-2">

  <div class="text-sm" style="width: 99%; border: 1px solid grey; padding: 3px; margin: 0px; background-color: rgb(221, 221, 221); text-align: start;">
    &lt;html&gt;
  <div style="width:90%;border:1px solid grey;padding:3px;margin:20px">
    &lt;head&gt;
  <div style="width:90%;border:1px solid grey;padding:5px;margin:20px" _msthash="471640" _msttexthash="630812">&lt;title&gt;Titre de la page&lt;/title&gt; </div>
    &lt;/head&gt;
  </div>
  <div style="width:90%;border:1px solid grey;padding:3px;margin:20px;background-color:#ddd">
     &lt;body&gt;
      <div style="width:90%;border:1px solid grey;padding:3px;margin:20px;background-color:#fff">
        <div style="width:90%;border:1px solid grey;padding:5px;margin:20px" _msthash="689910" _msttexthash="4192279">&lt;h1&gt;Il s’agit d’un titre&lt;/h1&gt;</div>
        <div style="width:90%;border:1px solid grey;padding:5px;margin:20px" _msthash="690053" _msttexthash="4161950">&lt;p&gt;Il s’agit d’un paragraphe.&lt;/p&gt;</div>
        <div style="width:90%;border:1px solid grey;padding:5px;margin:20px" _msthash="690196" _msttexthash="1952158">&lt;p&gt;C’est un autre paragraphe.&lt;/p&gt;</div>
      </div>
      &lt;/body&gt;
  </div>
  &lt;/html&gt;
  </div>

<div>

# Structure d'une Page HTML

**Remarque :**
> Le contenu à l’intérieur de la section `<body>` (la zone blanche) sera affiché dans un navigateur.
>
> Le contenu de l'element `<title>` sera affiché dans la barre de titre du navigateur ou dans l’onglet de la page.
</div>
</div>

---

# Éditeurs HTML
Un simple éditeur de texte est tout ce dont vous avez besoin pour apprendre le HTML.


<div class="flex justify-between items-center">
<logos-visual-studio-code  class="h-60 w-60"/>

<img src="https://code.visualstudio.com/assets/home/home-screenshot-mac-lg-2x.png" class="h-90">
</div>


---

# Paragraphes HTML

L’élément HTML `<p>` définit un paragraphe.

<br>

**Un paragraphe**
- commence toujours sur une nouvelle ligne.
-  il est généralement un bloc de texte
-  Les navigateurs ajoutent automatiquement un espace blanc (une marge) **avant** et **après** un paragraphe.


---
layout: two-cols
---

# Paragraphes HTML

```html
<!DOCTYPE html>
<head>
  <title>Titre de la page</title>
</head>

<html>
  <body>

    <p>aaaaaaaLorem Ipsum is simply dummy text of the printing and typesetting industry.
      Lorem Ipsum has been the industry's standard dummy text ever since the 1500s,
    </p>
    <p>Les navigateurs ajoutent automatiquement un espace blanc (une marge)
      avant et après un paragraphe.
    </p>
    <p>Contrary to popular belief, Lorem Ipsum is not simply random text.
      It has roots in a piece of classical Latin literature from 45 BC,
      making it over 2000 years old. Richard McClintock, a Latin professor
      at Hampden-Sydney College in Virginia, looked up one of the more
      obscure Latin words, consectetur
    </p>

  </body>
</html>

```
::right::

<div class="p-4 mt-7">

<p class="bg-indigo-50">aaaaaaaLorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s,</p><p class="bg-indigo-50">Les navigateurs ajoutent automatiquement un espace blanc (une marge) avant et après un paragraphe.</p>
<p class="bg-indigo-50">Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at Hampden-Sydney College in Virginia, looked up one of the more obscure Latin words, consectetur</p>

</div>


---

# Affichage HTML
Vous ne pouvez pas être sûr de la façon dont le code HTML sera affiché.

Les grands ou petits écrans et les fenêtres redimensionnées créeront des résultats différents.

Vous ne pouvez pas modifier l’affichage en ajoutant des espaces ou des lignes supplémentaires dans votre code HTML.
Le navigateur supprimera automatiquement tous les espaces et lignes supplémentaires lorsque la page est affichée :


<div grid="~ cols-2 gap-4">

```html
      <p>
      This paragraph
      contains a lot of lines
      in the source code,
      but the browser
      ignores it.
      </p>

      <p>
      This paragraph
      contains         a lot of spaces
      in the source         code,
      but the        browser                         ignores it.
      </p>
```


  <div>
    <p>
      This <br> paragraph
      contains a lot of lines
      in the source code,
      but the browser
      ignores it.
    </p>
    <p>
      This paragraph
      contains         a lot of spaces
      in the source         code,
      but the        browser                         ignores it.
    </p>

  </div>
</div>


---

# Ligne horizontales HTML
La balise `<hr>` définit une rupture dans une page HTML et est le plus souvent affichée sous forme de ligne horizontale.

L’élément est utilisé pour séparer le contenu (ou définir une modification) dans une page HTML :`<hr>`

<div grid="~ cols-2 gap-4">

  ```html
    <h1>This is heading 1</h1>
    <p>This is some text.</p>
    <hr>
    <h2>This is heading 2</h2>
    <p>This is some other text.</p>
    <hr>
  ```

  <div>
    <h1>This is heading 1</h1>
    <p>This <hr> is some text.</p>
    <hr>
    <h2>This is heading 2</h2>
    <p>This is some other text.</p>
    <hr>
  </div>
</div>

<twemoji-straight-ruler class="h-20 w-90"/>

> La balise `<hr>` est une balise vide, ce qui signifie qu’elle n’a pas de balise de fin.


---

# Sauts de ligne HTML
L’élément HTML `<br>` définit un saut de ligne.

Utilisez `<br>` si vous voulez un saut de ligne (une nouvelle ligne) sans commencer un nouveau paragraphe
<div grid="~ cols-2 gap-4">

  ```html
    <p>This is<br>a paragraph<br>with line breaks.</p>
  ```

  <div>
    <p>This is<br>a paragraph<br>with line breaks.</p>
  </div>

  <br>
  <br>

  <icomoon-free-pagebreak class="h-30 w-90 "/>

  > La balise `<br>` est une balise vide, ce qui signifie qu’elle n’a pas de balise de fin.

</div>

---

# Pratique

<div grid="~ cols-2 gap-4">

  ```html
  Titre
  <p>
      ligne 1
      ligne 2
      ligne 3
      ligne 4
      ligne 5
      ligne 6
  </p>
  ```

  <div>
    <h1>Titre</h1>
    <p>
      ligne 1<br>
      ligne 2<br>
      ligne 3<br>
      <hr>
      ligne 4<br>
      ligne 5<br>
      ligne 6<br>
    </p>
    <hr>
  </div>
</div>



---

# Titres HTML
Les titre HTML sont définis avec les balises `<h1>` à `<h6>`

> `<h1>` définit le titre le plus important.
>
> `<h6>` définit le titre le moins important.

<div grid="~ cols-2 gap-4s">

<div class="mt-10">

  ```html
    <h1>Heading 1</h1>
    <h2>Heading 2</h2>
    <h3>Heading 3</h3>
    <h4>Heading 4</h4>
    <h5>Heading 5</h5>
    <h6>Heading 6</h6>
  ```

</div>
<div class=" ml-10 mt-10">
    <h1>Heading 1</h1>
    <h2>Heading 2</h2>
    <h3>Heading 3</h3>
    <h4>Heading 4</h4>
    <h5>Heading 5</h5>
    <h6 class="!capitalize !opcity-100">Heading 6</h6>
</div>

</div>

**Remarque**
> Les navigateurs ajoutent automatiquement des espaces blancs (une marge) avant et après les titres.


---

# Les titres sont importants

Les moteurs de recherche utilisent les titres pour indexer la structure et le contenu de vos pages Web.

Les utilisateurs parcourent souvent une page par ses titres. Il est important d’utiliser des titres pour afficher la structure du document.

Les titres `<h1> ` doivent être utilisés pour les titres principaux, suivis des titres `<h2>`, puis des moins importants `<h3>`, et ainsi de suite.

**Remarque**
> Utilisez des titres HTML pour les titres uniquement.
>
> N’utilisez pas les titres pour rendre le texte GRAND ou gras.

<div grid="~ cols-2 gap-4">

</div>


---

# Mise en forme du texte HTML
HTML contient plusieurs éléments pour définir un texte avec une signification particulière.

Les éléments de mise en forme ont été conçus pour afficher des types spéciaux de texte :

- `<b>` - Texte en gras
- `<strong>` - Texte important
- `<i>` - Texte en italique
- `<em>` - Texte qui souligne un propos, une ideé, ...
- `<mark>` - Texte marqué
- `<small>` - Texte plus petit
- `<del>` - Texte supprimé
- `<ins>` - Texte inséré
- `<sub>` - Texte en indice
- `<sup>` - Texte en exposant


---

# Les balises HTML `<b>` et `<strong>`
Texte en gras

<div grid="~ cols-2 gap-4">

  <div>

  La balise HTML `<b>` définit le texte en gras, sans importance.

  ```html
  <b>This text is bold</b>
  ```

  <b>This text is bold</b>
  </div>

  <div>

  La balise HTML `<strong>` définit le texte avec une grande importance. Le contenu à l’intérieur est généralement affiché en gras.

  ```html
    <strong>This text is important!</strong>
  ```

  <strong>This text is important!</strong>
  </div>

</div>

---

# Les balises HTML `<i>` et `<em>`
Texte en gras

<div grid="~ cols-2 gap-4">

  <div>

  La balise HTML `<i>` définit une partie du texte affichée en italique.

  Elle est souvent utilisée pour indiquer un terme technique, une phrase d’une autre langue, une pensée, un nom de propre, etc.

  **Exemple**

  ```html
  <i>This text is italic</i>
  ```

  <i>This text is italic</i>

  </div>

  <div>

  La balise HTML `<em>` définit une partie du texte dans une autre voix ou humeur. Le contenu à l’intérieur est généralement affiché en italique

  Un lecteur d’écran prononcera les mots avec un accent en stressant le mot.


  ```html
    <em>This text is emphasized</em>
  ```

  <em>This text is emphasized</em>ss
  </div>

</div>

---
# Les balises HTML `<i>` et `<em>`
L’élément HTML `<i>` définit une partie du texte affiché en italique.

<div grid="~ cols-2 gap-4">

  <div>

  La balise `<i>` est souvent utilisée pour indiquer un terme technique, une phrase d’une autre langue, une pensée, etc.

  ```html
  <i>This text is italic</i>
  ```

  <i>This text is italic</i>

  </div>

  <div>

  La balise HTML `<em>` utilisée pour mettre le texte en valeur. Le contenu à l’intérieur est généralement affiché en italique.

  ```html
  <em>This text is emphasized</em>
  ```

  <em>This text is emphasized</em>

  </div>

</div>

---

# La balise HTML `<small>`
<br>

La balise HTML `<small>` définit un texte plus petit

**Exemple**
```html
<small>This is some smaller text.</small>
```

<div grid="~ cols-2 gap-4">

<div class="pt-20">
<h6> Small </h6>
 <small>This is some smaller text.</small>
</div>
<div class="pt-20">
<h6> Normal </h6>
 This is some smaller text.s
</div>

</div>

---

# La balise HTML `<mark>`
La balise HTML `<mark>` définit le texte qui doit être marqué ou mis en surbrillance

Exemple
```html
<p>Do not forget to buy <mark>milk</mark> today.</p>
```
<br>

<p>Do not forget to buy <mark>milk</mark> today.</p>


---

# Les balises HTML `<del>` `<ins>`
<br>

<div grid="~ cols-2 gap-4">

<div class="pt-20">

La balise HTML `<del>` définit un texte qui a été supprimé d’un document. Les navigateurs affiche généralement une ligne à travers le texte supprimé.

**Exemple**

```html
<p>My favorite color is <del>blue</del> red.</p>
```

<p>My favorite color is <del>blue</del> red.</p>

</div>

<div class="pt-20">

La balise HTML `<ins>` définit un texte qui a été inséré dans un document. Les navigateurs soulignent généralement le texte inséré.

**Exemple**

```html
<p>My favorite color is <del>blue</del> <ins>red</ins>.</p>
```

<p>My favorite color is <del>blue</del> <ins>red</ins>.</p>

</div>

</div>

---

# Les balises HTML `<sub>` `<sup>`

<div grid="~ cols-2 gap-4">

<div class="pt-10">

La balise HTML `<sub>` définit le texte en indice. Le texte en indice apparaît en demi-caractère en dessous de la ligne normale et est parfois rendu dans une police plus petite. Le texte en indice peut être utilisé pour les formules chimiques, comme:

H<sub>2</sub>O

**Exemple**
```html
<p>This is <sub>subscripted</sub> text.</p>
```

<p>This is <sub>subscripted</sub> text.</p>

</div>

<div class="pt-10">

La balise HTML `<sup>` définit le texte en exposant. Le texte en exposant apparaît en demi-caractère au-dessus de la ligne normale et est parfois rendu dans une police plus petite. Le texte en exposant peut être utilisé par exemple pour les surfaces, comme:

m<sup>2</sup>

***Exemple***
```html
<p>This is <sup>superscripted</sup> text.</p>
```
<p>This is <sup>superscripted</sup> text.</p>

</div>
</div>


---

# Commentaires HTML

Les commentaires HTML ne sont pas affichés dans le navigateur, mais ils peuvent aider à documenter votre code source HTML.

<div grid="~ cols-2 gap-4">
  <div class="pt-2">

  **Ajouter des commentaires**

  Avec les commentaires, vous pouvez placer des notifications et des rappels dans votre code HTML:

  ```html
  <!-- This is a comment -->
  <p>This is a paragraph.</p>
  <!-- Remember to add more information here -->
  ```

  <!-- This is a comment -->
  <p>This is a paragraph.</p>
  <!-- Remember to add more information here -->

  </div>

  <div class="pt-2">

  **Masquer le contenu**

  Ce qui peut être utile pour masquer un contenu temporairement

  ```html
  <p>This is a paragraph.</p>
  <!-- <p>This is another paragraph </p> -->
  <p>This is a paragraph too.</p>
  ```

  <p>This is a paragraph.</p>
  <!-- <p>This is another paragraph </p> -->
  <p>This is a paragraph too.</p>

  </div>
</div>

---

# Commentaires HTML (suite)


<div grid="~ cols-2 gap-4">
  <div class="pt-2">

  **Ajouter des commentaires**

  Vous pouvez également masquer plus d’une ligne, tout ce qui se trouve entre `<!--` et  `-->` sera masqué de l’affichage.

  ```html
  <p>This is a paragraph.</p>
  <!--
  <p>Look at this cool image:</p>
  <img border="0" src="pic_trulli.jpg" alt="Trulli">
  -->
  <p>This is a paragraph too.</p>
  ```

  <p>This is a paragraph.</p>
  <!--
  <p>Look at this cool image:</p>
  <img border="0" src="pic_trulli.jpg" alt="Trulli">
  -->
  <p>This is a paragraph too.</p>
  </div>

  <div class="pt-2">

  **Masquer le contenu en ligne**

  Les commentaires peuvent être utilisés pour masquer des parties au milieu du code HTML.

  ```html
  <p>This <!-- great text --> is a paragraph.</p>
  ```

  <p>This <!-- great text --> is a paragraph.</p>

  </div>
</div>

---


# Images HTML
Les images peuvent améliorer la conception et l’apparence d’une page Web.


<div grid="~ cols-2 gap-4">

  <div class="">

  **Syntaxe des images HTML**
  <div class="text-sm">

  - La balise HTML `<img>` est utilisée pour incorporer une image dans une page Web.
  - Les images ne sont pas techniquement insérées dans une page Web, les images sont liées à des pages Web. La balise `<img>` crée un espace de rétention pour l’image référencée.
  - La balise `<img>` est vide, elle contient uniquement des attributs et n’a pas de balise de fermeture.
  - La balise `<img>` possède deux attributs obligatoires :
    - **src** - Spécifie le chemin d’accès à l’image
    - **alt** - Spécifie un texte de remplacement pour l’image

  </div>

  </div>


  <div class="pt-2">

  ```html
  <img src="animal.jpg" alt="animal">
  ```

  <img src="static/animal.jpg" alt="animal">
  </div>

</div>

---

# Images HTML (Dimensions)
Les images peuvent améliorer la conception et l’apparence d’une page Web.


<div grid="~ cols-2 gap-4">

  <div class="">

  **Largeur et hauteur**

  Les attributs `width` et `height` servent pour definir la taille d'affichage des images.

  - `width` : Largeur
  - `height` : Hauteur



  </div>

  <div class="pt-2">

  ```html
  <img src="animal.jpg" alt="animal" width="128" height="128">
  ```

  <img src="static/animal.jpg" alt="animal" width="128" height="128">
  </div>

</div>


---

# Images HTML (Emplacement)
Les images peuvent améliorer la conception et l’apparence d’une page Web.


<div grid="~ cols-2 gap-x-4">

  <div class="">

  **Images dans un autre dossier**

  Si vous avez vos images dans un sous-dossier, vous devez inclure le nom du dossier dans l’attribut :src
  </div>

  <div>
  <img src="static/landscape.jpg" alt="Payasage" width="128" height="128">
  </div>

  <div class="col-span-2">

  ```html
    <img src="/images/html5.gif" alt="Payasage" width="128" height="128">
  ```
  </div>

  <div class="">

  **Images sur un autre serveur/site Web**

  Certains sites Web pointent vers une image sur un autre serveur.
  Pour pointer vers une image sur un autre serveur, vous devez spécifier une URL absolue (lien complèt) dans l’attribut **src**


  </div>

  <div>
  <img src="https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png" alt="Google" width="300">
  </div>

  <div class="col-span-2">

  ```html
    <img src="https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png" alt="Google" width="300">
  ```
  </div>

</div>

---

# Liens HTML

On retrouve les liens dans presque toutes les pages Web. Les liens permettent aux utilisateurs de naviger de page en page.

**Liens HTML - Hyperliens**

Les liens HTML s'appellent des hyperliens.

Vous pouvez cliquer sur un lien pour passer à un autre document.

Lorsque vous déplacez la souris sur un lien, la curseur se transforme en une petite main.

> **Remarque** :
>
> Un lien n’a pas besoin d’être du texte. Un lien peut être une image ou tout autre élément HTML !

---

# Liens HTML
<br>

**Liens HTML - Syntaxe**

La balise HTML `<a>` définit un lien hypertexte. elle a la syntaxe suivante :

```html
<a href="url">link text</a>
```

L’attribut le plus important de l’élément `<a>` est l’attribut **href**, qui indique la destination du lien.

Le texte du lien est la partie qui sera visible par le lecteur.

En cliquant sur le texte du lien, vous enverrez le lecteur à l’adresse URL spécifiée.

**Exemple**

```html
<a href="https://www.groupescolairemalki.com">Visit groupescolairemalki.com!</a>
```
<a href="https://www.groupescolairemalki.com" target="_blank">Visit groupescolairemalksi.com!</a>

---

# Liens HTML - URL absolue et relatives

<br>

Un lien vers un autre site utilisent une URL absolue (une adresse Web complète) dans l’attribut **href**.

Un lien local (un lien vers une page du même site Web) est spécifié avec une URL relative (sans la partie **https://www** ):

<div grid="~ cols-2 gap-x-4">

  <div class="">

  **Liens externe**

  ```html
  <h2>Absolute URLs</h2>
  <p><a href="https://www.groupescolairemalki.com/">Malki school</a></p>
  <p><a href="https://www.google.com/">Google</a></p>
  ```
  <h2>Absolute URLs</h2>
  <p><a href="https://www.groupescolairemalki.com/">Malki school</a></p>
  <p><a href="https://www.google.com/">Google</a></p>

  </div>

  <div class="">

  **Lien interne**

  ```html
  <h2>Relative URLs</h2>
  <p><a href="html_images.html">HTML Images</a></p>
  <p><a href="/css/cours.html">Cours CSS</a></p>
  ```
  <h2>Relative URLs</h2>
  <p><a href="html_images.html">HTML Images</a></p>
  <p><a href="/css/cours.html">Cours CSS</a></p>

  </div>

</div>

---

# Liens HTML - Utiliser une image comme lien

<br>

Pour utiliser une image comme lien, il suffit de mettre la balise `<img>` à l’intérieur de la balise `<a>`

```html
<a href="https://www.google.com/">
  <img src="https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png" alt="Google" width="300">
</a>
```
<a href="https://www.google.com/">
  <img src="https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png" alt="Google" width="300">
</a>

---

# Liens vers un autre répertoire
<br>

On peut avoir des répertoires et sous-répertoires
<br>

**On ajoute le nom du répertoire pour descendre :**
>
> `monrepertoire/mapage.html`

<br>

**On ajoute `../` pour remonter si on se trouve dans un sous répertoire :**
>
> `../index.html`

---

# Descendre dans un sous répertoire
<br>

Depuis la racine index vers page2 :

```html
<a href="page_interne/page-10.html">page 10</a>
```
Si on avait d’autres sous-répertoires :

```html
<a href="page_interne/autre_sous_rep/page-20.html">page 20</a>
```
---

# Remonter d’un répertoire
<br>

**Depuis la page2 vers la racine :**

```html
<a href="../index.html"> l'accueil</a>
```

**Si on veut remonter plusieurs répertoires (autant de `../` que de répertoires):**

```html
<a href="../../index.html"> l'accueil</a>
```

---

# Ouvrir un lien dans un nouvel onglet
<br>

L’attribut `target="_blank"` permet d’ouvrir un lien dans une nouvelle fenêtre/onglet du navigateur

```html
<a href="index.html" target="_blank" >
```

---

# Des liens « internes » ou ancres internes
<br>

Le lien interne permet de renvoyer l’utilisateur à l’intérieur d’une page

La cible est définie par un `id="ancre_du_lien"`

On utilise `<a href="#ancre_du_lien">` pour créer le lien
Utilisé pour les liens « retour en haut de page » par exemple,

---

# Favicon

Un favicon est une petite image affichée à côté du titre de la page dans l’onglet du navigateur.

![Favicon](/static/fav.png)

Pour ajouter un favicon à votre site Web, enregistrez votre image favicon dans le répertoire racine appelé images et enregistrez votre image favicon dans ce dossier. Un nom commun pour une image de favicon est **favicon.ico ou favicon.png ...**

Ensuite, ajoutez un élément `<link>` à votre fichier « html », après l’élément `<title>`, comme ceci:

```html
<head>
  <title>My Page Title</title>
  <link rel="icon" type="image/x-icon" href="/images/favicon.png">
</head>
```
---


# Exercices
## Exercices de base HTML

- Créez une page Web et définissez son titre sur : <br> « Ceci est une page Web ».
- Affichez votre nom à l’écran en premier titre et votre niveau scolaire en paragraphe.
- Affichez le message « Quand cette page Web a-t-elle été créée ? Vérifiez le titre de la page pour la réponse. » à l’écran, et redéfinissez le titre de la page sur la date d'aujourd'hui.

---

# Exercices 2
## Exercices de mise en forme de texte HTML

- Imprimez les carrés des chiffres de 1 à 20. Chaque numéro doit être sur une ligne distincte, à côté du chiffre 2 en exposant, un signe égal et le résultat. <br> Exemple : 10<sup>2</sup> = 100
- Imprimez les 10 premiers lettres de l'alphabet en gras avec leur position en indice avec un saut de ligne entre chaque lettre.<br> Exemple <b>Z</b><sub>26</sub>
- Imprime un titre de niveau h1 suivi d’une ligne horizontale. <br>Sous la ligne horizontale, imprimez un paragraphe relatif au texte du titre.
- Imprimez du texte supprimé et inséré de votre choix. <br>le text supprimé doit etre <del><mark>marqué</mark></del> et le text inséré en <ins><i>italique</i></ins>