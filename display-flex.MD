# Comprendre `start`, `center` et `end` avec Flexbox

Les propriétés **`justify-content`** et **`align-items`** utilisent les valeurs `start`, `center` et `end` pour positionner les éléments. La différence est **l'axe sur lequel elles agissent**.

> **À retenir :**
>
> - `justify-content` → Contrôle **l'axe principal**.
> - `align-items` → Contrôle **l'axe secondaire**.

Lorsque `flex-direction: row` (valeur par défaut) :

- **Axe principal** = Horizontal (Gauche → Droite)
- **Axe secondaire** = Vertical (Haut → Bas)

---

# 1. `justify-content`

La propriété **`justify-content`** permet d'aligner **tous les éléments flexibles** sur **l'axe principal (horizontal)**.

## `justify-content: start`

Place tous les éléments **au début (à gauche)** du conteneur.

### CSS

```css
.container {
  display: flex;
  justify-content: start;
}
```

### HTML

```html
<div class="container">
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div>
```

### Résultat

```
+--------------------------------+
| [1] [2] [3]                    |
+--------------------------------+
```

### Explication

- Les éléments commencent **à gauche**.
- Il n'y a **aucun espace avant le premier élément**.
- Tout l'espace restant se trouve **à droite**.

---

## `justify-content: center`

Place tous les éléments **au centre** du conteneur.

### CSS

```css
.container {
  display: flex;
  justify-content: center;
}
```

### Résultat

```
+--------------------------------+
|        [1] [2] [3]             |
+--------------------------------+
```

### Explication

- L'espace vide est réparti de manière égale à gauche et à droite.
- Les éléments restent regroupés.
- Très utile pour centrer un menu, des boutons ou des cartes.

---

## `justify-content: end`

Place tous les éléments **à la fin (à droite)** du conteneur.

### CSS

```css
.container {
  display: flex;
  justify-content: end;
}
```

### Résultat

```
+--------------------------------+
|                    [1] [2] [3] |
+--------------------------------+
```

### Explication

- Tous les éléments sont déplacés **à droite**.
- L'espace vide apparaît **à gauche**.
- Cette valeur est souvent utilisée pour aligner des boutons d'action à droite.

---

# Résumé de `justify-content`

| Valeur   | Position |
| -------- | -------- |
| `start`  | Gauche   |
| `center` | Centre   |
| `end`    | Droite   |

```
start
[1][2][3]____________

center
_____[1][2][3]_____

end
____________[1][2][3]
```

---

# 2. `align-items`

La propriété **`align-items`** permet d'aligner les éléments sur **l'axe secondaire (vertical)**.

Pour voir son effet, le conteneur doit avoir une hauteur.

```css
.container {
  display: flex;
  height: 200px;
}
```

---

## `align-items: start`

Place les éléments **en haut** du conteneur.

### CSS

```css
.container {
  display: flex;
  align-items: start;
  height: 200px;
}
```

### Résultat

```
+----------------------+
| [1] [2] [3]          |
|                      |
|                      |
|                      |
+----------------------+
```

### Explication

- Les éléments restent **en haut**.
- Aucun espace n'est laissé au-dessus.
- Tout l'espace restant est situé en dessous.

---

## `align-items: center`

Place les éléments **au centre verticalement**.

### CSS

```css
.container {
  display: flex;
  align-items: center;
  height: 200px;
}
```

### Résultat

```
+----------------------+
|                      |
|     [1] [2] [3]      |
|                      |
+----------------------+
```

### Explication

- Les éléments sont placés au milieu.
- L'espace est réparti de façon égale au-dessus et en dessous.
- Très utile pour centrer verticalement du texte, des icônes ou des boutons.

---

## `align-items: end`

Place les éléments **en bas** du conteneur.

### CSS

```css
.container {
  display: flex;
  align-items: end;
  height: 200px;
}
```

### Résultat

```
+----------------------+
|                      |
|                      |
|                      |
| [1] [2] [3]          |
+----------------------+
```

### Explication

- Les éléments sont déplacés **en bas**.
- L'espace vide apparaît **au-dessus**.
- Cette valeur est utile pour aligner des éléments au bas d'une carte ou d'une section.

---

# Résumé de `align-items`

| Valeur   | Position |
| -------- | -------- |
| `start`  | Haut     |
| `center` | Milieu   |
| `end`    | Bas      |

```
start
+---------+
| [1][2]  |
|         |
|         |
+---------+

center
+---------+
|         |
| [1][2]  |
|         |
+---------+

end
+---------+
|         |
|         |
| [1][2]  |
+---------+
```

---

# Comparaison des deux propriétés

| Propriété         | Contrôle       | `start` | `center` | `end`  |
| ----------------- | -------------- | ------- | -------- | ------ |
| `justify-content` | Axe principal  | Gauche  | Centre   | Droite |
| `align-items`     | Axe secondaire | Haut    | Centre   | Bas    |

---

# Astuce pour retenir

Imaginez un écran :

```
+--------------------------------------+
| Haut                                 |
|                                      |
|               Centre                 |
|                                      |
| Bas                                  |
+--------------------------------------+
```

- **`justify-content`** déplace les éléments de **gauche à droite (↔)**.
- **`align-items`** déplace les éléments de **haut en bas (↕)**.

> **Attention :**
>
> Si `flex-direction` devient `column`, les axes changent également :
>
> - `justify-content` contrôle alors **le haut et le bas**.
> - `align-items` contrôle **la gauche et la droite**.

C'est pourquoi il est préférable de retenir **l'axe principal** et **l'axe secondaire**, plutôt que simplement **horizontal** ou **vertical**.
