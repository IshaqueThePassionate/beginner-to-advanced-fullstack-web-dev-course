#  Module 01.11: HTML Lists

In our daily lives, we use lists for everything—from grocery shopping to to-do tasks. Similarly, in web development, lists are the standard way to group related pieces of information so they are easy for users to read and for browsers to understand.

---

## 1. Types of HTML Lists

HTML offers three distinct ways to group your data. Every list consists of a "Container" tag and one or more **List Items** (`<li>`).

### **A. Unordered List (`<ul>`)**

This is used when the **order of items does not matter**. By default, the browser displays these items with small black circles (bullets).

* **Common Use:** Navigation menus, features lists, or shopping items.

### **B. Ordered List (`<ol>`)**

This is used when the **sequence is important**. The browser automatically numbers these items (1, 2, 3...). You can also change the style to Roman numerals (I, II, III) or letters (A, B, C).

* **Common Use:** Step-by-step instructions, recipes, or top-ranking charts.

### **C. Definition List (`<dl>`)**

This acts like a dictionary or a glossary. It pairs a **Term** with its **Definition**.

* **Common Use:** FAQ sections, glossaries, or metadata displays.

---

## 2. Syntax Overview

### **Unordered List**

```html
<ul>
  <li>Apple</li>
  <li>Banana</li>
</ul>

```

### **Ordered List**

```html
<ol>
  <li>Open the door</li>
  <li>Enter the room</li>
</ol>

```

### **Definition List**

Unlike the others, this uses three tags: `<dl>` (list), `<dt>` (term), and `<dd>` (description).

```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>
</dl>

```

---

##  Execution Code Snippet

Copy this into your `index.html` to see the three different list styles side-by-side:

```html
<!DOCTYPE html>
<html>
<head>
    <title>HTML Lists Practice</title>
</head>
<body>

    <h1>HTML List Varieties</h1>

    <h3>Shopping List (Unordered)</h3>
    <ul>
        <li>Milk</li>
        <li>Eggs</li>
        <li>Bread</li>
    </ul>

    <hr />

    <h3>Recipe Steps (Ordered)</h3>
    <ol>
        <li>Boil water</li>
        <li>Add tea leaves</li>
        <li>Add sugar and milk</li>
    </ol>

    <hr />

    <h3>Coding Glossary (Definition)</h3>
    <dl>
        <dt>CSS</dt>
        <dd>Used to style and layout web pages.</dd>
        
        <dt>JavaScript</dt>
        <dd>Used to add interactivity to websites.</dd>
    </dl>

</body>
</html>

```

---
<br>

#  2. HTML Tables

HTML tables allow you to arrange data—like text, images, and links—into a structured grid of rows and columns. They are perfect for displaying schedules, price lists, or student records.

---

## 1. Basic Table Elements

A table is built using a specific hierarchy of tags. You start with a container and then define rows and data cells.

* **`<table>`**: The main container for the table.
* **`<tr>`**: (Table Row) Defines a horizontal row of cells.
* **`<th>`**: (Table Heading) Defines a header cell. Text inside is usually **bold** and centered by default.
* **`<td>`**: (Table Data) Defines a standard cell for your content.

---

## 2. Advanced Layout: Rowspan and Colspan

Sometimes you need a cell to take up more than one "slot" in the grid. We use two special attributes for this:

* **`colspan`**: Merges multiple **columns** into one wide cell.
* **`rowspan`**: Merges multiple **rows** into one tall cell.

**Code Example:**

```html
<table border="1">
  <tr>
    <th colspan="2">Merged Header (2 Columns)</th>
  </tr>
  <tr>
    <td rowspan="2">Merged Cell (2 Rows)</td>
    <td>Standard Cell</td>
  </tr>
  <tr>
    <td>Standard Cell</td>
  </tr>
</table>

```

---

## 3. Structural Tags (Semantic Tables)

For complex tables, we use structural tags to help browsers and search engines understand which part is the header, body, or summary.

* **`<caption>`**: Provides a title for the table (placed right after the opening `<table>` tag).
* **`<thead>`**: Groups the header content.
* **`<tbody>`**: Groups the main body content.
* **`<tfoot>`**: Groups the footer/summary content (often used for totals).
* **`<colgroup>`**: Allows you to apply styles (like background colors) to entire columns at once.

---

## 4. Accessibility and SEO

To make your tables professional and "screen-reader friendly," use the **`scope`** attribute inside the `<th>` tag. It tells the browser if a header is for a **col** (column) or a **row**.

```html
<th scope="col">Employee Name</th>

```

---

##  Execution Code Snippet

Copy this into your `index.html` to see a complete, professional table structure in action:

```html
<!DOCTYPE html>
<html>
<head>
    <title>HTML Tables Practice</title>
</head>
<body>

    <table border="1" cellpadding="10" cellspacing="0">
        <caption>Project Team Salaries</caption>
       
        <thead>
            <tr>
                <th scope="col">ID</th>
                <th scope="col">Name</th>
                <th scope="col">Position</th>
                <th scope="col">Salary</th>
            </tr>
        </thead>
       
        <tbody>
            <tr>
                <td>1</td>
                <td>Alice</td>
                <td>Developer</td>
                <td>$80,000</td>
            </tr>
            <tr>
                <td>2</td>
                <td>Bob</td>
                <td>Designer</td>
                <td>$70,000</td>
            </tr>
        </tbody>
       
        <tfoot>
            <tr>
                <td colspan="3" style="text-align: right;"><strong>Total Budget:</strong></td>
                <td>$150,000</td>
            </tr>
        </tfoot>
    </table>

</body>
</html>

```

---
