---

# Illustration de `justify-content`

La propriété `justify-content` déplace les éléments **horizontalement** (sur l'axe principal).

## `justify-content: start`

```
+--------------------------------------+
| ■  ■  ■                             |
+--------------------------------------+
```

Les éléments sont alignés **au début** (à gauche) du conteneur.

---

## `justify-content: center`

```
+--------------------------------------+
|          ■  ■  ■                     |
+--------------------------------------+
```

Les éléments sont placés **au centre** du conteneur.

---

## `justify-content: end`

```
+--------------------------------------+
|                           ■  ■  ■    |
+--------------------------------------+
```

Les éléments sont alignés **à la fin** (à droite) du conteneur.

---

# Illustration de `align-items`

La propriété `align-items` déplace les éléments **verticalement** (sur l'axe secondaire).

> Le conteneur possède une hauteur (`height: 200px`) afin de visualiser l'alignement.

## `align-items: start`

```
+----------------------+
|   ■  ■  ■            |
|                      |
|                      |
|                      |
+----------------------+
```

Les éléments sont placés **en haut** du conteneur.

---

## `align-items: center`

```
+----------------------+
|                      |
|    ■  ■  ■           |
|                      |
|                      |
+----------------------+
```

Les éléments sont placés **au milieu** du conteneur.

---

## `align-items: end`

```
+----------------------+
|                      |
|                      |
|                      |
|   ■  ■  ■            |
+----------------------+
```

Les éléments sont placés **en bas** du conteneur.

---

# Comparaison visuelle

| `justify-content`                            | `align-items`                            |
| -------------------------------------------- | ---------------------------------------- |
| Déplace les éléments de **gauche à droite**. | Déplace les éléments de **haut en bas**. |

```
JUSTIFY-CONTENT (Horizontal)

start
+----------------------------+
|■■■                         |
+----------------------------+

center
+----------------------------+
|         ■■■                |
+----------------------------+

end
+----------------------------+
|                     ■■■    |
+----------------------------+


ALIGN-ITEMS (Vertical)

start
+-------------+
|■■■          |
|             |
|             |
+-------------+

center
+-------------+
|             |
|■■■          |
|             |
+-------------+

end
+-------------+
|             |
|             |
|■■■          |
+-------------+
```

> **Astuce :**
>
> - **`justify-content`** → déplace les éléments **de gauche à droite (↔)**.
> - **`align-items`** → déplace les éléments **de haut en bas (↕)**.
>
> Si `flex-direction: column`, les axes sont inversés :
>
> - `justify-content` agit de **haut en bas**.
> - `align-items` agit de **gauche à droite**.
