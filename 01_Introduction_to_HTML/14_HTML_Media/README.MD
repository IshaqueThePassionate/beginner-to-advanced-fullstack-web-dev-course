#  Module 01.14: Video & Audio Tags

In modern web development, embedding multimedia is essential for creating dynamic and engaging experiences. HTML provides native `<video>` and `<audio>` tags, meaning you can play media directly in the browser without needing external plugins.

---

## 1. The `<video>` Tag

The `<video>` tag is used to embed video files. It is a paired tag that requires a closing `</video>`.

**Basic Syntax:**

```html
<video src="video.mp4" controls></video>

```

### Essential Video Attributes:

* **`src`**: The path to your video file.
* **`controls`**: **Crucial.** Adds the play/pause button, volume slider, and fullscreen toggle. Without this, the video won't have a user interface.
* **`autoplay`**: Starts the video immediately when the page loads (Note: Browsers often require `muted` for this to work).
* **`loop`**: Restarts the video automatically once it finishes.
* **`muted`**: Turns off the sound by default.
* **`poster`**: Displays a specific image (like a thumbnail) before the user clicks play.
* **`width` & `height**`: Sets the size of the video player on the screen.

---

## 2. The `<audio>` Tag

The `<audio>` tag works very similarly to the video tag but is designed specifically for sound files like music or podcasts.

**Basic Syntax:**

```html
<audio src="music.mp3" controls></audio>

```

### Essential Audio Attributes:

* **`src`**: The path to your audio file (e.g., .mp3, .wav, .ogg).
* **`controls`**: Displays the audio player interface.
* **`preload`**: This attribute tells the browser how much of the file to download when the page loads:
* **`none`**: Does not download anything until the user clicks play (saves data).
* **`metadata`**: Only downloads basic info like the duration of the track.
* **`auto`**: Downloads the whole file in the background so it's ready to play instantly.



---

## 3. Comparison of Media Attributes

| Attribute | Video Tag | Audio Tag | Purpose |
| --- | --- | --- | --- |
| **`src`** | ✅ | ✅ | Path to the file |
| **`controls`** | ✅ | ✅ | Shows Play/Pause/Volume |
| **`autoplay`** | ✅ | ✅ | Plays on page load |
| **`poster`** | ✅ | ❌ | Show thumbnail image |
| **`preload`** | ✅ | ✅ | Manages background loading |

---

## 🚀 Execution Code Snippet

Copy this into your `index.html` to see how video and audio players behave in your browser:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Multimedia Practice</title>
</head>
<body>

    <h1>HTML Multimedia Lab</h1>

    <h3>1. Video Example</h3>
    <video src="sample-video.mp4" 
           controls 
           width="400" 
           poster="thumbnail.jpg"
           muted>
        Your browser does not support the video tag.
    </video>

    <hr />

    <h3>2. Audio Example</h3>
    <p>Listen to this track:</p>
    <audio src="podcast-intro.mp3" 
           controls 
           preload="metadata">
        Your browser does not support the audio tag.
    </audio>

</body>
</html>

```

---

## Summary

* Always include the **`controls`** attribute; otherwise, your user cannot play the media!
* If you use **`autoplay`**, it is best practice to also use **`muted`**, as most browsers block sound that starts automatically.
* You can put text inside the tags (e.g., "Your browser does not support...") as a fallback for very old browsers.
---

<br>

# 2. SVG in HTML

**Scalable Vector Graphics (SVG)** is a powerful tool for modern web development. Unlike traditional images (like PNG or JPG), SVGs are made of mathematical paths, meaning they stay perfectly sharp and crisp no matter how much you zoom in or how large the screen is.

---

## 1. What is SVG?

SVG stands for **Scalable Vector Graphics**.

* **Vector-based:** Instead of being made of colored pixels, an SVG is made of mathematical formulas that describe lines, circles, and polygons.
* **Resolution Independent:** Because it’s math-based, an SVG looks exactly the same on a small smartphone and a massive 4K monitor.

---

## 2. Why Use SVG?

* **Scalability:** You can scale them indefinitely without any "blurriness."
* **File Size:** For icons and logos, SVG files are usually much smaller than PNGs.
* **Editability:** Since SVG is basically XML code, you can change its color or animate it using **CSS** and **JavaScript**.

---

## 3. How to Embed SVG in HTML

There are three main ways to put an SVG on your website:

### **A. Inline SVG**

You paste the SVG code directly into your HTML. This is the best method if you want to change colors or animate parts of the image with CSS.

```html
<svg height="100" width="100">
    <circle cx="50" cy="50" r="40" stroke="black" stroke-width="3" fill="red" />
</svg>

```

### **B. Using the `<img>` Tag**

You treat the SVG like a normal image file. This keeps your HTML clean but makes it harder to style specific parts of the graphic.

```html
<img src="logo.svg" alt="Company Logo">

```

### **C. CSS Background**

You can set an SVG as a background image for a `div` or any other element.

```css
.icon-box {
    background-image: url('icon.svg');
}

```

---

## 4. Key SVG Attributes

To control how your vector looks, you use these common attributes:

* **`width` and `height**`: Sets the size of the graphic.
* **`viewBox`**: Defines the "internal coordinate system" (the canvas size inside the code).
* **`fill`**: The background color of the shape.
* **`stroke`**: The color of the outline.
* **`stroke-width`**: The thickness of the outline.

---

## Execution Code Snippet

Copy this into your `index.html` to see how easy it is to draw shapes directly with code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>SVG Practice</title>
</head>
<body>

    <h1>Drawing with SVG</h1>

    <h3>1. A Simple Circle</h3>
    <svg width="100" height="100">
        <circle cx="50" cy="50" r="40" stroke="green" stroke-width="4" fill="yellow" />
    </svg>

    <hr />

    <h3>2. A Simple Square</h3>
    <svg width="100" height="100">
        <rect width="80" height="80" x="10" y="10" fill="blue" stroke="black" stroke-width="2" />
    </svg>

    <p>Try zooming into this page—notice how the shapes stay perfectly sharp!</p>

</body>
</html>

```

---

##  Summary 

* Use **Inline SVG** when you need to change colors or animate the graphic.
* Use the **`<img>` tag** for simple icons that don't need to change.
* Always provide an **`alt`** attribute when using the image tag for accessibility.

---

<br>

# 3. iFrames (Inline Frames)

An **iFrame** (short for Inline Frame) is a powerful HTML element that acts like a "window" on your website. It allows you to embed an entire second HTML document inside your current page. This is how you see YouTube videos, Google Maps, or social media posts integrated into other websites.

---

## 1. What is an iFrame?

Think of an iFrame as a webpage within a webpage. It enables you to display external content without forcing the user to leave your site.

---

## 2. Why Use iFrames?

iFrames are used whenever you need to bring in content that doesn't belong to your site:

* **Modularity:** Easily embed third-party widgets like weather reports, stock tickers, or Twitter feeds.
* **Content Isolation:** The code inside the iFrame is separate from your main site, which provides a layer of security and prevents styles from clashing.
* **Resource Separation:** An iFrame can load its content independently, so if the embedded content is slow, it won't stop your main page from loading.

---

## 3. Basic Syntax & Attributes

The syntax is simple, but it requires specific attributes to look and behave correctly.

**Syntax:**

```html
<iframe src="URL" width="500" height="300"></iframe>

```

### Key Attributes:

| Attribute | Description |
| --- | --- |
| **`src`** | The URL of the page or media you want to embed. |
| **`width` / `height**` | Defines the size of the "window" in pixels or percentages. |
| **`frameborder`** | Set to "0" to remove the border around the frame. |
| **`allowfullscreen`** | Often used for videos to allow the user to expand them. |
| **`name`** | Used to target the iFrame with links or JavaScript. |

---

## 4. Practical Examples

### **Embedding a YouTube Video**

To embed a video, you must use the "Embed" URL provided by YouTube (which uses the `/embed/` path).

```html
<iframe width="560" height="315" src="https://www.youtube.com/embed/dQw4w9WgXcQ" frameborder="0" allowfullscreen></iframe>

```

### **Embedding Google Maps**

This is perfect for "Contact Us" pages to show your business location.

```html
<iframe src="https://www.google.com/maps/embed?pb=..." width="600" height="450" style="border:0;" allowfullscreen=""></iframe>

```

---

##  Execution Code Snippet

Copy this into your `index.html` to see how an iFrame can display another website or video:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>iFrame Practice</title>
</head>
<body>

    <h1>Embedding External Content</h1>

    <h3>1. Embedding a Webpage</h3>
    <p>Below is a small window showing a specific URL:</p>
    <iframe src="https://www.wikipedia.org" width="100%" height="300" title="Wikipedia Frame"></iframe>

    <hr />

    <h3>2. Embedding a Video</h3>
    <iframe width="400" height="225" 
            src="https://www.youtube.com/embed/ScMzIvxBSi4" 
            title="YouTube video player" 
            frameborder="0" 
            allowfullscreen>
    </iframe>

</body>
</html>

```

---

## Summary 

* **Security:** Many major websites (like Google or Facebook) block themselves from being put in iFrames for security reasons. If a link doesn't work in your iFrame, it's likely being blocked by that site.
* **Title Attribute:** Always add a `title` attribute to your iFrame for **Accessibility**. It helps screen readers tell the user what is inside the frame.
* **Responsive:** Use `width="100%"` to make the iFrame adjust to different screen sizes.

