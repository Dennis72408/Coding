# Coding
index.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>DOM Manipulation Example</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <h1 id="main-heading">Welcome to My Page</h1>
  </header>

  <main>
    <section>
      <p id="text-content">This is some dynamic text.</p>
      <button id="change-text-btn">Change Text</button>
      <button id="change-style-btn">Change Style</button>
      <button id="toggle-element-btn">Add/Remove Element</button>
    </section>

    <aside id="extra-element" style="display: none;">
      <p>This is a dynamically added/removed element.</p>
    </aside>
  </main>

  <footer>
    <p>&copy; 2025 My Website</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>


---

script.js

// Change text content dynamically
document.getElementById('change-text-btn').addEventListener('click', function () {
  document.getElementById('text-content').textContent = 'The text has been changed!';
});

// Modify CSS styles dynamically
document.getElementById('change-style-btn').addEventListener('click', function () {
  const heading = document.getElementById('main-heading');
  heading.style.color = 'blue';
  heading.style.fontSize = '2.5rem';
  heading.style.backgroundColor = '#f0f0f0';
});

// Add or remove an element dynamically
document.getElementById('toggle-element-btn').addEventListener('click', function () {
  const element = document.getElementById('extra-element');
  if (element.style.display === 'none') {
    element.style.display = 'block';
  } else {
    element.style.display = 'none';
  }
});
