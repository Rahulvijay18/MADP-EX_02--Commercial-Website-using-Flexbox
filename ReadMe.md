# Ex02 Commercial Website
## Date: 13/08/2025

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM

### index.html

```

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EcoTravel</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <div class="logo">EcoTravel</div>
        <nav>
            <ul>
                <li><a href="#hero">Home</a></li>
                <li><a href="#destinations">Destinations</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="hero">
        <div class="hero-content">
            <h1>Travel Green, Explore the World</h1>
            <p>Discover beautiful destinations while protecting the planet.</p>
            <a href="#destinations" class="btn">Start Your Journey</a>
        </div>
    </section>

    <!-- Destinations Section -->
    <section id="destinations">
        <h2>Popular Eco Destinations</h2>
        <div class="recipe-grid">
            <div class="recipe-card">
                <img src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e" alt="Maldives Beach">
                <h3>Maldives Eco Beach</h3>
            </div>
            <div class="recipe-card">
                <img src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee" alt="Mountain Trekking">
                <h3>Himalayan Trek</h3>
            </div>
            <div class="recipe-card">
                <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb" alt="Forest Adventure">
                <h3>Amazon Rainforest</h3>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <h2>About EcoTravel</h2>
        <p>EcoTravel is committed to promoting sustainable tourism that helps protect our planet.
           We curate eco-friendly destinations and experiences that bring you closer to nature 
           without harming the environment. Let’s make every trip a step towards a greener future.</p>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2>Contact Us</h2>
        <a href="mailto:contact@ecotravel.com" class="btn">Email Us</a>
        <a href="tel:+123456789" class="btn">Call Us</a>
    </section>

    <footer>
        <p>© 2025 EcoTravel. All rights reserved.</p>
    </footer>

</body>
</html>

```

### style.css

```
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

body {
    line-height: 1.6;
}

/* Header */
header {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    padding: 20px 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 10;
}

.logo {
    color: #fff;
    font-size: 24px;
    font-weight: bold;
    position: absolute;
    left: 50px;
}

nav ul {
    display: flex;
    list-style: none;
}

nav ul li {
    margin-left: 20px;
}

nav ul li a {
    text-decoration: none;
    color: #fff;
    font-weight: 500;
    transition: 0.3s;
}

nav ul li a:hover {
    color: #00ff99;
}

/* Hero Section */
#hero {
    height: 100vh;
    position: relative;
    background: url('https://images.unsplash.com/photo-1507525428034-b723cf961d3e') no-repeat center center/cover;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    color: #fff;
    padding: 0 20px;
}

#hero::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.4);
    z-index: 1;
}

.hero-content {
    position: relative;
    z-index: 2;
}

.hero-content h1 {
    font-size: 48px;
    margin-bottom: 15px;
}

.hero-content p {
    font-size: 18px;
    margin-bottom: 20px;
}

.btn {
    display: inline-block;
    padding: 10px 20px;
    background: #00cc88;
    color: #fff;
    text-decoration: none;
    border-radius: 5px;
    transition: 0.3s;
}

.btn:hover {
    background: #009966;
}

/* Destinations Section */
#destinations {
    padding: 50px 20px;
    text-align: center;
}

.recipe-grid {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 20px;
    margin-top: 20px;
}

.recipe-card {
    background: #fff;
    border-radius: 8px;
    overflow: hidden;
    width: 300px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}

.recipe-card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
}

.recipe-card h3 {
    padding: 15px;
}

/* About Section */
#about {
    padding: 50px 20px;
    background: #f0fdf4;
    text-align: center;
}

#about p {
    max-width: 800px;
    margin: auto;
    font-size: 18px;
}

/* Contact Section */
#contact {
    padding: 50px 20px;
    text-align: center;
}

#contact .btn {
    margin: 10px;
}

/* Footer */
footer {
    text-align: center;
    padding: 20px;
    background: #333;
    color: #fff;
}

```

## OUTPUT

![alt text](<Screenshot 2025-08-13 210811.png>)

![alt text](<Screenshot 2025-08-13 210826.png>)

![alt text](<Screenshot 2025-08-13 210834.png>) 


## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
