# fierce
<!DOCTYPE html>
<html>
<head>
    <title>My Website</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
    <script src="script.js"></script>
    <style>
        /* CSS styles specific to this page */
        .highlight {
            background-color: yellow;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to My Website</h1>
    </header>

    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>

    <section>
        <h2>About</h2>
        <p>This is a brief description of my website.</p>
    </section>

    <section>
        <h2>Services</h2>
        <ul>
            <li>Service 1</li>
            <li>Service 2</li>
            <li>Service 3</li>
        </ul>
    </section>

    <section>
        <h2>Contact</h2>
        <form>
            <label for="name">Name:</label>
            <input type="text" id="name" name="name">

            <label for="email">Email:</label>
            <input type="email" id="email" name="email">

            <label for="message">Message:</label>
            <textarea id="message" name="message"></textarea>

            <input type="submit" value="Submit">
        </form>
    </section>

    <section>
        <h2>Gallery</h2>
        <div class="gallery">
            <img src="![Uploading jag f type.jpg…]()
.jpg" alt="Image 1">
            <img src="image2.jpg" alt="Image 2">
            <img src="image3.jpg" alt="Image 3">
        </div>
    </section>

    <footer>
        <p>&copy; 2023 My Website. All rights reserved.</p>
    </footer>

    <script>
        // JavaScript code for interactivity
        const inputs = document.querySelectorAll('input');

        inputs.forEach(input => {
            input.addEventListener('focus', function() {
                this.classList.add('highlight');
            });

            input.addEventListener('blur', function() {
                this.classList.remove('highlight');
            });
        });
    </script>
</body>
</html>
