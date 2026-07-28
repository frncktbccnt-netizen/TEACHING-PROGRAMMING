# 📘 Introduction au HTML

## Qu'est-ce que le HTML ?

**HTML** (**HyperText Markup Language**) est le langage utilisé pour créer la structure d'une page web.

Le HTML permet de définir les différents éléments d'une page, comme :

- Les titres
- Les paragraphes
- Les images
- Les liens
- Les formulaires
- Les tableaux
- Les listes
- Les vidéos, etc.

> **Remarque :** Le HTML ne sert pas à styliser une page. Pour cela, on utilise **CSS**. Pour rendre une page interactive, on utilise **JavaScript**.

---

# Les balises HTML

Une page HTML est composée de **balises**.

Une balise indique au navigateur quel type de contenu il doit afficher.

## Structure générale d'une balise

```html
<nomBalise>Contenu</nomBalise>
```

Exemple :

```html
<p>Bonjour tout le monde</p>
```

Ici :

- `<p>` est la balise ouvrante.
- `Bonjour tout le monde` est le contenu.
- `</p>` est la balise fermante.

---

# Les parties d'une balise

Prenons cet exemple :

```html
<p class="texte">Bonjour</p>
```

Cette balise possède plusieurs parties.

| Élément         | Description               |
| --------------- | ------------------------- |
| `<`             | Début de la balise        |
| `p`             | Nom de la balise          |
| `class="texte"` | Attribut                  |
| `>`             | Fin de la balise ouvrante |
| Bonjour         | Contenu                   |
| `</p>`          | Balise fermante           |

---

# Les attributs

Les attributs donnent des informations supplémentaires à une balise.

Syntaxe :

```html
<balise attribut="valeur"></balise>
```

Exemple :

```html
<img src="photo.jpg" alt="Une photo" />
```

Ici :

- `src`
- `alt`

sont des attributs.

---

# La balise `<p>`

La balise `<p>` sert à créer un **paragraphe**.

Syntaxe :

```html
<p>Votre texte ici</p>
```

Exemple :

```html
<p>Bienvenue sur mon site.</p>
```

Résultat :

Bienvenue sur mon site.

---

# Les balises liées au texte

## Les titres

HTML possède 6 niveaux de titres.

```html
<h1>Titre principal</h1>
<h2>Sous-titre</h2>
<h3>Titre niveau 3</h3>
<h4>Titre niveau 4</h4>
<h5>Titre niveau 5</h5>
<h6>Titre niveau 6</h6>
```

---

## Texte important

### Gras

```html
<strong>Texte important</strong>
```

ou

```html
<b>Texte en gras</b>
```

---

### Italique

```html
<em>Texte important</em>
```

ou

```html
<i>Texte en italique</i>
```

---

### Souligné

```html
<u>Texte souligné</u>
```

---

### Texte barré

```html
<s>Texte barré</s>
```

---

### Petit texte

```html
<small>Petit texte</small>
```

---

### Exposant

```html
x<sup>2</sup>
```

Résultat :

x²

---

### Indice

```html
H<sub>2</sub>O
```

Résultat :

H₂O

---

### Saut de ligne

```html
<br />
```

---

### Ligne horizontale

```html
<hr />
```

---

# La balise `<input>`

La balise `<input>` permet de créer un champ de formulaire.

Contrairement à `<p>`, elle ne possède pas de balise fermante.

Syntaxe :

```html
<input type="text" />
```

---

# Les principaux attributs de `<input>`

```html
<input type="text" name="nom" id="nom" placeholder="Entrez votre nom" value="" required />
```

| Attribut    | Description                  |
| ----------- | ---------------------------- |
| type        | Définit le type du champ     |
| name        | Nom envoyé au serveur        |
| id          | Identifiant unique           |
| placeholder | Texte affiché dans le champ  |
| value       | Valeur par défaut            |
| required    | Rend le champ obligatoire    |
| disabled    | Désactive le champ           |
| readonly    | Lecture seule                |
| maxlength   | Nombre maximal de caractères |
| minlength   | Nombre minimal de caractères |

---

# L'attribut `type`

L'attribut **type** est le plus important de la balise `<input>`.

Il indique la nature du champ.

## type="text"

```html
<input type="text" />
```

Champ texte classique.

---

## type="password"

```html
<input type="password" />
```

Cache les caractères.

---

## type="email"

```html
<input type="email" />
```

Pour une adresse e-mail.

---

## type="number"

```html
<input type="number" />
```

Accepte uniquement des nombres.

---

## type="date"

```html
<input type="date" />
```

Sélection d'une date.

---

## type="time"

```html
<input type="time" />
```

Sélection d'une heure.

---

## type="color"

```html
<input type="color" />
```

Permet de choisir une couleur.

---

## type="file"

```html
<input type="file" />
```

Permet de sélectionner un fichier.

---

## type="checkbox"

```html
<input type="checkbox" />
```

Case à cocher.

---

## type="radio"

```html
<input type="radio" />
```

Bouton radio.

---

## type="range"

```html
<input type="range" />
```

Curseur.

---

## type="search"

```html
<input type="search" />
```

Champ de recherche.

---

## type="url"

```html
<input type="url" />
```

Pour une adresse web.

---

## type="tel"

```html
<input type="tel" />
```

Pour un numéro de téléphone.

---

## type="submit"

```html
<input type="submit" value="Envoyer" />
```

Bouton d'envoi.

---

## type="reset"

```html
<input type="reset" />
```

Réinitialise le formulaire.

---

## type="button"

```html
<input type="button" value="Cliquer" />
```

Bouton simple.

---

## type="hidden"

```html
<input type="hidden" />
```

Champ invisible.

---

# La balise `<textarea>`

La balise `<textarea>` permet d'écrire un texte sur plusieurs lignes.

Syntaxe :

```html
<textarea></textarea>
```

Exemple :

```html
<textarea rows="5" cols="30" placeholder="Votre message"></textarea>
```

## Attributs principaux

| Attribut    | Description                  |
| ----------- | ---------------------------- |
| rows        | Nombre de lignes             |
| cols        | Largeur                      |
| placeholder | Texte d'aide                 |
| maxlength   | Nombre maximal de caractères |
| required    | Champ obligatoire            |
| readonly    | Lecture seule                |

---

# La balise `<img>`

La balise `<img>` permet d'afficher une image.

Syntaxe :

```html
<img src="image.jpg" alt="Description" />
```

## Attributs

| Attribut | Description           |
| -------- | --------------------- |
| src      | Chemin de l'image     |
| alt      | Texte alternatif      |
| width    | Largeur               |
| height   | Hauteur               |
| loading  | Chargement de l'image |

Exemple :

```html
<img src="chat.jpg" alt="Un chat" width="300" height="200" />
```

---

# Les autres balises importantes à apprendre

## Structure de la page

- `<!DOCTYPE html>`
- `<html>`
- `<head>`
- `<body>`
- `<title>`
- `<meta>`
- `<link>`
- `<script>`

---

## Liens

```html
<a href=""></a>
```

---

## Les listes

Liste non ordonnée :

```html
<ul>
  <li>HTML</li>
  <li>CSS</li>
</ul>
```

Liste ordonnée :

```html
<ol>
  <li>HTML</li>
  <li>CSS</li>
</ol>
```

---

## Les divisions

```html
<div></div>
```

Division générique utilisée pour organiser la page.

---

## Les éléments en ligne

```html
<span></span>
```

Permet de cibler une partie d'un texte.

---

## Les formulaires

```html
<form></form>
```

Contient les champs de saisie.

---

## Les boutons

```html
<button>Cliquez</button>
```

---

## Les tableaux

- `<table>`
- `<tr>`
- `<td>`
- `<th>`
- `<thead>`
- `<tbody>`

---

# Résumé

Les premières balises à maîtriser sont :

- `html`
- `head`
- `body`
- `title`
- `meta`
- `h1` à `h6`
- `p`
- `strong`
- `em`
- `br`
- `hr`
- `a`
- `img`
- `div`
- `span`
- `ul`
- `ol`
- `li`
- `form`
- `label`
- `input`
- `textarea`
- `button`

Ces balises constituent la base du développement HTML et seront indispensables avant d'apprendre le CSS et JavaScript.

# 🎨 Introduction au CSS

## Qu'est-ce que le CSS ?

**CSS** (**Cascading Style Sheets**) est le langage utilisé pour mettre en forme une page HTML.

Avec le CSS, on peut :

- Changer les couleurs
- Modifier la taille du texte
- Ajouter des bordures
- Changer les polices d'écriture
- Modifier l'espacement
- Positionner les éléments
- Créer des animations

> **HTML crée la structure d'une page, tandis que CSS s'occupe de son apparence.**

---

# Comment ajouter du CSS ?

Il existe trois façons d'ajouter du CSS.

## 1. CSS en ligne (Inline)

```html
<p style="color: blue;">Bonjour</p>
```

Cette méthode est peu utilisée car elle mélange le HTML et le CSS.

---

## 2. CSS interne

```html
<head>
  <style>
    p {
      color: red;
    }
  </style>
</head>
```

---

## 3. CSS externe (Recommandé)

Fichier HTML

```html
<link rel="stylesheet" href="style.css" />
```

Fichier **style.css**

```css
p {
  color: red;
}
```

Cette méthode est la plus utilisée.

---

# Les sélecteurs CSS

Un sélecteur permet de choisir l'élément que l'on souhaite modifier.

Exemple :

```css
p {
  color: blue;
}
```

Tous les paragraphes seront affichés en bleu.

---

# L'attribut `class`

L'attribut **class** permet de donner un nom à un ou plusieurs éléments HTML afin de leur appliquer un style CSS.

Une même classe peut être utilisée sur plusieurs éléments.

## Syntaxe

HTML

```html
<p class="texte">Bonjour</p>
```

CSS

```css
.texte {
  color: red;
}
```

Le point (`.`) devant le nom de la classe est obligatoire en CSS.

---

## Une classe sur plusieurs éléments

```html
<h1 class="titre">Bienvenue</h1>

<p class="titre">Ceci est un paragraphe.</p>

<button class="titre">Cliquer</button>
```

CSS

```css
.titre {
  color: blue;
}
```

Tous les éléments ayant la classe **titre** auront la même couleur.

---

## Plusieurs classes sur un même élément

HTML

```html
<p class="texte important">Bonjour</p>
```

CSS

```css
.texte {
  color: black;
}

.important {
  font-weight: bold;
}
```

Un élément peut posséder plusieurs classes.

---

# Quelques propriétés CSS importantes

## Les propriétés du paragraphe (`p`)

### Changer la couleur

```css
p {
  color: blue;
}
```

---

### Changer la taille du texte

```css
p {
  font-size: 20px;
}
```

---

### Changer la police

```css
p {
  font-family: Arial;
}
```

---

### Mettre le texte en gras

```css
p {
  font-weight: bold;
}
```

---

### Centrer le texte

```css
p {
  text-align: center;
}
```

---

### Ajouter un espace intérieur

```css
p {
  padding: 20px;
}
```

---

### Ajouter une marge extérieure

```css
p {
  margin: 20px;
}
```

---

### Ajouter une couleur de fond

```css
p {
  background-color: lightblue;
}
```

---

### Ajouter une bordure

```css
p {
  border: 2px solid black;
}
```

---

# Les propriétés du champ `<input>`

```css
input {
  width: 300px;
}
```

Définit la largeur.

---

```css
input {
  height: 40px;
}
```

Définit la hauteur.

---

```css
input {
  padding: 10px;
}
```

Ajoute un espace intérieur.

---

```css
input {
  border: 1px solid gray;
}
```

Ajoute une bordure.

---

```css
input {
  border-radius: 8px;
}
```

Arrondit les coins.

---

```css
input {
  outline: none;
}
```

Supprime le contour de sélection par défaut.

---

```css
input {
  font-size: 16px;
}
```

Modifie la taille du texte.

---

# Les propriétés du bouton (`button`)

```css
button {
  background-color: blue;
}
```

Couleur de fond.

---

```css
button {
  color: white;
}
```

Couleur du texte.

---

```css
button {
  border: none;
}
```

Supprime la bordure.

---

```css
button {
  padding: 12px 25px;
}
```

Ajoute un espace intérieur.

---

```css
button {
  border-radius: 8px;
}
```

Arrondit les coins.

---

```css
button {
  cursor: pointer;
}
```

Transforme le curseur en main lorsque la souris passe sur le bouton.

---

```css
button {
  font-size: 18px;
}
```

Modifie la taille du texte.

---

# Les pseudo-classes et pseudo-éléments

Les pseudo-classes permettent de modifier l'apparence d'un élément selon son état.

Les pseudo-éléments permettent de cibler une partie précise d'un élément.

---

# `:hover`

S'applique lorsque la souris passe sur un élément.

```css
button:hover {
  background-color: green;
}
```

Exemple avec un paragraphe :

```css
p:hover {
  color: red;
}
```

---

# `:active`

S'applique pendant que l'utilisateur clique sur un élément.

```css
button:active {
  background-color: orange;
}
```

Ou avec un paragraphe :

```css
p:active {
  color: purple;
}
```

---

# `::first-letter`

Permet de modifier uniquement la première lettre d'un paragraphe.

```css
p::first-letter {
  font-size: 40px;
  color: red;
  font-weight: bold;
}
```

Résultat :

- La première lettre sera plus grande.
- Elle sera en rouge.
- Elle sera en gras.

---

# Résumé

Les notions essentielles à retenir sont :

- Le CSS sert à mettre en forme une page HTML.
- Les styles peuvent être ajoutés en ligne, en interne ou dans un fichier externe.
- Les sélecteurs permettent de choisir les éléments à modifier.
- L'attribut **class** permet d'appliquer le même style à plusieurs éléments.
- Les propriétés CSS modifient l'apparence des éléments.
- Les pseudo-classes (`:hover`, `:active`) réagissent aux actions de l'utilisateur.
- Les pseudo-éléments (`::first-letter`) permettent de styliser une partie spécifique d'un élément.
