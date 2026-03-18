

#  Module 01.11: Selectors — ID vs. Class

In web development, we often need to "point" to a specific tag to change its color, size, or behavior. We do this using **IDs** and **Classes**.

---

## 1. What is an ID?

An **ID** is a **unique identifier**. Just like a person has one unique ID card number, an HTML element can have an ID that belongs *only* to it on that specific page.

* **Usage:** Use an ID when there is only **one** such element on the page (like a "Submit" button or a "Main Navigation" bar).
* **Code Example:**

```html
<div id="main-header">This is a unique header.</div>

```

---

## 2. What are Classes?

A **Class** is used to group multiple elements together. You can give the same class name to as many tags as you want.

* **Usage:** Use classes when you want to apply the **same look or behavior** to a group of elements (like making all "warning" messages red).
* **Code Example:**

```html
<p class="text-large">This is a large paragraph.</p>
<div class="text-large">This is a large div.</div>

```

---

## 3. The `<style>` Tag

To actually *see* IDs and Classes in action, we use the `<style>` tag. This tag lives in the `<head>` section and holds our **CSS** (styling) rules.

* **Selecting an ID:** Use a hash symbol (`#`) followed by the name.
* **Selecting a Class:** Use a dot symbol (`.`) followed by the name.

### Simple Implementation Example:

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    /* CSS for the ID */
    #special-box {
      border: 2px solid black;
    }

    /* CSS for the Class */
    .blue-text {
      color: blue;
    }
  </style>
</head>
<body>
  <h1 id="special-box">Unique Title</h1>
  <p class="blue-text">This is blue.</p>
  <p class="blue-text">This is also blue.</p>
</body>
</html>

```

---

## 4. Key Differences: ID vs. Class

| Feature | ID (`#`) | Class (`.`) |
| --- | --- | --- |
| **Uniqueness** | Must be **Unique**. One ID per page. | Can be **Reused**. Multiple tags, one class. |
| **Primary Use** | JavaScript and specific unique styling. | General styling for groups of elements. |
| **Specificity** | High (overrides classes). | Lower (general purpose). |

---

* Use **IDs** for things that are "one of a kind" on your page.
* Use **Classes** for things that you want to style the same way multiple times.
* Remember: In your CSS code, the **Dot (`.`)** is for Classes and the **Hash (`#`)** is for IDs.

---
