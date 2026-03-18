#  The Code Tag (`<code>`)

The `<code>` tag is a semantic HTML element designed specifically to display fragments of computer code. While the `<pre>` tag handles the layout and spacing, the `<code>` tag tells the browser and search engines that the text inside is a technical instruction or a programming snippet.

---

## 1. What is the `<code>` Tag?

The `<code>` tag is an **inline element**. It styles the text inside using a **monospaced font** (where every letter has the same width), which is the standard look for programming environments.

### Key Benefits:

* **Semantic Meaning:** It clarifies that the text is not regular prose, helping search engines and screen readers identify technical content.
* **Readability:** Code stands out from the rest of the paragraph, making it easier for developers to scan.
* **Styling:** It serves as a perfect hook for CSS or syntax highlighting libraries (like Prism.js or Highlight.js) to add colors to your code.

---

## 2. Basic Usage (Inline)

You use `<code>` inline when you want to mention a specific command or variable name within a sentence.

**Syntax:**

```html
<p>To save your file, use the <code>ctrl + s</code> shortcut.</p>

```

---

## 3. Advanced Usage: `<code>` with `<pre>`

For **multiline** code snippets (like a full function or a script), the `<code>` tag is almost always wrapped inside a `<pre>` tag.

* The **`<pre>`** tag preserves the indentation and line breaks.
* The **`<code>`** tag provides the semantic meaning and font style.

**Syntax:**

```html
<pre>
    <code>
        function sayHello() {
            console.log("Hello, World!");
        }
    </code>
</pre>

```

---

##  Execution Code Snippet

Copy this into your `index.html` to see the difference between inline code and a code block:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Code Tag Practice</title>
    <style>
        /* Optional: Making the code look like a professional editor */
        code {
            background-color: #f4f4f4;
            padding: 2px 4px;
            border-radius: 4px;
            color: #d63384;
        }
        pre code {
            background-color: #272822;
            color: #f8f8f2;
            display: block;
            padding: 15px;
            overflow-x: auto;
        }
    </style>
</head>
<body>

    <h1>Developer Documentation</h1>

    <p>In HTML, the <code>&lt;img&gt;</code> tag is used to display images. Remember that it is a self-closing tag.</p>

    <hr />

    <h3>Example JavaScript Block:</h3>
    <pre><code>
// This is a code block
let score = 100;

if (score >= 50) {
    console.log("You Passed!");
}
    </code></pre>

</body>
</html>

```
---

<br>


# 2. Semantic Tags

In older versions of HTML, developers used `<div>` tags for everything. While `<div>` works, it doesn't tell the browser or Google anything about the content inside. **Semantic Tags** solved this by using names that clearly describe their purpose.

---

## 1. What are Semantic Tags?

A semantic element clearly describes its meaning to both the browser and the developer. Instead of a "generic box," you use a tag that says exactly what that box contains.

### Key Semantic Tags to Know:

* **`<header>`**: The top section of a page or section, usually containing the logo and main title.
* **`<nav>`**: Reserved specifically for navigation links (menus).
* **`<main>`**: The unique, primary content of the document. There should only be one `<main>` tag per page.
* **`<article>`**: A self-contained piece of content that could be reused elsewhere (like a blog post, news story, or forum post).
* **`<section>`**: A thematic grouping of content, typically with a heading.
* **`<aside>`**: Content tangentially related to the main text, like a sidebar, call-out box, or advertisements.
* **`<footer>`**: The bottom section containing copyright info, contact links, or sitemaps.
* **`<figure>` & `<figcaption>**`: Used to group an image or chart with a descriptive caption.
* **`<time>`**: Specifically identifies dates, times, or durations.

---

## 2. Why Use Semantic Tags?

1. **SEO (Search Engine Optimization):** Google understands your page structure better, which can help your site rank higher.
2. **Accessibility:** Screen readers use these tags to help visually impaired users navigate the page (e.g., "Jumping to main content").
3. **Code Readability:** It is much easier for developers to maintain code when they see `<header>` instead of `<div class="top-part-of-page">`.

---

## 3. Practical Examples

### **Page Layout Structure**

```html
<header>
    <h1>Learning Tech</h1>
    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Course</a></li>
        </ul>
    </nav>
</header>
 
<footer>
    <p>© 2026 Student Portal</p>
</footer>

```

### **Content Grouping**

```html
<article>
    <h2>Understanding HTML5</h2>
    <section>
      <h3>Introduction</h3>
      <p>Semantic tags were a major update...</p>
    </section>
</article>

<figure>
    <img src="code-sample.jpg" alt="A block of HTML code">
    <figcaption>Fig 1.1: Example of semantic nesting.</figcaption>
</figure>

```

---

##  Execution Code Snippet

Copy this into your `index.html` to see a properly structured semantic page:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Semantic HTML Practice</title>
</head>
<body>

    <header>
        <h1>My Personal Blog</h1>
        <nav>
            <a href="#">Home</a> | <a href="#">Articles</a> | <a href="#">Contact</a>
        </nav>
    </header>

    <main>
        <article>
            <header>
                <h2>The Future of Web Development</h2>
                <p>Published on: <time datetime="2026-03-16">March 16, 2026</time></p>
            </header>
            
            <section>
                <p>Semantic tags make the web a better place for everyone...</p>
            </section>
            
            <aside>
                <p>Author Bio: A student learning HTML in Sindh.</p>
            </aside>
        </article>
    </main>

    <footer>
        <p>Copyright &copy; 2026 Your Name</p>
    </footer>

</body>
</html>

```

---


<br>

# 3. The Canvas Element (`<canvas>`)

The `<canvas>` element is a powerful tool in HTML used to draw graphics on the fly. While tags like `<img>` or `<svg>` are used to display existing images or vectors, `<canvas>` provides a blank drawing board where you can render shapes, graphs, and animations.

---

## 1. What is Canvas?

The `<canvas>` element acts as a container for graphics. It creates a fixed-size drawing area on your webpage. By itself, the canvas is just a transparent white box; you use **JavaScript** to actually "draw" the pixels inside it.

---

## 2. Why Use Canvas?

* **High Performance:** It is excellent for rendering complex graphics and thousands of objects at once.
* **Dynamic Content:** Perfect for creating real-time graphs, stock charts, or weather maps.
* **Gaming:** Most web-based 2D and 3D games are built using the `<canvas>` element as the main game window.
* **Interactivity:** It allows users to interact with graphics, such as drawing with a mouse or playing a game.

---

## 3. Basic Syntax & Attributes

To create a canvas, you define the tag and set its dimensions. It is a paired tag, so it requires a closing `</canvas>`.

**Syntax:**

```html
<canvas id="myCanvas" width="200" height="100"></canvas>

```

### Essential Attributes:

* **`id`**: This is very important because you will need it to "find" the canvas using JavaScript to start drawing.
* **`width`**: Sets the width of the drawing area (default is 300px).
* **`height`**: Sets the height of the drawing area (default is 150px).

> **Note:** Always set the width and height directly in the HTML attributes rather than CSS. If you resize a canvas with CSS, the drawing inside might look stretched or blurry.

---

## 4. Styling the "Container"

Since the canvas is an HTML element, you can use CSS to add borders, backgrounds, or shadows to the "board" itself.

```css
canvas {
    border: 2px solid #000000;
    background-color: #f0f0f0;
}

```

---

## Execution Code Snippet

Copy this into your `index.html`. Even though we haven't reached the JavaScript modules yet, I’ve included a tiny bit of script so you can actually see the canvas "drawing" a shape:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Canvas Practice</title>
    <style>
        #myCanvas {
            border: 1px solid black;
            display: block;
            margin: 20px auto;
        }
    </style>
</head>
<body>

    <h1 style="text-align: center;">HTML5 Canvas Drawing Board</h1>

    <canvas id="myCanvas" width="400" height="200">
        Your browser does not support the HTML5 canvas tag.
    </canvas>

    <script>
        // Simple script to draw on the canvas
        var c = document.getElementById("myCanvas");
        var ctx = c.getContext("2d");
        
        // Draw a Blue Rectangle
        ctx.fillStyle = "#0000FF";
        ctx.fillRect(50, 50, 150, 100);
        
        // Draw some text
        ctx.font = "20px Arial";
        ctx.fillText("Canvas Drawing", 210, 100);
    </script>

</body>
</html>

```

---

<br>

# 4. Global Attributes

**Global Attributes** are a special set of attributes that are common to all HTML elements. Unlike specific attributes (like `src` for images or `href` for links), global attributes can be used on **any** tag, from a `<div>` to a `<button>`. They are essential for styling, identification, and adding custom data.

---

## 1. What Are HTML Global Attributes?

As the name suggests, "Global" means universal. These attributes provide a consistent way to control elements regardless of their type. They allow developers to hook into elements using CSS for styling or JavaScript for functionality.

---

## 2. Common Global Attributes Table

Below are the most frequently used global attributes that every developer should know:

| Attribute | Description |
| --- | --- |
| **`id`** | Specifies a **unique** id for an element. No two elements on the same page can have the same ID. |
| **`class`** | Specifies one or more class names for an element (used for CSS styling). Multiple elements can share the same class. |
| **`style`** | Specifies inline CSS styles for an element. |
| **`title`** | Specifies extra information about an element (usually shown as a tooltip on hover). |
| **`lang`** | Specifies the language of the element's content (e.g., `en`, `ur`). |
| **`data-*`** | Used to store custom data private to the page or application. |
| **`contenteditable`** | Specifies whether the content of an element is editable or not. |
| **`hidden`** | A boolean attribute that prevents the element from being rendered by the browser. |
| **`accesskey`** | Specifies a shortcut key to activate or focus an element. |

---

## 3. Practical Usage Examples

### **A. Using `class` and `id**`

The `id` is like a CNIC (unique to one), while the `class` is like a uniform (many people can wear it).

```html
<div id="main-header" class="blue-text big-font">
    Welcome to my Website
</div>

```

### **B. Using `contenteditable**`

This is a "cool" attribute that turns any element into a text editor directly in the browser.

```html
<p contenteditable="true">
    You can click here and change this text yourself!
</p>

```

### **C. Using `data-*` (Custom Data)**

The `*` can be replaced with any word. This is used to store extra info that isn't visible to the user but is useful for JavaScript.

```html
<div data-user-id="12345" data-role="admin">
    User Profile Card
</div>

```

---

##  Execution Code Snippet

Copy this into your `index.html` to see how global attributes change the behavior of different elements:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Global Attributes Practice</title>
    <style>
        .highlight { background-color: yellow; font-weight: bold; }
        #unique-box { border: 2px solid red; padding: 10px; }
    </style>
</head>
<body>

    <h1>Global Attributes Lab</h1>

    <div id="unique-box">
        This box has a unique ID.
    </div>

    <p class="highlight">This paragraph is highlighted using a class.</p>
    <span class="highlight">This span also uses the same class!</span>

    <hr />

    <p title="This is a tooltip!">Hover your mouse over me to see the title attribute in action.</p>

    <div style="border: 1px dashed blue; padding: 10px;" contenteditable="true">
        I am <strong>editable</strong>. Click here and try to type something!
    </div>

</body>
</html>

```

---

<br>

# 5. HTML Entities

In HTML, certain characters are "reserved." For example, the browser thinks `<` is the start of a new tag. If you want to actually display a `<` symbol on your screen, you must use an **HTML Entity**. Entities also allow you to display symbols that aren't on your keyboard, like the copyright symbol ©.

---

## 1. What Are HTML Entities?

An HTML entity is a specific string of text that the browser converts into a symbol.

* **The Rule:** Every entity starts with an ampersand (**`&`**) and ends with a semicolon (**`;`**).

---

## 2. Why Use HTML Entities?

### **A. Reserved Characters**

If you type `<p> 5 < 10 </p>`, the browser might get confused and think `< 10` is a tag it doesn't recognize. Using entities ensures the browser treats them as text.

### **B. Special Symbols**

Symbols like currency icons (¥), mathematical signs (±), or legal marks (®) are often not on standard keyboards. Entities provide a safe way to include them.

### **C. Non-Breaking Spaces (`&nbsp;`)**

Normally, browsers squash multiple spaces into one. If you need a "hard space" that prevents the browser from breaking the line at that point, you use `&nbsp;`.

---

## 3. Most Common HTML Entities

| Symbol | Entity Code | Description |
| --- | --- | --- |
| **`<`** | `&lt;` | Less than |
| **`>`** | `&gt;` | Greater than |
| **`&`** | `&amp;` | Ampersand |
| **`"`** | `&quot;` | Double Quotation Mark |
| **`©`** | `&copy;` | Copyright Symbol |
| **`®`** | `&reg;` | Registered Trademark |
| **` `** | `&nbsp;` | Non-breaking space |

---

## Execution Code Snippet

Copy this into your `index.html` to see how these codes transform into real symbols on the screen:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>HTML Entities Practice</title>
</head>
<body>

    <h1>HTML Entities & Special Symbols</h1>

    <h3>1. Reserved Characters</h3>
    <p>To display a tag in text, write: &lt;h1&gt; Hello &lt;/h1&gt;</p>
    <p>Comparison: 10 &lt; 20 and 50 &gt; 25</p>

    <hr />

    <h3>2. Legal & Symbols</h3>
    <p>Copyright &copy; 2026 Your Name</p>
    <p>Registered Trademark &reg;</p>
    <p>Price: &euro; 50 or &pound; 40</p>

    <hr />

    <h3>3. Spacing Control</h3>
    <p>This&nbsp;&nbsp;&nbsp;text&nbsp;&nbsp;&nbsp;has&nbsp;&nbsp;&nbsp;extra&nbsp;&nbsp;&nbsp;spaces!</p>

</body>
</html>

```

---

<br>

# 6. Quotation Tags

When writing content, you often need to quote someone else's words. HTML provides two specific tags for this: `<blockquote>` and `<q>`. These tags do more than just change the appearance of text; they provide **semantic meaning**, telling search engines and screen readers exactly which parts of your page are quoted from other sources.

---

## 1. Block Quotes vs. Inline Quotes

### **A. The `<blockquote>` Tag**

This tag is used for **long quotations** that take up their own space on the page.

* **Behavior:** It is a **block-level element**, meaning it starts on a new line and usually has a margin (indentation) on the left side.
* **Best for:** Quotes that span multiple lines or paragraphs.

### **B. The `<q>` Tag**

This tag is used for **short quotations** that fit right inside a sentence.

* **Behavior:** It is an **inline element**. Most modern browsers automatically add quotation marks (`" "`) around the text inside a `<q>` tag.
* **Best for:** Short phrases or a single sentence spoken by a person.

---

## 2. The `cite` Attribute

Both tags support the `cite` attribute. This attribute is used to provide the **URL** or source of the quotation. While it isn't visible to the user on the webpage, it is very helpful for SEO and web crawlers to verify the source of the information.

**Syntax:**

```html
<blockquote cite="https://www.brainyquote.com">
  Your time is limited, so don't waste it living someone else's life.
</blockquote>

```

---

## 3. Comparison Table

| Tag | Type | Automatic Styling | Best Use Case |
| --- | --- | --- | --- |
| **`<blockquote>`** | Block-level | Indentation (Margins) | Long excerpts, full paragraphs. |
| **`<q>`** | Inline | Double Quotation Marks | Short quotes within a sentence. |

---

## 🚀 Execution Code Snippet

Copy this into your `index.html` to see the visual difference between the two types of quotes:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Quotation Tags Practice</title>
    <style>
        /* Optional: Making the blockquote look professional */
        blockquote {
            background: #f9f9f9;
            border-left: 10px solid #ccc;
            margin: 1.5em 10px;
            padding: 0.5em 10px;
            font-style: italic;
        }
    </style>
</head>
<body>

    <h1>Famous Quotes</h1>

    <p>Albert Einstein once said, <q>Imagination is more important than knowledge.</q></p>

    <hr />

    <h3>A Deep Thought:</h3>
    <blockquote cite="https://en.wikipedia.org/wiki/Steve_Jobs">
        "Design is not just what it looks like and feels like. Design is how it works."
        <br><br>
        — Steve Jobs
    </blockquote>

</body>
</html>

```

---

<br>

# 7. Obsolete HTML Tags

As web standards evolve, certain HTML tags become **deprecated** or **obsolete**. This means they are no longer recommended for use. While older browsers might still show them, modern web development focuses on separating **content** (HTML) from **presentation** (CSS).

---

## 1. What are Obsolete Tags?

Obsolete tags are elements that have been removed from the official HTML standard. They were mostly used for styling (like changing colors or alignment), which is now the job of CSS.

---

## 2. Why Should You Avoid Them?

* **Poor Accessibility:** Screen readers and assistive technologies may not interpret these tags correctly.
* **Browser Inconsistency:** Some modern mobile browsers might ignore these tags entirely, making your site look broken.
* **Hard to Maintain:** If you use `<font>` tags everywhere, changing your website's color requires updating every single page. With CSS, you change it in one place.

---

## 3. Common Obsolete Tags & Modern Alternatives

| Obsolete Tag | Original Purpose | Modern Alternative (CSS) |
| --- | --- | --- |
| **`<font>`** | Changing color, size, or typeface. | Use `color`, `font-size`, and `font-family` in CSS. |
| **`<center>`** | Centering text or images. | Use `text-align: center;` or Flexbox in CSS. |
| **`<big>`** | Making text larger. | Use `font-size` in CSS. |
| **`<strike>`** | Crossing out text. | Use `<del>` (semantic) or `text-decoration: line-through;`. |
| **`<u>`** | Underlining text. | Use `text-decoration: underline;` (Note: `<u>` is now only for unarticulated annotations). |

---

## 4. Practical Examples of Modern Styling

Instead of using tags to "force" a look, we use the `style` attribute (or an external CSS file) to apply the look to a modern, semantic tag like `<span>` or `<div>`.

### **Replacing the `<font>` Tag**

* **Old Way:** `<font color="red">Caution!</font>`
* **New Way:** `<span style="color: red;">Caution!</span>`

### **Replacing the `<center>` Tag**

* **Old Way:** `<center><h1>Welcome</h1></center>`
* **New Way:** `<h1 style="text-align: center;">Welcome</h1>`

---

##  Execution Code Snippet

Copy this into your `index.html` to see how we achieve the same visual results using modern, valid code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Modern Alternatives Practice</title>
</head>
<body>

    <h1>Modern Web Standards</h1>

    <div style="text-align: center; background-color: #f0f0f0; padding: 20px;">
        <h2>This is centered using CSS</h2>
        
        <p style="color: blue; font-family: 'Verdana', sans-serif; font-size: 18px;">
            This text is styled with CSS, not the obsolete font tag.
        </p>

        <p>You can <span style="text-decoration: underline;">underline</span> text safely using styles.</p>
    </div>

</body>
</html>

```

---

<br>

# 8. Character Sets

Character sets are the "translation guides" that computers use to turn binary numbers into the letters, numbers, and symbols you see on a screen. In HTML, specifying the correct character set ensures that your text—whether it's English, Urdu, or a special emoji—is displayed correctly across every browser and device.

---

## 1. What is a Character Set?

A character set is a mapping of numerical values to specific symbols. Every time you type a letter, the computer stores it as a number. The character set tells the browser: "Number 65 represents the letter 'A', and number 1575 represents the Urdu letter 'Alif'."

---

## 2. Why is it Important?

* **Accurate Rendering:** Prevents "garbage" characters (like weird symbols or squares) from appearing instead of your text.
* **Multi-language Support:** Allows a single page to display multiple languages (like English and Urdu) simultaneously.
* **SEO and Accessibility:** Search engines and screen readers need to know the encoding to read your content properly.

---

## 3. Specifying the Character Set

The character set must be defined at the very top of your `<head>` section. This is done using the `charset` attribute within a `<meta>` tag.

**Modern Standard (Recommended):**

```html
<meta charset="UTF-8">

```

---

## 4. Common Character Sets

| Character Set | Description |
| --- | --- |
| **UTF-8** | **Universal Character Set.** It covers almost all characters, symbols, and emojis in the world. It is the gold standard for the modern web. |
| **ASCII** | The original standard for the English alphabet and basic symbols. Very limited compared to modern needs. |
| **ISO-8859-1** | Primarily used for Western European languages. It cannot handle many Asian or Middle Eastern characters. |

---

##  Execution Code Snippet

Copy this into your `index.html` to see how **UTF-8** handles different languages and symbols flawlessly:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Character Sets Practice</title>
</head>
<body>

    <h1>Character Set Demonstration</h1>

    <section>
        <h3>1. Multi-language Support</h3>
        <p>English: Hello, how are you?</p>
        <p>Urdu: آپ کیسے ہیں؟ (Aap kaise hain?)</p>
    </section>

    <hr />

    <section>
        <h3>2. Special Symbols & Emojis</h3>
        <p>Mathematical: π ≈ 3.14159</p>
        <p>Currency: € 50.00</p>
        <p>Emoji Support: 🚀 💻 🌐</p>
    </section>

</body>
</html>

```

---
