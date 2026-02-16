
---
# <center>*__HTML Lessons__*
---
## **Lessons by @ezsnippet – IG [Neeraj Wallia]**

---
### 1. What is Web Development?
Web development is the process of creating and building websites. It involves:

- Designing
- Adding functionalities (buttons, forms, etc.)

**Example**: Building a house.

**To build a basic website you need**:
- HTML
- CSS
- JavaScript

---
### 2. How the Web Works – Client-Server Model

#### Client
- The **consumer** of the service (device/software that makes a request)
- Examples: Browser, mobile app, etc.
- Main responsibilities:
  - Displaying data
  - User interaction

#### Server
- The **provider** of the service
- Listens for requests from clients and sends back responses
- Main responsibilities:
  - Store data
  - Set up rules
  - Serve data

---
### 3. Recommended Tools & VS Code Extensions
Use **VS Code** and install these extensions:

- **Live Server**
- **Prettier**
- **Auto Rename Tag**

---
### 4. The Three Core Technologies

**HTML** – HyperText Markup Language  
→ Skeleton / structure of the website  
- Uses tags: `<h1>`, `<p>`, `<div>`, etc.  
- Does **not** handle styling or functionality.

**CSS** – Cascading Style Sheets  
→ Appearance / skin of the website  
- Adds colors, fonts, spacing, animations, etc.

**JavaScript**  
→ Functionality / behavior of the website (dynamic updates, interactions, etc.)  
- Written inside `<script></script>` tags.

---
### 5. First Webpage – HTML Basics

**Code Editor**: VS Code

**HTML Tags** are the fundamental building blocks of HTML.  
They tell the browser **how** to display content.  
Example: `<p>` tag displays text as a paragraph.

---
### 6. Basic HTML Structure

```html
<!DOCTYPE html>          <!-- 1. Document Type -->
<html>                   <!-- 2. Root element -->
<head>                   <!-- 3. Metadata -->
    <title>Page Title</title>
</head>
<body>                   <!-- 4. Visible content -->
    <!-- Your content goes here -->
</body>
</html>
```

- **Title tag**: Text that appears on the browser tab

---
### 7. HTML Text – Headings
There are **6 levels** of headings:

```html
<h1>Biggest heading</h1>
<h2>Second level</h2>
<h3>Third level</h3>
<h4>Fourth level</h4>
<h5>Fifth level</h5>
<h6>Smallest heading</h6>
```

---
### 8. HTML Lists

**Ordered List** (`<ol>` + `<li>`)

**Unordered List** (`<ul>` + `<li>`)

**Nested Lists** (lists inside lists)

---
### 10. ID in HTML
- `id` attribute gives a **unique identifier** to an element
- Used for styling in CSS and selecting in JavaScript

**Example**

```html
<p id="myElement">This paragraph is red</p>
```

```css
#myElement {
    color: red;
}
```

---
### 11. Self-Closing Tags
Two types of tags:

1. **Normal tags** → have opening and closing tags  
   `<p>This is a paragraph</p>`

2. **Self-closing tags** → close themselves (no content inside)  
   Examples: `<img>`, `<input>`, `<br>`, `<hr>`

### 12. Image Tag (Self-closing)

---
```html
<img src="path/to/image.jpg" alt="Description" width="420" height="690">
```

**Attributes**:
- `src` → source of the image
- `alt` → alternate text (important for accessibility)
- `width` / `height` → control size (px)

**Post link**: https://www.instagram.com/p/DHAOWfcyF7R/

---
### 13. Forms
Forms are HTML structures that allow users to input data (text fields, buttons, checkboxes, etc.).

---

**Note**: Section 9 was missing in the original notes.

This is a clean, well-structured, and properly formatted version of the entire lesson series. You can copy-paste it directly into any Markdown viewer (Notion, Obsidian, GitHub, etc.). Let me know if you want any section expanded with code examples!

---

### 14. Form Validation

- This prevents from submitting incomplete or incorrect data.
- HTML`5` attribures : 
    - `required` : Forces a field to be filled out before submission
    - `type` : specifies the expected input type (eg : email, numbrs, date).
    - `pattern` : Allows defining a regular expression for the input.
    - `min, max` : sets minimum & maximum values for numeric inputs.
    - `minlength, maxlength` : sets minimum & maximum lengths for text inputs.
    ```html
    <!--Creating a login form-->
    <form>
        <!--We want the username field to be mandatory hence we will be using the required attribute-->
        <!--This will not allow us to submit.-->
        Username <input type="text" required> 
        <br>
        <br>
        Password <input type="password" required minlength="6">
        <br>
        <br>
        <input type="submit">
    </form>
    ```

---
