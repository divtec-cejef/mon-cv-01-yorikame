# Les astuces et remarques du père Fallet
Vous trouverez ci-après un florilège des différentes erreurs que je constate fréquemment
durant mes revues de codes avec mes chères élèves et apprentis.

Bonne lecture, Steve.
## HTML
* Organiser votre site avec des dossiers (`css/`, `fonts/`, `img/`, ... )
 ```
racine-de-mon-site
  │  
  └─── css
  │     └─ main.css
  │ 
  └─── fonts
  │     └─ arial.eot
  │     └─ arial.svg
  │     └─ arial.ttf
  │     └─ arial.woff
  │ 
  └─── img
  │     └─ logo.svg
  │     └─ photo-plage.jpg  
  │ 
  └─ favicon.ico
  └─ index.html
 ```
* Nom des fichiers et dossiers **en minuscules et sans caractères spéciaux** `CSS/TropStylé.css` > `css/trop-style.css`
 y compris les images et polices.
* La page d'accueil de votre site doit se nommer `index.html` tout en minuscule.
* Définir la **bonne langue** dans `<html>`.
  Si votre contenu est en français, mettre `<html lang="fr">`, et non `<html lang="en">`.
* Mettre un vrais `<title>` à votre site !
  Le titre doit être composé des mêmes mots-clé que le titre principal du site `<h1>`, suivi du nom de votre site.
```html
<title>Tout l’assortiment de jouets | Migros</title>
```` 
* Il manque `viewport` obligatoire pour un bon affichage sur smartphone 
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
* Ne pas oublier d'ajouter l'**icône de site**, appelée favicon.
```html
<link rel="icon" href="favicon.ico">
```
* Pas d'espaces ni de majuscules dans les id ou class, utiliser des `-` ou  `_` à la place. `class="épéeRouge"` > `class="epee-rouge"`
* Supprimer les espaces inutiles au début des balises.
  * Faux : `<p> apprentie informaticienne 1ère année à l'EMT </p>`
  * Juste : `<p>apprentie informaticienne 1ère année à l'EMT</p>`
* Supprimer les espaces dans `href` pour le numéro de tel : `<a href="tel:0041791234567">Mon tel</a>`
* Un paragraphe `<p>` doit contenir au minimum une phrase. Si ce n'est pas le cas on utilisera une `<div>` à la place.
* Pas d'espace autour du signe `=` dans les attributs HTML
    * Faux : `<ul class = "sommaire">`
    * Juste : `<ul class="sommaire">`
* Les `<p>` peuvent uniquement contenir des éléments inline comme : `<strong>`, `<em>`, `<a>`, ...
* On ne peut pas écrire des textes directement dans le `<body>` il faut les ajouter dans un élément comme : `<p>`, `<div>`, `<h1>`, ...
* Pas utiliser `<br>` pour créer des espaces ou des marges. On utilise les `<br>` uniquement dans les blocs de textes.
  * Utiliser le CSS avec `padding` ou `margin` pour créer des marges et espacer les éléments.
* Ne pas oublier de préciser le texte alternatif des images avec l'attribut `alt=""`
```html
    <img src="img/fifty-burgers.png" alt="Logo Fifty Burgers"/>
```` 
* Éviter de donner des tailles aux images en HTML, le faire en CSS avec `height` et `width`
* Toujours **terminer** vos fichiers de code (HTML, CSS, JavaScript, ...) par une **nouvelle ligne vide** pour simplifier les traitements automatisés.
* Valider votre code : https://validator.w3.org/nu/

## CSS
* Il manque des instructions pour le designe de base du site
```css
body {
    font-family: Verdana, sans-serif;   /* Police d'écriture de base */
    font-weight: normal;                /* Epaisseur du texte de base*/
    font-size: 1.2rem;                  /* taille du texte de base*/
    line-height: 1.4;                   /* Hauteur de ligne de base, généralement entre 1.3 et 1.7 */
    color: black;                       /* couleur du texte de base*/
    background-color: white;            /* couleur d'arrière plan du site */
}
```
* utiliser des noms de classes CSS représentatifs et compréhensibles.
* Utiliser les `em` à la place des % pour les tailles de textes : `200% => 2em`
* Toujours écrire les noms des couleurs en minuscules
* Toujours ajouter une ligne blanche entre deux blocs de règles CSS
```
h2 {
    color:red;
}

h3 {
    color:blue;
}
```  
* Mettre les accolade sur la même ligne que le sélecteur
```
/* Faux */
h1
{
    color:red;
}

/* Faux */
h1 { color:red; }

/* Juste */
h1 {
    color:red;
}
```
* Revenir à la ligne après la `,` si plusieurs sélecteurs
```
/* Faux */ 
h1, h2, h3 {
    color:red;
}

/* Juste */
h1,
h2,
h3 {
    color:red;
}
```



