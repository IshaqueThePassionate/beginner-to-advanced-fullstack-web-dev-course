
# Module 01.7: HTML Attributes

HTML attributes define the **characteristics** of an element. They are always placed inside the **opening tag** and follow a specific format:

> **Format:** `name="value"`

* **Name:** The property you want to set (e.g., `src`, `href`, `id`).
* **Value:** The specific setting for that property, usually enclosed in double quotes.

---

### 1. The Three Main Categories

Attributes are generally divided into three types based on their purpose:

| Type | Description | Examples |
| --- | --- | --- |
| **Core Attributes** | The most common attributes used for styling and identifying elements. | `id`, `class`, `style`, `title` |
| **Internationalization** | Used to handle different languages and text directions. | `lang`, `dir` |
| **Generic Attributes** | Used for custom data or extra info that doesn't change appearance. | `data-*` |

---

### 2. Deep Dive: Core Attributes

These are the "Big Four" that you will use constantly as a developer.

#### **A. The `id` Attribute**

The `id` is a **unique** identifier. Just like your National ID or CNIC, no two elements on the same page can have the same `id`.

```html
<p id="html">This is an HTML tutorial</p>
<p id="python">This is a Python tutorial</p>

```

#### **B. The `class` Attribute**

Unlike the ID, a `class` can be used on **multiple** elements. This is used when you want a group of different tags to share the same styling or behavior.

```html
<p class="blue-text">This paragraph is blue.</p>
<h2 class="blue-text">This heading is also blue.</h2>

```

#### **C. The `title` Attribute**

The `title` adds extra information. When a user hovers their mouse over the element, a small **tooltip** appears showing the text you wrote.

```html
<h4 title="hello, motto">Hover over me!</h4>

```

#### **D. The `style` Attribute**

This is used for **Inline Styling**. It allows you to apply CSS directly to a single tag without needing a separate CSS file.

```html
<p style="color: red;">This text is red because of the style attribute.</p>

```

---

### 3. Internationalization Attributes

These are essential for making your website accessible to people in different regions.

* **`lang`**: Tells the browser the language of the content (e.g., `lang="en"` for English, `lang="ur"` for Urdu).
* **`dir`**: Tells the browser the direction of the text. `ltr` is Left-to-Right (English), and `rtl` is Right-to-Left (Urdu/Arabic).

---

### 4. Case Sensitivity (Best Practices)

In HTML5, you can technically write attributes in uppercase (`TITLE="value"`) or lowercase (`title="value"`).

**However**, the industry standard (and the W3C recommendation) is to **always use lowercase**. This makes your code cleaner, more professional, and compatible with stricter systems like XHTML.

---
<br>

#  Module 01.10: HTML Comments

Think of comments as "invisible notes" inside your code. They are essential for keeping your project organized, especially when you start working on large Full Stack applications with other developers.

---

## 1. Why Use Comments?

* **Code Readability:** They explain what a specific section of code is doing.
* **Documentation:** You can leave notes for your "future self" or team members.
* **Debugging:** You can "comment out" a line of code to hide it from the browser temporarily instead of deleting it.
* **Skipped by Browser:** No matter what you write inside a comment, it will **never** appear on the actual webpage.

---

## 2. The Syntax

HTML comments follow a very specific format. They must start and end with these symbols:

> **Start:** ``

### ⚡ The Pro Shortcut

In VS Code (and most other editors), you don't need to type these symbols manually. Just highlight the code you want to comment and press:

* **`Ctrl + /`** (Windows/Linux)
* **`Cmd + /`** (Mac)

---

## 3. Types of Comments

### A. Single-Line Comments

Used for quick, short notes on a single line.

```html
<nav>
    <a href="#">Home</a>
</nav>

```

### B. Multi-Line Comments

Used for detailed explanations or for hiding large blocks of code. Anything placed between the opening `` will be ignored, even if it spans 100 lines.

```html
<section>
    <h2>User Profile</h2>
</section>

```

---

## 4. Best Practices

* **Don't Over-Comment:** You don't need to explain obvious things (like `` above an `<h1>`).
* **Explain the "Why":** Use comments to explain **why** you did something tricky, not just **what** you did.
* **Security Warning:** Never put sensitive information (like passwords or private keys) in HTML comments. Even though they don't show on the page, anyone can see them by using **"View Page Source"**.

---
