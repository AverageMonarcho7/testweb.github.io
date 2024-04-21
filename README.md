```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome Page</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #add8e6; /* Light blue background */
            color: #333;
        }
        h1 {
            font-size: 2em;
            opacity: 0; /* Start with the text being invisible */
            transition: opacity 2s ease; /* Animation to change the opacity */
        }
        .emoji {
            font-size: 3em; /* Larger emoji size */
            opacity: 0; /* Start with the emoji being invisible */
            transition: opacity 2s ease; /* Animation for opacity */
            animation: spin 2s infinite linear; /* Spinning animation */
        }
        @keyframes spin {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
    </style>
</head>
<body>
    <h1 id="greeting">My name is Kevin Sacramento.</h1>
    <div class="emoji" id="emoji">👍</div>

    <script>
        function displayContent() {
            document.getElementById('greeting').style.opacity = 1; // Fade in the greeting text
            document.getElementById('emoji').style.opacity = 1; // Fade in the emoji
            console.log("Hello Kevin! Your personalized greeting and emoji are now visible.");
        }

        // Delay the display of the greeting and emoji by 3 seconds
        setTimeout(displayContent, 3000);
    </script>
</body>
</html>
