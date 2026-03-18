##  Module 01.13: Meta Tags & Favicons

Meta tags provide **Metadata** about your HTML document. Metadata is essentially "data about data." These tags tell the browser how to display the page and provide search engines (SEO) with critical information about your content.

---

## 1. Using Meta Tags

Meta tags always belong inside the `<head>` section of your document. While they are not visible to users on the actual webpage, they are vital for browsers and Google.

### Explanation of Common Meta Tags:

* **Character Encoding (`charset`):** `<meta charset="UTF-8">` sets the character encoding for the webpage. UTF-8 is the standard recommendation because it supports almost all characters and symbols from every language.
* **Viewport:** `<meta name="viewport" content="width=device-width, initial-scale=1.0">` is essential for **Responsive Design**. It ensures your website scales correctly to fit the screen width of mobile devices.
* **IE Compatibility:** `<meta http-equiv="X-UA-Compatible" content="ie=edge">` tells Internet Explorer to use the latest available rendering engine.
* **Description:** `<meta name="description" content="...">` provides a brief summary of the page. Search engines often display this text in search results.
* **Keywords:** `<meta name="keywords" content="...">` lists relevant words for the page. (Note: These are less important for SEO today than they used to be).
* **Author:** `<meta name="author" content="...">` identifies the person who created the webpage.

---

## 2. How to Add a Favicon

A **Favicon** is the small icon that appears next to your website's title in browser tabs. It is a key part of branding and helps users identify your site when they have multiple tabs open.

### Steps to Add a Favicon:

1. **Create/Choose:** Create a square image (usually 16x16 or 32x32 pixels) in `.ico` format. You can use online favicon generators to convert images.
2. **Upload:** Place the `.ico` file in your website's root directory (the same folder as `index.html`).
3. **Update HTML:** Insert the following code in the `<head>` section:

```html
<link rel="icon" href="favicon.ico" type="image/x-icon">

```

---

## Execution Code Snippet

This snippet demonstrates how to organize all common meta tags and the favicon link correctly:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8"> 
    
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
    
    <meta http-equiv="X-UA-Compatible" content="ie=edge"> 
    
    <meta name="description" content="A comprehensive guide to learning Full Stack Development."> 
    
    <meta name="keywords" content="HTML, CSS, JavaScript, Programming"> 
    
    <meta name="author" content="Your Name"> 
    
    <link rel="icon" href="favicon.ico" type="image/x-icon">

    <title>Document Title</title>
</head>
<body>
    <h1>Meta Tags and Favicon are set!</h1>
    <p>Check the head section in the source code to see the metadata instructions.</p>
</body>
</html>

```

---

##  Summary

* **Meta tags** are always placed in the `<head>`, never in the `<body>`.
* The **Viewport** tag is mandatory for a modern, mobile-friendly website.
* A **Favicon** makes your website look professional and helps with brand recognition.

---

<br>


# 2. Link & Script Tags

The `<link>` and `<script>` tags are the bridges that connect your HTML document to external resources. They allow you to pull in styles (CSS) to make your page look beautiful and logic (JavaScript) to make your page interactive.

---

## 1. The `<link>` Tag

The `<link>` tag is most commonly used to connect an external **CSS Stylesheet** to your HTML file. This allows you to keep your design separate from your content.

### Key Characteristics:

* **Location:** It is always placed inside the `<head>` section.
* **Self-Closing:** It is an unpaired tag; it does not need a `</link>` closing tag.
* **Attributes:**
* `rel`: Specifies the relationship between the current document and the linked resource (usually `stylesheet`).
* `type`: Specifies the media type (usually `text/css`).
* `href`: Specifies the path to the CSS file.



**Syntax:**

```html
<link rel="stylesheet" type="text/css" href="styles.css">

```

---

## 2. The `<script>` Tag

The `<script>` tag is used to embed or link **JavaScript** code. This adds functionality, like button clicks, animations, or data processing.

### Key Characteristics:

* **Location:** It can be placed in the `<head>` or at the very bottom of the `<body>` (the bottom is often preferred to ensure the HTML loads first).
* **Paired Tag:** Unlike the link tag, the script tag **must** be closed with `</script>`.
* **Attribute:**
* `src`: Specifies the path to the external JavaScript file.



**Syntax for External Script:**

```html
<script src="script.js" type="text/javascript"></script>

```

**Syntax for Inline Script:**

```html
<script>
    console.log("Hello from inside the HTML!");
</script>

```

---

## 3. Link vs. Script Comparison

| Feature | `<link>` Tag | `<script>` Tag |
| --- | --- | --- |
| **Primary Use** | External CSS Styles | External or Inline JavaScript |
| **Tag Type** | Self-closing (Unpaired) | Paired (Must be closed) |
| **Path Attribute** | `href` | `src` |
| **Common Location** | Always in `<head>` | In `<head>` or end of `<body>` |

---

##  Execution Code Snippet

Copy this into your `index.html` to see the standard way of linking external resources:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Link and Script Practice</title>

    <link rel="stylesheet" href="style.css">

</head>
<body>

    <h1>Resource Connection</h1>
    <p>This page is linked to external styles and logic.</p>

    <script src="app.js"></script>
</body>
</html>

```

---

##  Summary 

* Use **`<link>`** for your "Design" (CSS).
* Use **`<script>`** for your "Action" (JavaScript).
* Remember that `<link>` uses **`href`**, while `<script>` uses **`src`**. Mixing these up is a very common beginner mistake!
