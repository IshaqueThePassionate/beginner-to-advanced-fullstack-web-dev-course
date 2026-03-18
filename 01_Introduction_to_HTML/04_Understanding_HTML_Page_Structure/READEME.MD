
# Module 01.4: Understanding HTML Page Structure

We went a bit through the page structure in the previous module but in this module we would be discussing it in detail. 

Every professional website, from Google to a small personal blog, follows the same basic blueprint. HTML uses **nested tags**, meaning one tag acts as a container for another.

---

## 1. The Basic Blueprint

Here is the most basic version of an HTML document structure. Almost every website on the internet starts with these exact lines of code.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Document</title>
</head>
<body>
   </body>
</html>

```

---

## 2. Breaking Down the Essential Elements

Let’s look at each part of that code to understand what it actually does for the browser.

### **The DOCTYPE Declaration** (`<!DOCTYPE html>`)

This is the very first thing in your file. It isn't exactly an HTML tag; it's an **instruction**. It informs the web browser that this document is using **HTML5** (the latest version). This ensures your page looks modern and behaves correctly.

### **The Root Element** (`<html> ... </html>`)

The `<html>` tag is the "container of all containers." Every other tag on your page must live inside the `<html>` and `</html>` tags.

### **The Head Section** (`<head> ... </head>`)

This is the **"Information Center"** of your page.

* It contains **metadata** (data about data).
* It holds links to external files like CSS (for styling) or JavaScript (for logic).
* Most of the things here are **invisible** to the user, except for the **Title**.

### **The Title Tag** (`<title> ... </title>`)

This tag lives inside the `<head>`. Whatever text you put here will appear in the **browser's tab** or the title bar at the top of the window.

### **The Body Tag** (`<body> ... </body>`)

This is the **"Visual Center"** of your page. Everything you want the visitor to see—text, images, buttons, or videos—must be placed inside the `<body>` tags.

---

## 3. Visualization: How the Code Translates to the Screen

To understand how the browser separates the **Head** from the **Body**, consider this example code:

```html
<html>
<head>
    <title>Page title</title>
</head>
<body>
    <h1>This is a heading</h1>
    <p>This is a paragraph.</p>
    <p>This is another paragraph.</p>
</body>
</html>

```

### How it appears in a Browser:

* **The Tab:** The browser looks at the `<title>` and puts "Page title" on the tab at the top.
* **The Page Area:** The browser looks inside the `<body>` and renders the `<h1>` (Heading) and the `<p>` (Paragraphs) on the white background of the window.

---

## 📝 Summary

* **`<!DOCTYPE html>`:** Specifies the document is HTML5.
* **`<html lang="en">`:** Defines the language of the page (good for SEO).
* **`<head>`:** Contains hidden info like metadata and the tab title.
* **`<body>`:** Contains all visible content.
* **`<h1>` and `<p>`:** Examples of content tags (Headings and Paragraphs) that live inside the body.

---

## 🖼 Rendering Example

Look at this specific code:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Document</title>
</head>
<body>
    <h1> This is a heading</h1>
    <p>This is a paragraph</p>
</body>
</html>

```

When this is rendered, the browser separates the instructions:

1. The `<title>` goes into the browser **Tab**.
2. The `<h1>` and `<p>` go into the **Main Window**.

---

**Now that you understand the skeleton of a page, are you ready to learn about the specific tags we use to fill the body, like Headings, Paragraphs, and Links?**