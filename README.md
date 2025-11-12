<!---
{
  "id": "3ee0acd9-0f99-4423-b4f3-a0ca84a16422",
  "teaches": "Creating a Simple HTML Page",
  "depends_on": ["2c7334b3-b07d-48d6-a562-79072d8e166e"],
  "author": "Stephan Bökelmann",
  "first_used": "2025-04-13",
  "keywords": ["HTML", "vim", "terminal", "basic web page", "cross-platform"]
}
--->

# Creating a Simple HTML Page

> In this exercise you will learn how to create and edit a basic HTML page. Furthermore we will explore how to preview your page in a web browser and add common HTML structures like headings, lists, tables, and internal links.

### Introduction

Building a website is a basic skill that every programmer should have. It's not just about creating flashy pages—it's about communicating ideas clearly and organizing documentation in a way that can be shared, reused, and understood by others.

HTML (HyperText Markup Language) has been a gamechanger ever since Tim Berners-Lee created the first HTTP server and browser in the early 1990s. It remains the backbone of the web today. With just a few lines of code, you can structure content that browsers interpret and display beautifully.

The best part? You don’t need a web server or internet connection to start learning. Everything begins locally—right on your own computer. All you need is a plain text editor and a browser. In this exercise, we'll use `vim`, a powerful and efficient text editor available on all major platforms. You'll create and view your first web pages, understand how HTML elements are structured, and even connect multiple pages together.

This hands-on approach will empower you to start thinking in HTML and lay the groundwork for building more complex websites and applications.


### Further Readings and Other Sources

- [MDN Web Docs: HTML Introduction](https://developer.mozilla.org/en-US/docs/Web/HTML)

---

## Tasks

### Task 1: Creating and Viewing a Minimal HTML File

1. Open your terminal and navigate to a working directory.
2. Launch vim to create a new file:
   ```sh
   vim index.html
   ```
3. Press `i` to enter INSERT mode and paste the following HTML content:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Hello World</title>
</head>
<body>
    Hello, World!
</body>
</html>
```
4. Press `Esc`, then type `:wq` and press `Enter` to save and quit.
5. Open the file in your browser using the appropriate command for your OS:
   - **Linux**:
     ```sh
     xdg-open index.html
     ```
   - **macOS**:
     ```sh
     open index.html
     ```
   - **Windows CMD or PowerShell**:
     ```powershell
     start index.html
     ```

### Task 2: Enhancing the Page with Structured Content

1. Reopen `index.html` in vim:
   ```sh
   vim index.html
   ```
2. Add the following inside the `<body>` tag after "Hello, World!":
   ```html
   <h1>Main Heading</h1>
   <h2>Subheading</h2>
   <ul>
       <li>First item</li>
       <li>Second item</li>
       <li>Third item</li>
   </ul>
   <table border="1">
       <tr><th>Name</th><th>Age</th></tr>
       <tr><td>Alice</td><td>30</td></tr>
       <tr><td>Bob</td><td>25</td></tr>
   </table>
   ```
3. Save and exit (`:wq`) and reopen in your browser using the previous command.

### Task 3: Creating and Linking a Second Page

1. Create a new file:
   ```sh
   vim second.html
   ```
2. Paste the following content:
   ```html
   <!DOCTYPE html>
   <html>
   <head><title>Second Page</title></head>
   <body>
       <h1>Welcome to the Second Page</h1>
       <a href="index.html">Go Back to Home</a>
   </body>
   </html>
   ```
3. Save and exit.
4. Edit `index.html` again and add this link somewhere in the `<body>`:
   ```html
   <p><a href="second.html">Visit the Second Page</a></p>
   ```
5. Save and test both files in the browser to confirm that navigation works.

---

## Advice

Building web pages in a text editor encourages a clear understanding of HTML structure and tag nesting. This skill is not only fundamental but also highly transferable to other contexts like Markdown, XML, or any code that relies on markup.
