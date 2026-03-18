

#  Module 01.09: Skeletal Tags (The Foundation)

Just like a human body needs a skeleton to stand, an HTML document needs **Skeletal Tags** to function. These tags define the overall structure and layout of the entire webpage. Without these, the browser would not know how to organize your content.

---

## 1. The `<html>` Tag: "The Root"

The `<html>` tag is the root element that wraps all the content on the page. It tells the web browser that the document is an HTML file.

**Syntax & Implementation:**

```html
<html>
  </html>

```

* **Role:** It acts as the "Parent" container for the two main sections: the Header (`<head>`) and the Body (`<body>`).

---

## 2. The `<head>` Tag: "The Header"

The `<head>` section is the header part of an HTML page. It contains information that helps the browser and search engines understand the page, though most of it is invisible to the user.

**Syntax & Implementation:**

```html
<head>
  </head>

```

* **Role:** It stores **Meta Information** (data about the page). While the user doesn't see this content on the page, it is vital for **SEO** (Search Engine Optimization) and linking external styles or scripts.

---

## 3. The `<title>` Tag: "The Tab Title"

The `<title>` tag defines the title part of the page. It lives inside the `<head>` section.

**Syntax & Implementation:**

```html
<title>
  // Your Website Title Here
</title>

```

* **Role:** It defines the title of the document, which is displayed in the **browser's title tab**. This is also the name shown when someone bookmarks your page.

---

## 4. The `<body>` Tag: "The Visual Center"

The `<body>` tag is the body part of the HTML page. It encloses the main content that is actually rendered on the screen for the visitor.

**Syntax & Implementation:**

```html
<body>
  // All visible content (text, images, links) goes here
</body>

```

* **Role:** Everything placed inside this tag—headings, paragraphs, images, videos, and buttons—is displayed in the browser window.

---

##  Visualizing the Skeleton

To understand how these tags fit together, look at this hierarchy. Each tag has a specific "zone" in the browser:

1. **`<html>`**: The boundary for the entire project.
2. **`<head>`**: The invisible "brain" at the top.
3. **`<title>`**: The label on the browser tab.
4. **`<body>`**: The white space where your website is actually built.

---

##  Full Skeletal Code Snippet

Copy this into your `index.html` to see the complete, correct structure:

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Skeletal Structure Practice</title>
    </head>
    <body>
        <h1>The Foundation is Ready!</h1>
        <p>This is the visible part of the webpage.</p>
    </body>
</html>

```
---

<br>

#  Heading Tags (Hierarchy & SEO)

Heading tags are essential for defining the **structure** and **priority** of your content. They range from `<h1>` to `<h6>`, creating a clear hierarchy that helps both human readers and search engine crawlers (like Google) understand what your page is about.

---

## 1. The Importance of Headings

* **Organization:** They break your content into digestible sections.
* **SEO:** Proper use of headings improves your search engine ranking.
* **Accessibility:** Screen readers use headings to help visually impaired users navigate your site.

---

## 2. Level-by-Level Breakdown

### **`<h1>` Tag: First-Level Heading**

The `<h1>` is the most important tag on the page. It is usually the largest and boldest, reserved for the **Main Title**.

```html
<h1>
  </h1>

```

### **`<h2>` Tag: Second-Level Heading**

Smaller than `<h1>`, this tag is the standard choice for **Major Section Titles**.

```html
<h2>
  </h2>

```

### **`<h3>` Tag: Third-Level Heading**

Used for **Sub-sections** within an `<h2>` block. It helps keep detailed content organized.

```html
<h3>
  </h3>

```

### **`<h4>` Tag: Fourth-Level Heading**

Used for further breaking down content within an `<h3>` section.

```html
<h4>
  </h4>

```

### **`<h5>` Tag: Fifth-Level Heading**

Smaller and less prominent. These are rarely used but helpful for very deeply nested content.

```html
<h5>
  </h5>

```

### **`<h6>` Tag: Sixth-Level Heading**

The smallest heading tag. It is rarely seen in general usage but exists for specific formatting needs.

```html
<h6>
  </h6>

```

---

##  Visual Hierarchy

The browser automatically scales the size of the text based on the tag level. Here is how they compare:

---

##  Summary Table

| Tag | Purpose | Prominence |
| --- | --- | --- |
| **`<h1>`** | Main Title (Only use one per page) | Largest / Boldest |
| **`<h2>`** | Major Sections | Large |
| **`<h3>`** | Sub-sections | Medium |
| **`<h4>`** | Detailed sub-sections | Small |
| **`<h5>`** | Deeply nested sections | Very Small |
| **`<h6>`** | Minor/Specific headings | Smallest |

---

##  Execution Code Snippet

Copy this into your `index.html` to see the visual difference in your browser:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Heading Tags Practice</title>
</head>
<body>

    <h1>Heading Level 1: The Main Title</h1>
    <h2>Heading Level 2: Major Section</h2>
    <h3>Heading Level 3: Sub-section</h3>
    <h4>Heading Level 4: Minor Section</h4>
    <h5>Heading Level 5: Deeply Nested</h5>
    <h6>Heading Level 6: The Smallest Heading</h6>

</body>
</html>

```
---
<br>

# The Paragraph Tag (`<p>`)

The `<p>` tag is the foundation of readable text on the web. It allows you to organize your content into distinct, manageable blocks rather than one giant wall of text.

---

## 1. Defining a Paragraph in HTML

The `<p>` tag is used to wrap a block of text and format it as a paragraph.

* **Automatic Spacing:** One of the key features of the `<p>` tag is that browsers automatically add an empty line (margin) above and below the paragraph. This provides clear visual separation between different sections of text.
* **Paired Tag:** This is a paired tag, meaning it must start with `<p>` and end with `</p>`.

**Syntax:**

```html
<p>
  </p>

```

---

## 2. Attributes and Styling

While the paragraph tag is simple, you can customize it to change its appearance or behavior using attributes:

* **`class` or `id`:** Used to "label" the paragraph so you can target it later with CSS.
* **`style`:** Used to apply styles (like colors or fonts) directly to the tag.

**Example of a Styled Paragraph:**

```html
<p class="intro-text" style="color: blue; font-weight: bold;">
  This is a styled paragraph that appears blue and bold.
</p>

```

---

## 3. Best Practices

To write professional, clean code, keep these tips in mind:

1. **Content Only:** Use the `<p>` tag for actual text (sentences and stories).
2. **Avoid Layout Abuse:** Do not use empty `<p></p>` tags just to create space between elements. Instead, use CSS margins or `<br />` for line breaks.
3. **Semantic Structure:** For larger chunks of a page, use tags like `<section>` or `<article>` to wrap your paragraphs. This helps search engines understand the context of your writing.

---

##  Execution Code Snippet

Copy this into your `index.html` to see how multiple paragraphs automatically create spacing:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Paragraph Practice</title>
</head>
<body>

    <h1>The Importance of Structure</h1>
    
    <p>This is the first paragraph. Notice how the browser adds space below it automatically.</p>
    
    <p>This is the second paragraph. Because we used the p tag, it doesn't stick to the text above it, making it easy to read.</p>
    
    <p style="color: green;">You can even use the style attribute to make a specific paragraph stand out!</p>

</body>
</html>

```
---

<br>

# The Horizontal Rule Tag (`<hr>`)

The `<hr>` tag is a simple but powerful tool for organizing your content. It allows you to create a clear visual break between different topics or sections of your webpage.

---

## 1. How to Use the `<hr>` Tag

The `<hr>` tag stands for "Horizontal Rule." Unlike headings or paragraphs, this tag does not wrap around text. Instead, it tells the browser to draw a straight line across the page.

**Syntax:**

```html
<hr />

```

---

## 2. Key Characteristics

* **Empty/Self-Closing Tag:** The `<hr>` tag is an unpaired tag. It does not have a closing tag (`</hr>`) because it doesn't contain any content—it *is* the content.
* **Visual Separation:** It is primarily used to indicate a **thematic break**. For example, you might use it between the end of a story and the start of an author's biography.
* **Default Styling:** By default, browsers render this as a thin, gray line with some space (margin) above and below it.

---

## 3. Best Practices

In modern web development, we use the `<hr>` tag when there is a shift in the topic.

* Use it to separate a header from the main content.
* Use it between different articles on a single page.
* Avoid using it purely for decoration; if you just want "space" without a line, use CSS margins instead.

---

##  Execution Code Snippet

Copy this into your `index.html` to see how the horizontal line separates different sections of text:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Horizontal Rule Practice</title>
</head>
<body>

    <h1>Chapter 1: The Beginning</h1>
    <p>This is the introduction to our story. Everything starts here.</p>

    <hr /> <h2>Chapter 2: The Adventure</h2>
    <p>Now that the introduction is over, the real action begins in this section.</p>

    <hr />

    <footer>
        <p>End of Document</p>
    </footer>

</body>
</html>

```
---
<br>

# The Line Break Tag (`<br>`)

While the paragraph tag (`<p>`) is used for large blocks of text with spacing, the `<br>` tag is used for smaller, precise movements. It allows you to move to the next line without adding the extra empty space that a paragraph creates.

---

## 1. What is the `<br>` Tag?

The `<br>` tag stands for "Break." Its primary job is to force the text that follows it to start on a new line immediately.

* **Empty/Self-Closing Tag:** Like the `<hr>` tag, the `<br>` is an unpaired tag. You do not need to "close" it with `</br>`.
* **No Extra Spacing:** Unlike paragraphs, which add vertical space (margins) between lines, the `<br>` tag simply drops the text down one line, keeping the lines close together.

**Syntax:**

```html
<br />

```
---

## 2. When to Use It

The `<br>` tag is most useful when the **structure** of the lines matters as much as the content itself. Common use cases include:

* **Postal Addresses:** Keeping the name, street, and city on separate lines.
* **Poetry or Song Lyrics:** Preserving the specific rhythm and line endings of the writer.
* **Contact Details:** Separating phone numbers from email addresses in a small area.

---

## 3. Best Practices

* **Don't Overuse for Layout:** If you find yourself using five `<br>` tags in a row to create space, you should be using **CSS margins** or **Paragraphs** instead.
* **Accessibility:** Screen readers sometimes struggle with excessive line breaks, so only use them when a new line is logically necessary for the content.

---

## Execution Code Snippet

Copy this into your `index.html` to see the difference between a paragraph break and a simple line break:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Line Break Practice</title>
</head>
<body>

    <h1>Contact Information</h1>
    
    <p>
        John Doe <br />
        123 Web Developer Lane <br />
        Code City, 54321
    </p>

    <hr />

    <h2>Poetry Example</h2>
    <p>
        Roses are red, <br />
        Violets are blue, <br />
        HTML is easy, <br />
        And so are you!
    </p>

</body>
</html>

```
---

<br>

#  The Anchor Tag (`<a>`)

The **Anchor Tag** is what makes the "World Wide Web" a web. It creates **hyperlinks**, allowing users to jump from one page to another, or even to different sections within the same page.

---

## 1. Syntax of HTML Links

The `<a>` tag is a paired tag. It wraps around the text or image that you want to make clickable.

**Syntax:**

```html
<a href="URL_OR_PATH">
    Clickable Content
</a>

```

---

## 2. Essential Attributes

To make a link functional, we use two primary attributes:

### **A. The `href` Attribute**

The `href` (Hypertext Reference) is the most important attribute. it defines the destination address.

* **External Link:** `href="https://www.google.com"`
* **Internal Link:** `href="about.html"`

### **B. The `target` Attribute**

This attribute tells the browser **where** to open the link.

| Value | Description |
| --- | --- |
| **`_self`** | Opens in the same tab (This is the **default**). |
| **`_blank`** | Opens the link in a **new tab** or window. |
| **`_parent`** | Opens in the parent frame. |
| **`_top`** | Opens in the full body of the window (breaks out of frames). |

---

## 3. Linking to Specific Page Sections

You can create "bookmarks" within a long page. This is common for "Back to Top" buttons or Table of Contents.

1. Give the target element a unique **`id`**.
2. Create a link with a hash (**`#`**) followed by that ID.

**Example:**

```html
<a href="#contact-info">Jump to Contact</a>

<h2 id="contact-info">Contact Us</h2>

```

---

## 4. Understanding Link Colors

By default, browsers style links based on their "state" so users know where they have already been:

* **Unvisited Link:** Blue and underlined.
* **Visited Link:** Purple and underlined.
* **Active Link:** Red and underlined (this shows the moment you click it).

---

##  Execution Code Snippet

Copy this into your `index.html` to test both external links and internal section jumping:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Anchor Tag Practice</title>
</head>
<body>

    <h1>Navigation Practice</h1>
    
    <p>Visit the <a href="https://www.wikipedia.org" target="_blank">Wikipedia website</a> in a new tab.</p>

    <p>Want to see the bottom? <a href="#end-of-page">Jump to Footer</a></p>

    <div style="margin-top: 1000px;">
        </div>

    <hr />
    <h2 id="end-of-page">You reached the end!</h2>
    <a href="#">Back to Top</a>

</body>
</html>

```
---

<br>

#  The Image Tag (`<img>`)

Images are essential for providing visual context and making web pages engaging. In HTML, we use the `<img>` tag to embed photos, icons, and graphics into our documents.

---

## 1. Basic Syntax

The `<img>` tag is an **unpaired (self-closing)** tag. This means it does not wrap around content; it simply points to a file and displays it.

**Syntax:**

```html
<img src="path_to_image.jpg" alt="description" />

```

---

## 2. Mandatory Attributes

For an image to work correctly and professionally, you must include these two attributes:

* **`src` (Source):** This specifies the path to the image file. This can be a local file on your computer (e.g., `images/photo.jpg`) or a URL from the internet.
* **`alt` (Alternative Text):** This provides a text description of the image. It is critical for:
* **Accessibility:** Screen readers read this aloud for visually impaired users.
* **Error Handling:** If the image fails to load, the browser displays this text instead.
* **SEO:** Search engines use this text to understand what is in the image.



---

## 3. Image Dimensions and SEO

You can control the size of an image using the `width` and `height` attributes.

**Code Example:**

```html
<img src="logo.png" alt="Company Logo" width="300" height="100" />

```

### Why set dimensions in HTML?

Even though modern styling is done via CSS, setting the width and height directly in the `<img>` tag is a **best practice for SEO**.

* **Prevents Layout Shift:** It tells the browser exactly how much space to reserve *before* the image finishes downloading.
* **CLS Score:** This improves your **Cumulative Layout Shift** (CLS), a key Google metric. A stable page that doesn't "jump" while loading ranks higher in search results.

---

## 4. Supported Formats

HTML supports almost all standard image types, including:

* **PNG:** Great for transparency.
* **JPEG / JPG:** Best for high-quality photographs.
* **GIF:** Used for simple animations.
* **SVG:** Scalable vector graphics (stay sharp at any size).

---

## Execution Code Snippet

Copy this into your `index.html` to see how to properly implement an image with dimensions:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Image Tag Practice</title>
</head>
<body>

    <h1>Visual Content</h1>
    
    <p>Below is an image loaded from a URL with set dimensions:</p>

    <img 
        src="https://via.placeholder.com/300x150" 
        alt="A 300 by 150 placeholder graphic" 
        width="300" 
        height="150" 
    />

    <p>Setting the width and height prevents the page from jumping when it loads!</p>

</body>
</html>

```
---

<br>

# The Preformatted Text Tag (`<pre>`)

In standard HTML, if you press "Enter" or add multiple spaces in your code, the browser ignores them and squashes the text together. The `<pre>` tag is the solution to this—it tells the browser to respect every single space and line break exactly as you typed it.

---

## 1. What Does the `<pre>` Tag Do?

The `<pre>` tag stands for **"Preformatted Text."** It is an indispensable tool for developers because it preserves the original layout of the text.

* **Fixed-Width Font:** By default, browsers display `<pre>` content in a "Monospace" font (like Courier), where every letter takes up the same amount of horizontal space.
* **Whitespace Preservation:** It maintains both spaces and line breaks. If you indent a line by 4 spaces, the browser will show exactly 4 spaces.

---

## 2. Syntax for Using the `<pre>` Tag

The `<pre>` tag is a paired tag. You must place your content between the opening and closing tags.

**Syntax:**

```html
<pre>
    Your text or code goes here...
    It will look exactly
        like this.
</pre>

```

---

## 3. When to Use the `<pre>` Tag?

This tag is most effective when the **visual structure** of the text is just as important as the words themselves.

* **Code Snippets:** Displaying Python, C++, or Java code where indentation is required for logic.
* **ASCII Art:** Creating images out of text characters.
* **Data Logs:** Displaying raw data from a server or file.

---

## 4. Example: Displaying a Python Program

Consider a simple Python script. Without the `<pre>` tag, the browser would put the entire program on one single line, breaking the code. With the `<pre>` tag, it remains functional and readable.

**HTML Implementation:**

```html
<h3>Python Code Example:</h3>
<pre>
def main():
    print("Hello, World!")
 
if __name__ == "__main__":
    main()
</pre>

```

**How it appears in the browser:**

```text
def main():
    print("Hello, World!")
 
if __name__ == "__main__":
    main()

```

---

## Execution Code Snippet

Copy this into your `index.html` to see the difference between how a Paragraph handles code versus how the Pre tag handles it:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Pre Tag Practice</title>
</head>
<body>

    <h1>Displaying Code in HTML</h1>
    
    <h3>Example 1: Using the Paragraph Tag (Incorrect)</h3>
    <p>
        def greet():
            print("Hi!")
    </p>

    <hr />

    <h3>Example 2: Using the Pre Tag (Correct)</h3>
    <pre>
def greet():
    print("Hi!")
    </pre>

</body>
</html>

```
---

<br>