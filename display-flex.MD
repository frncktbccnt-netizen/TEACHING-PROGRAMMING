# Understanding `start`, `center`, and `end` in Flexbox

Both **`justify-content`** and **`align-items`** use the values `start`, `center`, and `end` to position elements. The difference is **which axis they control**.

> **Remember:**
>
> - `justify-content` → Controls the **main axis**.
> - `align-items` → Controls the **cross axis**.

When `flex-direction: row` (the default):

- **Main axis** = Horizontal (Left → Right)
- **Cross axis** = Vertical (Top → Bottom)

---

# 1. `justify-content`

`justify-content` positions **all flex items** along the **main (horizontal) axis**.

## `justify-content: start`

Places all items at the **beginning (left side)** of the container.

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

### Result

```
+--------------------------------+
| [1] [2] [3]                    |
+--------------------------------+
```

### Explanation

- Items begin from the **left**.
- There is **no extra space before the first item**.
- Any remaining space stays on the **right**.

---

## `justify-content: center`

Places all items in the **middle** of the container.

### CSS

```css
.container {
  display: flex;
  justify-content: center;
}
```

### Result

```
+--------------------------------+
|        [1] [2] [3]             |
+--------------------------------+
```

### Explanation

- Empty space is divided equally on both sides.
- The group of items stays together.
- Useful for centering menus, buttons, or cards.

---

## `justify-content: end`

Places all items at the **end (right side)** of the container.

### CSS

```css
.container {
  display: flex;
  justify-content: end;
}
```

### Result

```
+--------------------------------+
|                    [1] [2] [3] |
+--------------------------------+
```

### Explanation

- All items move to the **right**.
- Empty space appears on the **left**.
- Often used to align buttons or actions to the right.

---

# Summary of `justify-content`

| Value    | Position |
| -------- | -------- |
| `start`  | Left     |
| `center` | Middle   |
| `end`    | Right    |

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

`align-items` positions flex items on the **cross (vertical) axis**.

To see the effect clearly, the container needs a height.

```css
.container {
  display: flex;
  height: 200px;
}
```

---

## `align-items: start`

Places items at the **top** of the container.

### CSS

```css
.container {
  display: flex;
  align-items: start;
  height: 200px;
}
```

### Result

```
+----------------------+
| [1] [2] [3]          |
|                      |
|                      |
|                      |
+----------------------+
```

### Explanation

- Items stay at the **top**.
- No empty space above them.
- Remaining space is below.

---

## `align-items: center`

Places items in the **vertical center**.

### CSS

```css
.container {
  display: flex;
  align-items: center;
  height: 200px;
}
```

### Result

```
+----------------------+
|                      |
|     [1] [2] [3]      |
|                      |
+----------------------+
```

### Explanation

- Equal space above and below the items.
- Very useful for vertically centering text, icons, or buttons.

---

## `align-items: end`

Places items at the **bottom** of the container.

### CSS

```css
.container {
  display: flex;
  align-items: end;
  height: 200px;
}
```

### Result

```
+----------------------+
|                      |
|                      |
|                      |
| [1] [2] [3]          |
+----------------------+
```

### Explanation

- Items move to the **bottom**.
- Empty space appears above them.
- Useful for aligning elements to the bottom of a card or section.

---

# Summary of `align-items`

| Value    | Position |
| -------- | -------- |
| `start`  | Top      |
| `center` | Middle   |
| `end`    | Bottom   |

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

# Side-by-Side Comparison

| Property          | Controls               | `start` | `center` | `end`  |
| ----------------- | ---------------------- | ------- | -------- | ------ |
| `justify-content` | Horizontal (main axis) | Left    | Middle   | Right  |
| `align-items`     | Vertical (cross axis)  | Top     | Middle   | Bottom |

---

# Easy Way to Remember

Imagine a TV screen:

```
+--------------------------------------+
| Top                                  |
|                                      |
|          Center                      |
|                                      |
| Bottom                               |
+--------------------------------------+
```

- **`justify-content`** moves items **left ↔ right**.
- **`align-items`** moves items **up ↕ down**.

If `flex-direction` changes to `column`, the axes also change:

- `justify-content` controls **top ↕ bottom**.
- `align-items` controls **left ↔ right**.

This is why it is important to remember **the axis**, not just "horizontal" or "vertical."
