
# Module 01: Introduction to HTML

HTML is the absolute foundation of the web. Before a website looks beautiful (CSS) or becomes "smart" (JavaScript), it must have a structure. HTML forms the **backbone** of every webpage you see.

---

## 1. What is HTML?

**HTML** stands for **HyperText Markup Language**. It was created by **Tim Berners-Lee in 1991**.

* **HyperText:** Refers to the "links" (hyperlinks) that connect web pages to one another.
* **Markup Language:** This is not a programming language. It is a language that uses specific **tags** to "mark up" or structure content (headings, paragraphs, images, etc.).

### The Core Analogy (Building a Car)

Think of building a website like building a car:

* **HTML (The Skeleton):** The basic frame and structure. Without it, the car has no shape.
* **CSS (The Paint):** The color, design, and style. It makes the car look appealing.
* **JavaScript (The Engine):** The functionality. It makes the car move and respond to buttons.

---

## 2. Features of HTML

* **Platform-Independent:** Chrome or Firefox will display the same HTML identically whether you are on Windows, Mac, or Linux.
* **Multimedia Integration:** You can easily add images, audio, and videos (e.g., how YouTube displays video content).
* **Integration:** It works seamlessly with CSS and JavaScript to create interactive and dynamic pages.
* **Standardization:** HTML5 is the latest and most stable version used by the industry today.

---

## 3. The Anatomy of an HTML Tag

A **Tag** consists of meaningful text enclosed in angle brackets `< >`.

* **Opening Tag:** `<p>` (Starts the instruction)
* **Content:** This is my text.
* **Closing Tag:** `</p>` (Ends the instruction)
* **The Element:** The combination of the tags and the content together.

---

## 4. The "Boilerplate" Structure

Every HTML file requires a standard set of instructions to work correctly. In modern editors like **VS Code**, you don't have to type this manually.

### The Shortcut ⚡

Simply type `!` and press **Enter** or **Tab**. This will automatically generate the "Boilerplate" code for you.

### The Code Breakdown

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Web Page</title>
</head>
<body>
    <h1>Welcome to My Fullstack Journey</h1>
    <p>This is a paragraph created using HTML tags.</p>
</body>
</html>

```

 **`<!DOCTYPE html>`:** This tells the browser, "I am using the latest version of HTML (HTML5)." Without this, the browser might use "Quirks Mode" and display your site incorrectly.

**`<html lang="en">`:** The root element. The lang attribute helps search engines (SEO) and screen readers know the language of the site.

 **`<head>`:** This is the "Brain" of the page. It contains metadata (info about the page) that the user doesn't see, like the title or character encoding (UTF-8).

 **`<body>`:** This is the "Heart" of the page. Everything written here is what the user actually sees on their screen.

---

## 5. History at a Glance

* **1989:** Tim Berners-Lee establishes the World Wide Web (WWW).
* **1991:** First version of HTML is created.
* **1999:** HTML 4.01 is standardized (still used by many today).
* **Today:** **HTML5** is the global standard, offering the most stable and feature-rich experience.

---

## Quick Exercise: Inspect the Web

As Tim Berners-Lee intended, the web is open!

1. Open any website (e.g., Google or Wikipedia).
2. Right-click and select **"View Page Source"** to see the raw code sent by the server.
3. Right-click and select **"Inspect"** to see the live structure (the DOM) that the browser is currently rendering.

---

