# ideal semantic HTML page

- Here’s a structure for an ideal semantic HTML page using only the most important HTML5 tags for layout and readability:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Page Title</title>
</head>
<body>

  <header>
    <h1>Website Logo or Title</h1>
    <nav>
      <ul>
        <li><a href="#section1">Home</a></li>
        <li><a href="#section2">About</a></li>
        <li><a href="#section3">Services</a></li>
        <li><a href="#section4">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section id="section1">
      <h2>Home</h2>
      <p>Introductory content...</p>
    </section>

    <section id="section2">
      <h2>About</h2>
      <article>
        <h3>Our Mission</h3>
        <p>Details about the mission...</p>
      </article>
      <article>
        <h3>Our Team</h3>
        <p>Details about the team...</p>
      </article>
    </section>

    <section id="section3">
      <h2>Services</h2>
      <article>
        <h3>Service One</h3>
        <p>Description of service one...</p>
      </article>
      <article>
        <h3>Service Two</h3>
        <p>Description of service two...</p>
      </article>
    </section>

    <section id="section4">
      <h2>Contact</h2>
      <form>
        <label for="name">Name:</label>
        <input type="text" id="name" name="name" />
        
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" />

        <label for="message">Message:</label>
        <textarea id="message" name="message"></textarea>

        <button type="submit">Send</button>
      </form>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Your Company. All rights reserved.</p>
  </footer>

</body>
</html>
```

## ✅ Key Semantic Tags Used

| Tag          | Purpose                          |
| ------------ | -------------------------------- |
| `<!DOCTYPE>` | Declares the HTML5 document type |
| `<html>`     | Root element                     |
| `<head>`     | Metadata, title, links, etc.     |
| `<body>`     | Main content container           |
| `<header>`   | Top area: logo, title, nav       |
| `<nav>`      | Navigation links                 |
| `<main>`     | Primary page content             |
| `<section>`  | Thematic grouping of content     |
| `<article>`  | Independent self-contained units |
| `<footer>`   | Bottom content like copyright    |
| `<form>`     | Input section for user data      |


