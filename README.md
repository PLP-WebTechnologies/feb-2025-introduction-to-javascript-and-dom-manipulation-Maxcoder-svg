# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Web Page</title>
    <style>
        /* Inline CSS for styling */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }

        header {
            background-color: #333;
            color: white;
            padding: 10px 0;
            text-align: center;
        }

        main {
            padding: 20px;
        }

        section {
            margin-bottom: 20px;
        }

        button {
            padding: 10px 20px;
            margin-top: 10px;
            cursor: pointer;
            border: none;
            background-color: #4CAF50;
            color: white;
            font-size: 16px;
        }

        button:hover {
            background-color: #45a049;
        }

        footer {
            text-align: center;
            padding: 10px;
            background-color: #333;
            color: white;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <header>
        <h1>Interactive Web Page</h1>
    </header>

    <!-- Main Content Section -->
    <main>
        <section>
            <h2>Change Text and Styles</h2>
            <p id="text-content">This is some text that will change when you click the button below.</p>
            <button id="change-text-btn">Change Text</button>
        </section>

        <section>
            <h2>Modify Styles</h2>
            <p id="styled-paragraph">This text will change style when you click the button below.</p>
            <button id="change-style-btn">Change Style</button>
        </section>

        <section>
            <h2>Dynamic Element Addition</h2>
            <button id="add-element-btn">Add New Element</button>
        </section>
    </main>

    <!-- Footer Section -->
    <footer>
        <p>&copy; 2025 My Interactive Web Page</p>
    </footer>

    <!-- Embedded JavaScript -->
    <script>
        // 1. Change text content dynamically
        const changeTextButton = document.getElementById('change-text-btn');
        const textContent = document.getElementById('text-content');

        changeTextButton.addEventListener('click', () => {
            textContent.textContent = "The text has been changed dynamically!";
        });

        // 2. Modify CSS styles via JavaScript
        const changeStyleButton = document.getElementById('change-style-btn');
        const styledParagraph = document.getElementById('styled-paragraph');

        changeStyleButton.addEventListener('click', () => {
            styledParagraph.style.color = "blue"; // Change text color
            styledParagraph.style.fontSize = "20px"; // Change font size
            styledParagraph.style.fontWeight = "bold"; // Change font weight
        });

        // 3. Add or remove an element when a button is clicked
        const addElementButton = document.getElementById('add-element-btn');

        addElementButton.addEventListener('click', () => {
            // Create a new element (a new paragraph)
            const newElement = document.createElement('p');
            newElement.textContent = "This is a dynamically added element!";
            
            // Append the new element to the main content
            document.querySelector('main').appendChild(newElement);
        });
    </script>
</body>
</html>

