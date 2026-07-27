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
