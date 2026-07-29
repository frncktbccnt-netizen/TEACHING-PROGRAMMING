# Display Flex (CSS)

## `display: flex`

La propriété **`display: flex`** transforme un élément HTML en **conteneur flexible (Flexbox)**.  
Tous les éléments enfants deviennent des **éléments flexibles** et peuvent être alignés facilement sur une ligne ou une colonne.

### Exemple

```css
.container {
  display: flex;
}
```

```html
<div class="container">
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div>
```

**Résultat :** les éléments `1`, `2` et `3` s'affichent sur une même ligne.

---

# `justify-content`

La propriété **`justify-content`** permet d'aligner les éléments sur **l'axe principal**.

> **Par défaut :**
>
> - Axe principal = **horizontal** (gauche → droite)

## Les principales valeurs

| Valeur          | Description                                                                           |
| --------------- | ------------------------------------------------------------------------------------- |
| `flex-start`    | Les éléments commencent au début du conteneur.                                        |
| `center`        | Les éléments sont centrés horizontalement.                                            |
| `flex-end`      | Les éléments sont placés à la fin du conteneur.                                       |
| `space-between` | Le premier et le dernier touchent les bords, l'espace est réparti entre les éléments. |
| `space-around`  | Chaque élément possède un espace autour de lui.                                       |
| `space-evenly`  | Tous les espaces sont exactement égaux.                                               |

### Exemple 1 : `center`

```css
.container {
  display: flex;
  justify-content: center;
}
```

**Résultat :**

```
      [1] [2] [3]
```

---

### Exemple 2 : `space-between`

```css
.container {
  display: flex;
  justify-content: space-between;
}
```

**Résultat :**

```
[1]                [2]                [3]
```

---

### Exemple 3 : `flex-end`

```css
.container {
  display: flex;
  justify-content: flex-end;
}
```

**Résultat :**

```
                     [1] [2] [3]
```

---

# `align-items`

La propriété **`align-items`** aligne les éléments sur **l'axe secondaire**.

> **Par défaut :**
>
> - Axe secondaire = **vertical** (haut → bas)

## Les principales valeurs

| Valeur       | Description                                                  |
| ------------ | ------------------------------------------------------------ |
| `stretch`    | Les éléments s'étirent pour remplir la hauteur du conteneur. |
| `flex-start` | Les éléments sont alignés en haut.                           |
| `center`     | Les éléments sont centrés verticalement.                     |
| `flex-end`   | Les éléments sont alignés en bas.                            |
| `baseline`   | Les textes sont alignés sur leur ligne de base.              |

### Exemple 1 : `center`

```css
.container {
  display: flex;
  align-items: center;
  height: 200px;
}
```

**Résultat :**

```
+----------------------+
|                      |
|      [1] [2] [3]     |
|                      |
+----------------------+
```

---

### Exemple 2 : `flex-start`

```css
.container {
  display: flex;
  align-items: flex-start;
  height: 200px;
}
```

**Résultat :**

```
+----------------------+
| [1] [2] [3]          |
|                      |
|                      |
+----------------------+
```

---

### Exemple 3 : `flex-end`

```css
.container {
  display: flex;
  align-items: flex-end;
  height: 200px;
}
```

**Résultat :**

```
+----------------------+
|                      |
|                      |
| [1] [2] [3]          |
+----------------------+
```

---

# Exemple complet

```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
```

```html
<div class="container">
  <button>Connexion</button>
</div>
```

### Résultat

Le bouton est **parfaitement centré** :

- Horizontalement grâce à `justify-content: center`
- Verticalement grâce à `align-items: center`

---

# Astuce pour retenir

| Propriété         | Agit sur                              |
| ----------------- | ------------------------------------- |
| `justify-content` | Axe principal (horizontal par défaut) |
| `align-items`     | Axe secondaire (vertical par défaut)  |

## Mémo

- ↔ **Gauche / Droite** → `justify-content`
- ↕ **Haut / Bas** → `align-items`

---

# Résumé

```css
.container {
  display: flex; /* Active Flexbox */
  justify-content: center; /* Centre horizontalement */
  align-items: center; /* Centre verticalement */
}
```

**À retenir :**

- `display: flex` → Active Flexbox.
- `justify-content` → Déplace les éléments sur l'axe principal.
- `align-items` → Déplace les éléments sur l'axe secondaire.
- Les deux propriétés sont souvent utilisées ensemble pour centrer des éléments.
