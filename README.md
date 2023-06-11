# fierce
<!DOCTYPE html>
<html>
<head>
  <title>Supercar World</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <nav>
      <div class="container">
        <div class="logo">
          <a href="index.php">Supercar World</a>
        </div>
        <ul class="menu">
          <li><a href="index.php">Home</a></li>
          <li><a href="about.php">About</a></li>
          <li><a href="models.php">Models</a></li>
          <li><a href="gallery.php">Gallery</a></li>
          <li><a href="contact.php">Contact</a></li>
        </ul>
      </div>
    </nav>
  </header>

  <section class="hero">
    <div class="container">
      <h1>Welcome to Supercar World</h1>
      <p>Discover the thrill of high-performance vehicles</p>
      <a href="models.php" class="btn">Explore Models</a>
    </div>
  </section>

  <section class="about">
    <div class="container">
      <h2>About Us</h2>
      <p>Welcome to Supercar World, the ultimate destination for car enthusiasts who appreciate the finest and fastest automobiles on the planet. With our passion for supercars and commitment to excellence, we bring you the latest news, reviews, and insights into the world of high-performance vehicles.</p>
    </div>
  </section>

  <section class="models">
    <div class="container">
      <h2>Our Models</h2>
      <?php
        // Connect to the database
        $conn = mysqli_connect("localhost", "username", "password", "supercars");

        // Check connection
        if (!$conn) {
          die("Connection failed: " . mysqli_connect_error());
        }

        // Fetch models from the database
        $sql = "SELECT * FROM models";
        $result = mysqli_query($conn, $sql);

        // Display models
        if (mysqli_num_rows($result) > 0) {
          while ($row = mysqli_fetch_assoc($result)) {
            echo '<div class="model">';
            echo '<img src="' . $row['image'] . '" alt="' . $row['name'] . '">';
            echo '<h3>' . $row['name'] . '</h3>';
            echo '<p>' . $row['description'] . '</p>';
            echo '<a href="model.php?id=' . $row['id'] . '" class="btn">Learn More</a>';
            echo '</div>';
          }
        } else {
          echo '<p>No models available.</p>';
        }

        // Close the database connection
        mysqli_close($conn);
      ?>
    </div>
  </section>

  <footer>
    <div class="container">
      <p>&copy; <?php echo date('Y'); ?> Supercar World. All rights reserved.</p>
    </div>
  </footer>
</body>
</html>
