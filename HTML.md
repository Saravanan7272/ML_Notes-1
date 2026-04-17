# HTML

## HTML5 – Complete Professional Tags & Attributes Reference

---

## 🌐 1. Document Structure

```html
<!DOCTYPE html> <!-- Defines HTML5 document -->
<html lang="en"> <!-- Root element; lang=en, ta, hi -->
<head> <!-- Metadata container -->
  <meta charset="UTF-8"> <!-- Character encoding -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- Responsive layout -->
  <title>Page Title</title> <!-- Browser title -->
</head>
<body> <!-- Visible content -->
</body>
</html>

```

**Common attributes**: `lang`, `dir=ltr|rtl`

---

## 🧠 2. Metadata Tags (`<head>`)

```html
<meta charset="UTF-8">
<meta name="description" content="HTML reference">
<meta name="keywords" content="HTML, tags">
<meta name="author" content="Developer">
<meta http-equiv="refresh" content="5">
<link rel="stylesheet" href="style.css">
<link rel="icon" href="favicon.ico">
<style> body { color: black; } </style>
<script src="app.js" defer></script>
<base href="https://example.com/">

```

---

## ✍️ 3. Text & Formatting

```html
<p>Paragraph</p>
<b>Bold</b>
<strong>Important</strong>
<i>Italic</i>
<em>Emphasized</em>
<u>Underline</u>
<mark>Highlight</mark>
<small>Small text</small>
<del>Deleted</del>
<ins>Inserted</ins>
<sub>Subscript</sub>
<sup>Superscript</sup>
<br> <!-- Line break -->
<hr> <!-- Horizontal rule -->

```

---

## 🏷️ 4. Headings

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>

```

---

## 📋 5. Lists

```html
<ul type="disc|circle|square">
  <li>Item</li>
</ul>

<ol type="1|A|a|I|i" start="1">
  <li>Item</li>
</ol>

<dl>
  <dt>Term</dt>
  <dd>Description</dd>
</dl>

```

---

## 🔗 6. Links & Media

```html
<a href="https://example.com" target="_blank" rel="noopener">Link</a>

<img src="img.png" alt="desc" width="100" height="100" loading="lazy">

<audio controls autoplay muted loop>
  <source src="sound.mp3" type="audio/mpeg">
</audio>

<video controls width="300" poster="thumb.jpg">
  <source src="video.mp4" type="video/mp4">
</video>

```

---

## 📊 7. Tables

```html
<table border="1">
  <caption>Table Title</caption>
  <thead>
    <tr><th>H1</th><th>H2</th></tr>
  </thead>
  <tbody>
    <tr><td>A</td><td>B</td></tr>
  </tbody>
  <tfoot>
    <tr><td colspan="2">Footer</td></tr>
  </tfoot>
</table>

```

Attributes: `rowspan`, `colspan`, `scope`

---

## 📝 8. Forms & Inputs (EXHAUSTIVE – Developer Grade)

### `<form>` — Form container

```html
<form action="/submit" method="get|post" enctype="application/x-www-form-urlencoded|multipart/form-data|text/plain"
      target="_self|_blank" autocomplete="on|off" novalidate name="myForm">
</form>

```

**Attributes**

- `action` → URL to submit data
- `method` → HTTP method (`get`, `post`)
- `enctype` → Encoding type (required for file upload)
- `target` → Where response opens
- `autocomplete` → Browser autofill
- `novalidate` → Disable HTML validation
- `name` → Form identifier

---

### `<input>` — Single-line form control

```html
<input type="text" name="username" value="" placeholder="Enter name"
       required minlength="3" maxlength="20"
       readonly disabled autofocus autocomplete="on"
       pattern="[A-Za-z]+" inputmode="text"
       min="0" max="100" step="1"
       checked multiple accept="image/*"
       list="datalistId" form="formId">

```

### All `type` values

```
text, password, email, number, tel, url, search
checkbox, radio, range, color
file, hidden, image, submit, reset, button
date, time, datetime-local, month, week

```

### Common `<input>` attributes

- `type` → Control type
- `name` → Key sent to server
- `value` → Default value
- `placeholder` → Hint text
- `required` → Mandatory field
- `readonly` → Not editable
- `disabled` → Not submitted
- `min`, `max`, `step` → Numeric/date limits
- `minlength`, `maxlength` → Text limits
- `pattern` → Regex validation
- `checked` → Default selection (radio/checkbox)
- `multiple` → Multiple values (file/email)
- `accept` → Allowed file types
- `autocomplete` → Autofill behavior
- `autofocus` → Focus on load
- `list` → Connects to `<datalist>`
- `form` → Associate with external form

---

### `<textarea>` — Multi-line text

```html
<textarea name="message" rows="5" cols="40"
          minlength="10" maxlength="500"
          placeholder="Type here" required
          readonly disabled wrap="soft|hard"></textarea>

```

**Attributes**: `rows`, `cols`, `wrap`, `minlength`, `maxlength`, `placeholder`

---

### `<select>` / `<option>` / `<optgroup>`

```html
<select name="country" multiple size="3" required disabled>
  <optgroup label="Asia">
    <option value="in" selected>India</option>
  </optgroup>
</select>

```

**`<select>` attributes**: `multiple`, `size`, `required`, `disabled`

**`<option>` attributes**: `value`, `selected`, `disabled`, `label`

---

### `<button>` — Clickable button

```html
<button type="submit|reset|button" name="btn" value="ok" disabled autofocus>
  Submit
</button>

```

---

### `<label>`

```html
<label for="userId">Username</label>

```

- `for` → Links label to input `id`

---

### `<fieldset>` / `<legend>`

```html
<fieldset disabled>
  <legend>User Info</legend>
</fieldset>

```

---

### `<datalist>` — Input suggestions

```html
<datalist id="skills">
  <option value="HTML">
  <option value="CSS">
</datalist>

```

---

### `<output>` — Calculation result

```html
<output name="result" for="a b">10</output>

```

---

## 🌍 14. Global Attributes (APPLY TO EVERY TAG – COMPLETE)

```
id               → Unique identifier
class            → CSS class
style            → Inline CSS
title            → Tooltip
hidden           → Hide element
tabindex         → Keyboard order
contenteditable  → Editable text
spellcheck       → true | false
draggable        → true | false
lang             → Language code
dir              → ltr | rtl
accesskey        → Keyboard shortcut
translate        → yes | no

role             → ARIA role
aria-label       → Accessibility label
aria-hidden      → true | false
data-*           → Custom data attributes

```

---

## 🧱 9. Semantic Layout (HTML5)

```html
<header>Top section</header>
<nav>Navigation</nav>
<main>Main content</main>
<section>Section</section>
<article>Article</article>
<aside>Sidebar</aside>
<footer>Footer</footer>

```

---

## 💻 10. Code & Quotes

```html
<code>console.log()</code>
<pre>Preserved format</pre>
<kbd>Ctrl + C</kbd>
<samp>Output</samp>
<var>x</var>

<blockquote cite="url">Quote</blockquote>
<q>Inline quote</q>

```

---

## ⚙️ 11. Interactive & UI

```html
<details open>
  <summary>More</summary>
  Content
</details>

<dialog open>Dialog box</dialog>

<progress value="60" max="100"></progress>
<meter min="0" max="100" value="70"></meter>

```

---

## 🧩 12. Embedded Content

```html
<iframe src="page.html" width="300" height="200" loading="lazy"></iframe>

<object data="file.pdf" type="application/pdf"></object>
<embed src="file.pdf">

```

---

## 🎨 13. Graphics

```html
<canvas id="c" width="200" height="100"></canvas>

<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" fill="red" />
</svg>

```

---

## 🌍 14. Global Attributes (Used on ANY tag)

```
id, class, style, title, hidden, tabindex
contenteditable, draggable, spellcheck
data-*, role, aria-*

```

---

## ❌ 15. Obsolete / Deprecated (Avoid)

```
<font>, <center>, <big>, <strike>, <frameset>, <frame>, <applet>

```

---

#### tt-teletype text tag-old XHTML deprecated now

**purpose:Terminal output,Command-line text,Machine-generated text,Fixed-width data where alignment mattered**

### Example (old HTML)

```html
<p>System output:</p>
<tt>ERROR 404: File not found</tt>
//This visually rendered the text in a monospace font.
```

**The correct modern alternatives Tag: <code>,<pre>,css style:{font-family: monospace}**

---

### 🌱 The Base: Why HTML Was Created

### HTML (around 1991)

- HTML = **HyperText Markup Language**
- Created to **share documents on the web**
- Very **simple and forgiving**
- Browsers did not care much about mistakes

Example:

```html
<p>Hello
<b>World
```

Even if tags were not closed properly, browsers still showed the page.

✅ Easy to use, ❌ But messy and inconsistent

---

## 📏 The Problem With Old HTML

As websites became:

- Bigger
- More complex
- More interactive

HTML started causing problems:

- Different browsers behaved differently
- Bad code still worked → developers became careless
- Machines (parsers, tools) couldn’t reliably understand pages

So people thought:

> “What if we make HTML strict and clean?”
> 

---

## 🧱 XHTML – The “Strict” Phase

### XHTML (around 2000)

- XHTML = **Extensible HyperText Markup Language**
- HTML rewritten using **XML rules**
- Controlled by **W3C**

### Rules of XHTML (VERY strict):

1. Every tag must be closed
2. Tags must be lowercase
3. Proper nesting is required

```html
❌ Wrong in XHTML:
<p><b>Hello</p></b>
✅ Correct:
<p><b>Hello</b></p>
```

If you made **one small mistake** → page could **completely fail** 😨

### Why XHTML failed

- Too strict for real-world web
- Old browsers didn’t fully support it
- Developers hated breaking pages for tiny errors

👉 XHTML was **good in theory**, bad in practice

---

## 🔄 Back to Reality: HTML Comes Back

People realized:

- The web needs to be **forgiving**
- Browsers already handle errors
- We need new features (video, audio, apps)

Some browser companies (Apple, Mozilla, Google) formed **WHATWG**

Their idea: “Let’s improve HTML instead of replacing it”

---

## HTML5 – The Modern Web

### HTML5 (official around 2014)

HTML5 is:

- A **continuation of HTML**, not XHTML
- Designed for **real-world websites**
- Error-tolerant (like old HTML)
- Powerful (like modern apps)

### What HTML5 added:

- Semantic tags:
    
    ```html
    <header> <footer> <article> <section>
    ```
    
- Multimedia (no plugins needed):
    
    ```html
    <video> <audio>
    ```
    
- Better forms
- Canvas, storage, APIs

#### Important fact: HTML5 **does NOT require XHTML rules**, but you *can* still write clean code.

---

https://cdn.educba.com/academy/wp-content/uploads/2018/07/XHTML-vs-HTML5.jpg

1. **HTML** → simple, messy, forgiving
2. **XHTML** → strict, clean, but impractical
3. **HTML5** → forgiving + powerful + modern

**HTML5 is the modern, practical evolution of HTML, created after XHTML proved too strict for the real web.**

---

### 🌱 First: What is XML (in simple words)?

**XML = eXtensible Markup Language**

👉 **XML is NOT for showing webpages**

👉 **XML is for storing and carrying data**

Think of XML as: A data container, not a design language

---

### 🤔 Why XML Was Created (The Problem)

In early web days:

- HTML was used everywhere
- But HTML was made to **display data**, not **store data**
- Computers needed a **clean, strict way** to exchange information

Example problem:

- A server sends data to another server
- Or a bank sends transaction data
- Or a system sends configuration settings

HTML was **too loose** for this.

So the question was: How can computers talk to each other clearly, without confusion?”

### 🕰️ When XML Came

- XML was created in **1998**
- By **W3C**

Their goal: “Create a simple, strict, readable format for data exchange”

---

### 🧱 What XML Actually Is

XML lets **YOU create your own tags**.

Example:

```xml
<student>
  <name>Ali</name>
  <age>20</age>
  <course>Computer Science</course>
</student>

```

🔹 These tags mean something

🔹 Machines understand structure

🔹 Humans can read it easily

---

## 📏 XML Rules (Why It’s Strict)

XML follows **very strict rules**:

1. Every tag must close
2. Proper nesting
3. Case-sensitive
4. One root element

```xml
❌ Wrong:
<Name>Ali</name>
✅ Correct:
<Name>Ali</Name>
```

Why so strict? 👉 Computers love **rules**, not guesses

---

### 🆚 XML vs HTML (Very Important)

| Feature | XML | HTML |
| --- | --- | --- |
| Purpose | Store & transport data | Display data |
| Tags | User-defined | Predefined |
| Strict | Yes | No |
| Error handling | Fails on error | Forgiving |
| Looks like a page | ❌ No | ✅ Yes |

👉 **XML does not replace HTML**

👉 They do **different jobs**

---

## 🧩 Where XHTML Fits In

XHTML is: HTML written using XML rules

So: XHTML = HTML + XML discipline

HTML tried to become XML-like…

But later HTML5 chose a **practical path** instead.

---

### 📍 Where XML Is Used Today (Important!)

XML is **still very important** today 💡

#### ✅ Used in:

- **Data exchange between systems**
- **Configuration files**
- **Web services**
- **Enterprise software**
- **Office files** (.docx, .xlsx are XML inside!)

Examples:

- SOAP APIs
- Android layout files
- Server config files
- RSS feeds

#### ❌ Where XML Is NOT Used Much Now

- Modern web APIs mostly use **JSON**
- Frontend apps rarely write raw XML

But: 👉 XML is **not dead,** 👉 It is just used **behind the scenes**

---

1. **HTML → display web pages**
2. **XML → store & transport data**
3. **XHTML → tried to mix both**
4. **HTML5 → display + apps**
5. **XML → continues for data systems**

---