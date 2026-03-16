
#  Module 01.1: How Websites Actually Work

To be a great developer, you need to understand the relationship between your code, the browser, and the server. This section breaks down the "Working" of the web.

---

## 1. Frontend vs. Backend: The Two Sides of the Web

Every application has two main parts:

* **Frontend (The Visible Part):** This is what you see and interact with. It includes buttons, images, tables, and text. It is built using **HTML, CSS, and JavaScript**.
* **Backend (Behind-the-Scenes):** This part handles the "brain" and the "memory." It stores and processes data (like your username or password). It is built using languages like **Python, Ruby, or Java**.

---

## 2. What is an HTML Document?

An HTML document is simply a **text file** that contains specific instructions (tags).

* **The Extension:** You must save these files with a `.html` or `.htm` extension.
* **The Content:** It contains text wrapped in angle brackets `< >`. These tags are **standardized and fixed**; you cannot make up your own tags because the browser wouldn't understand them.

---

## 3. The Role of the Web Browser

A web browser (Chrome, Firefox, Safari) is a complex program designed to be a **translator**.

* **The Problem:** Computers read code; humans read websites.
* **The Solution:** The browser reads the raw HTML tags and **renders** them into a beautiful, human-readable format.

### What is a "Rendered Page"?

The "Rendered Page" is simply the output screen. It is the final result you see in your browser window after it has processed your HTML document.

---

## 4. Step-by-Step: How a Website Loads

When you want to visit a site like `example.com`, this 3-step process happens:

1. **Request:** Your Web Browser (**Client**) asks the Web Server for the website files.
2. **Delivery:** The Server sends back the **HTML, CSS, and JavaScript** files.
3. **Parsing & Rendering:** The browser reads these files and shows you the final website.

---

## 5. How a Browser Works (The Internal Process)

A browser doesn't just "show" text; it performs two main technical tasks: **Parsing** and **Rendering**.

### A. Parsing (Building the Tree)

When the browser receives raw data (bytes) from a server, it converts them into characters $\rightarrow$ then into tokens $\rightarrow$ then into **nodes**.
These nodes are organized into a tree-like structure called the **DOM (Document Object Model)**. Think of the DOM as a map of your website.

### B. Rendering (Drawing the Screen)

Once the **DOM Tree** is ready, the browser goes through every node in that tree and draws (renders) it onto your screen.

---


Don't worry about these terms like `DOM TREE`, We will be discussing more about DOM Tree in detail in Javascript section.
