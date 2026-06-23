# HTML Tags Cheatsheet
> Quick reference for all tags covered in lessons + essential everyday tags.

---

## Table of Contents
1. [Document Structure](#1-document-structure)
2. [Text & Headings](#2-text--headings)
3. [Lists](#3-lists)
4. [Links](#4-links)
5. [Images & Media](#5-images--media)
6. [Forms & Inputs](#6-forms--inputs)
7. [Layout & Grouping](#7-layout--grouping)
8. [Utility / Misc](#8-utility--misc)

---

## 1. Document Structure

### `<!DOCTYPE html>`
Tells the browser this is an HTML5 document. Always the very first line.
```html
<!DOCTYPE html>
```
> No attributes. Not a real tag — it's a declaration.

---

### `<html>`
The root element that wraps the entire page.
```html
<html lang="en"> ... </html>
```
| Attribute | Description |
|-----------|-------------|
| `lang` | Language of the page (e.g. `"en"`, `"fr"`) |

---

### `<head>`
Container for metadata — not visible on the page.
```html
<head>
    <title>My Page</title>
</head>
```
> No commonly used attributes.

---

### `<title>`
Sets the text shown on the browser tab.
```html
<title>My Awesome Page</title>
```
> No attributes.

---

### `<body>`
Contains all the visible content of the page.
```html
<body> ... </body>
```
> No commonly used attributes.

---

## 2. Text & Headings

### `<h1>` – `<h6>`
Six levels of headings. `<h1>` is the largest/most important, `<h6>` is the smallest.
```html
<h1>Main Title</h1>
<h2>Section Title</h2>
<h3>Sub-section</h3>
```
| Attribute | Description |
|-----------|-------------|
| `id` | Unique identifier for the element |
| `class` | CSS class name(s) |
| `style` | Inline CSS styles |

---

### `<p>`
Defines a paragraph of text.
```html
<p>This is a paragraph.</p>
```
| Attribute | Description |
|-----------|-------------|
| `id` | Unique identifier |
| `class` | CSS class name(s) |
| `style` | Inline CSS styles |

---

### `<strong>`
Makes text **bold** — also signals importance to browsers/screen readers.
```html
<strong>Important text</strong>
```

---

### `<em>`
Makes text *italic* — signals emphasis.
```html
<em>Emphasized text</em>
```

---

## 3. Lists

### `<ol>`
Ordered (numbered) list container.
```html
<ol>
    <li>First item</li>
    <li>Second item</li>
</ol>
```
| Attribute | Description |
|-----------|-------------|
| `type` | Numbering style: `"1"` (default), `"A"`, `"a"`, `"I"`, `"i"` |
| `start` | Starting number (e.g. `start="5"` begins at 5) |
| `reversed` | Counts down instead of up |

---

### `<ul>`
Unordered (bulleted) list container.
```html
<ul>
    <li>Apples</li>
    <li>Oranges</li>
</ul>
```
| Attribute | Description |
|-----------|-------------|
| `style` | Can use `list-style-type` to change bullet style |

---

### `<li>`
A single list item. Used inside `<ol>` or `<ul>`.
```html
<li>List item</li>
```
| Attribute | Description |
|-----------|-------------|
| `value` | Sets the number for that item in `<ol>` |

---

## 4. Links

### `<a>`
Anchor tag — creates a hyperlink.
```html
<a href="https://example.com" target="_blank">Visit Example</a>
```
| Attribute | Description |
|-----------|-------------|
| `href` | URL the link points to |
| `target` | Where to open: `"_blank"` (new tab), `"_self"` (same tab) |
| `title` | Tooltip text shown on hover |
| `rel` | Relationship (e.g. `"noopener noreferrer"` for security with `_blank`) |
| `download` | Prompts a file download instead of navigation |

---

## 5. Images & Media

### `<img>` *(self-closing)*
Embeds an image. The `src` must be a **direct image URL** (ending in `.jpg`, `.png`, etc.), not a webpage link.
```html
<img src="path/to/image.jpg" alt="Description" width="420" height="690">
```
| Attribute | Description |
|-----------|-------------|
| `src` | Path or URL of the image (**must be a direct image link**) |
| `alt` | Alternate text — shown if image fails, important for accessibility |
| `width` | Width in pixels (or %) |
| `height` | Height in pixels |
| `title` | Tooltip on hover |
| `loading` | `"lazy"` defers loading until image is near the viewport |

---

## 6. Forms & Inputs

### `<form>`
Container for all form elements. Data is submitted when the user hits submit.
```html
<form action="/submit" method="POST"> ... </form>
```
| Attribute | Description |
|-----------|-------------|
| `action` | URL where form data is sent |
| `method` | HTTP method: `"GET"` or `"POST"` |
| `enctype` | Encoding type — use `"multipart/form-data"` for file uploads |
| `novalidate` | Disables HTML5 built-in validation |

---

### `<input>` *(self-closing)*
The most versatile form element — changes behaviour based on `type`.
```html
<input type="text" id="username" name="username" placeholder="Enter name" required>
```
| Attribute | Description |
|-----------|-------------|
| `type` | Input kind: `text`, `password`, `email`, `number`, `checkbox`, `radio`, `file`, `date`, `submit`, `reset` |
| `name` | Key sent with the form data |
| `id` | Links to a `<label>` via `for` attribute |
| `value` | Default value |
| `placeholder` | Hint text shown inside the field |
| `required` | Field must be filled before submission |
| `disabled` | Greys out and disables the field |
| `readonly` | Value visible but not editable |
| `min` / `max` | Min/max values for `number`, `date` types |
| `minlength` / `maxlength` | Min/max character length for text inputs |
| `pattern` | Regex the value must match |
| `checked` | Pre-checks a `checkbox` or `radio` |

---

### `<label>`
Describes an input field. Clicking it focuses the linked input — improves accessibility and UX.
```html
<label for="username">Username :</label>
<input type="text" id="username" name="username">
```
| Attribute | Description |
|-----------|-------------|
| `for` | Must match the `id` of the input it labels |

---

### `<button>`
A clickable button inside or outside a form.
```html
<button type="submit">Login</button>
<button type="reset">Reset</button>
<button type="button">Click Me</button>
```
| Attribute | Description |
|-----------|-------------|
| `type` | `"submit"` (submits form), `"reset"` (clears form), `"button"` (no default action) |
| `disabled` | Greys out the button |

---

### `<select>`
Creates a dropdown list. Must be nested inside `<form>`.
```html
<select name="color">
    <option disabled>Choose a color</option>
    <option value="red">Red</option>
    <option value="green" selected>Green</option>
</select>
```
| Attribute | Description |
|-----------|-------------|
| `name` | Key sent with form data |
| `multiple` | Allows selecting more than one option |
| `size` | Number of visible options (shows as a list box) |
| `required` | Forces the user to select an option |

---

### `<option>`
A single item inside `<select>`.
```html
<option value="blue">Blue</option>
```
| Attribute | Description |
|-----------|-------------|
| `value` | The value sent with form data |
| `selected` | Makes this option the default selection |
| `disabled` | Greys out the option (useful for placeholder options) |

---

### `<textarea>`
A multi-line text input field.
```html
<textarea name="message" rows="10" cols="40" placeholder="Type here..."></textarea>
```
| Attribute | Description |
|-----------|-------------|
| `name` | Key sent with form data |
| `rows` | Visible number of lines |
| `cols` | Visible width in characters |
| `placeholder` | Hint text |
| `required` | Must be filled before submission |
| `maxlength` | Max number of characters allowed |
| `readonly` | Value visible but not editable |
| `disabled` | Greys out the field |

---

## 7. Layout & Grouping

### `<div>`
A **block-level** container — takes up the full width of its row. Used to group and style sections.
```html
<div class="card">
    <h2>Title</h2>
    <p>Some content.</p>
</div>
```
| Attribute | Description |
|-----------|-------------|
| `id` | Unique identifier |
| `class` | CSS class name(s) for styling |
| `style` | Inline CSS |

---

### `<span>`
An **inline** container — wraps text without breaking the line. Used to style part of text.
```html
<p>The sky is <span style="color:blue">blue</span>.</p>
```
| Attribute | Description |
|-----------|-------------|
| `id` | Unique identifier |
| `class` | CSS class name(s) |
| `style` | Inline CSS |

---

## 8. Utility / Misc

### `<br>` *(self-closing)*
Inserts a line break inside text — like pressing Enter.
```html
Line one.<br>Line two.
```
> No attributes.

---

### `<hr>` *(self-closing)*
Draws a horizontal divider line across the page.
```html
<h1>Section Title</h1>
<hr>
<p>Content below the line.</p>
```
> No commonly used attributes (styling is done via CSS).

---

### `<script>`
Embeds or links JavaScript. Usually placed just before `</body>`.
```html
<!-- Inline JS -->
<script>
    alert("Hello!");
</script>

<!-- External JS file -->
<script src="app.js"></script>
```
| Attribute | Description |
|-----------|-------------|
| `src` | Path to an external `.js` file |
| `defer` | Runs script after page has loaded (recommended) |
| `async` | Runs script as soon as it's downloaded |
| `type` | Usually omitted; default is `"text/javascript"` |

---

### `<link>` *(self-closing)*
Links external resources — most commonly a CSS stylesheet. Goes inside `<head>`.
```html
<link rel="stylesheet" href="style.css">
```
| Attribute | Description |
|-----------|-------------|
| `rel` | Relationship type — always `"stylesheet"` for CSS |
| `href` | Path to the external file |
| `type` | Usually omitted; default is `"text/css"` |

---

### `<meta>` *(self-closing)*
Provides metadata about the page. Goes inside `<head>`.
```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
| Attribute | Description |
|-----------|-------------|
| `charset` | Character encoding — always use `"UTF-8"` |
| `name` | Type of metadata: `"viewport"`, `"description"`, `"author"` |
| `content` | Value for the `name` or `http-equiv` attribute |

---

> **Tip**: The tags `<img>`, `<input>`, `<br>`, `<hr>`, `<link>`, and `<meta>` are all **self-closing** — they don't need a closing tag.
