Assignment 9.3 — Combine Flexbox and Grid Responsively
Here is a complete assignment solution using HTML5, CSS Grid, and Flexbox. We will create a responsive landing page for a travel website called ExploreWorld.

The page includes a navigation bar, a hero section with text and an image, six feature cards, and a footer. The layout will adapt to mobile, tablet, and desktop screens.

1. Project structure
Create a folder named Assignment-9.3:


text
Assignment-9.3/
├── index.html
├── style.css
└── screenshots/
    ├── mobile.png
    ├── tablet.png
    └── desktop.png
2. HTML file — index.html
The HTML uses semantic elements, Flexbox-friendly navigation, a hero section, and six feature cards.


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Explore amazing destinations with ExploreWorld.">
    <title>Assignment 9.3 - ExploreWorld</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Header and Navigation -->
    <header class="site-header">
        <div class="container navbar">
            <a href="#home" class="logo">ExploreWorld</a>

            <nav aria-label="Main navigation">
                <a href="#home">Home</a>
                <a href="#features">Features</a>
                <a href="#about">About</a>
            </nav>

            <a href="#features" class="nav-button">Explore Now</a>
        </div>
    </header>

    <main>
        <!-- Hero Section -->
        <section class="hero container" id="home">
            <div class="hero-content">
                <p class="eyebrow">DISCOVER SOMETHING NEW</p>

                <h1>Explore the World, One Journey at a Time</h1>

                <p class="hero-description">
                    Find beautiful destinations, experience new cultures,
                    and create unforgettable memories with ExploreWorld.
                </p>

                <div class="hero-actions">
                    <a href="#features" class="button button-primary">
                        Discover Places
                    </a>
                    <a href="#about" class="button button-secondary">
                        Learn More
                    </a>
                </div>
            </div>

            <div class="hero-image">
                <img
                    src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?auto=format&fit=crop&w=1200&q=85"
                    alt="Majestic mountain peaks surrounded by clouds">
            </div>
        </section>

        <!-- Features Section -->
        <section class="features-section" id="features">
            <div class="container">
                <div class="section-heading">
                    <p class="eyebrow">WHY CHOOSE US</p>
                    <h2>Make Every Trip Special</h2>
                    <p>
                        Everything you need to make your next adventure
                        memorable, comfortable, and exciting.
                    </p>
                </div>

                <div class="features-grid">

                    <article class="feature-card">
                        <img
                            src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=800&q=80"
                            alt="Beautiful mountain landscape">
                        <div class="card-content">
                            <h3>Beautiful Destinations</h3>
                            <p>
                                Discover breathtaking landscapes and
                                remarkable places around the world.
                            </p>
                            <a href="#about" class="card-link">Learn more →</a>
                        </div>
                    </article>

                    <article class="feature-card">
                        <img
                            src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=800&q=80"
                            alt="Tropical beach with blue ocean">
                        <div class="card-content">
                            <h3>Relaxing Getaways</h3>
                            <p>
                                Escape your busy routine and enjoy peaceful
                                beaches and relaxing holidays.
                            </p>
                            <a href="#about" class="card-link">Learn more →</a>
                        </div>
                    </article>

                    <article class="feature-card">
                        <img
                            src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?auto=format&fit=crop&w=800&q=80"
                            alt="Peaceful lake surrounded by mountains">
                        <div class="card-content">
                            <h3>Nature Adventures</h3>
                            <p>
                                Explore forests, lakes, and mountains
                                while enjoying the natural world.
                            </p>
                            <a href="#about" class="card-link">Learn more →</a>
                        </div>
                    </article>

                    <article class="feature-card">
                        <img
                            src="https://images.unsplash.com/photo-1519608487953-e999c86e7455?auto=format&fit=crop&w=800&q=80"
                            alt="Starry sky above a natural landscape">
                        <div class="card-content">
                            <h3>Unique Experiences</h3>
                            <p>
                                Make lasting memories with experiences
                                that take you beyond the ordinary.
                            </p>
                            <a href="#about" class="card-link">Learn more →</a>
                        </div>
                    </article>

                    <article class="feature-card">
                        <img
                            src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?auto=format&fit=crop&w=800&q=80"
                            alt="Green forest illuminated by sunlight">
                        <div class="card-content">
                            <h3>Eco-Friendly Travel</h3>
                            <p>
                                Discover responsible ways to travel
                                and help preserve beautiful places.
                            </p>
                            <a href="#about" class="card-link">Learn more →</a>
                        </div>
                    </article>

                    <article class="feature-card">
                        <img
                            src="https://images.unsplash.com/photo-1476514525535-07fb3b4ae5f1?auto=format&fit=crop&w=800&q=80"
                            alt="Travel destination beside a beautiful lake">
                        <div class="card-content">
                            <h3>Memorable Journeys</h3>
                            <p>
                                Turn your travel dreams into memorable
                                adventures with every new journey.
                            </p>
                            <a href="#about" class="card-link">Learn more →</a>
                        </div>
                    </article>

                </div>
            </div>
        </section>

        <!-- About Section -->
        <section class="about-section container" id="about">
            <h2>Your Next Adventure Starts Here</h2>
            <p>
                ExploreWorld inspires travelers to discover new places,
                appreciate different cultures, and experience the beauty
                of our planet.
            </p>
            <a href="#home" class="button button-primary">Back to Top</a>
        </section>
    </main>

    <!-- Footer -->
    <footer class="site-footer">
        <p>&copy; 2026 ExploreWorld. All rights reserved.</p>
    </footer>

</body>
</html>
3. CSS file — style.css
This stylesheet uses Flexbox for the header, navigation, and hero alignment, and CSS Grid for the feature cards. Media queries change the layout for smaller screens.


css

/* Assignment 9.3: Flexbox and Grid Responsive Landing Page */

/* 1. Global styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.6;
    color: #263238;
    background-color: #ffffff;
}

img {
    display: block;
    width: 100%;
    max-width: 100%;
}

a {
    text-decoration: none;
}

.container {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 16px;
}

/* 2. Header and navbar - Flexbox */
.site-header {
    background-color: #ffffff;
    border-bottom: 1px solid #e5e7eb;
}

.navbar {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 14px;
    padding-top: 18px;
    padding-bottom: 18px;
}

.logo {
    color: #176b52;
    font-size: 25px;
    font-weight: 800;
}

.navbar nav {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 18px;
}

.navbar nav a {
    color: #374151;
    font-size: 14px;
}

.navbar nav a:hover {
    color: #176b52;
}

.nav-button {
    display: inline-block;
    padding: 9px 16px;
    border-radius: 6px;
    background-color: #176b52;
    color: white;
    font-size: 14px;
}

/* 3. Hero section - Flexbox */
.hero {
    display: flex;
    flex-direction: column;
    gap: 30px;
    padding-top: 40px;
    padding-bottom: 50px;
}

.hero-content {
    flex: 1;
    min-width: 0;
}

.eyebrow {
    margin-bottom: 12px;
    color: #16805d;
    font-size: 12px;
    font-weight: bold;
    letter-spacing: 2px;
}

.hero h1 {
    margin-bottom: 18px;
    color: #163c32;
    font-size: clamp(32px, 6vw, 52px);
    line-height: 1.15;
    overflow-wrap: break-word;
}

.hero-description {
    max-width: 520px;
    margin-bottom: 24px;
    color: #5b6470;
    font-size: 16px;
}

.hero-actions {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 12px;
}

.button {
    display: inline-block;
    padding: 12px 18px;
    border-radius: 6px;
    font-size: 14px;
    font-weight: bold;
    text-align: center;
}

.button-primary {
    background-color: #176b52;
    color: white;
}

.button-primary:hover {
    background-color: #10543f;
}

.button-secondary {
    border: 1px solid #176b52;
    color: #176b52;
}

.hero-image {
    flex: 1;
    min-width: 0;
}

.hero-image img {
    width: 100%;
    height: 280px;
    object-fit: cover;
    border-radius: 14px;
}

/* 4. Features section */
.features-section {
    padding: 55px 0;
    background-color: #f3f8f5;
}

.section-heading {
    max-width: 650px;
    margin: 0 auto 32px;
    text-align: center;
}

.section-heading h2,
.about-section h2 {
    margin-bottom: 12px;
    color: #163c32;
    font-size: clamp(26px, 4vw, 36px);
    line-height: 1.25;
}

.section-heading > p:last-child {
    color: #647067;
    font-size: 15px;
}

/* CSS Grid: one column by default */
.features-grid {
    display: grid;
    grid-template-columns: minmax(0, 1fr);
    gap: 22px;
}

.feature-card {
    display: flex;
    flex-direction: column;
    min-width: 0;
    overflow: hidden;
    background-color: #ffffff;
    border: 1px solid #e6ece8;
    border-radius: 10px;
    box-shadow: 0 4px 14px rgba(24, 60, 45, 0.06);
}

.feature-card > img {
    width: 100%;
    height: 210px;
    object-fit: cover;
}

.card-content {
    display: flex;
    flex: 1;
    flex-direction: column;
    align-items: flex-start;
    padding: 20px;
}

.card-content h3 {
    margin-bottom: 10px;
    color: #163c32;
    font-size: 19px;
    line-height: 1.35;
}

.card-content p {
    margin-bottom: 18px;
    color: #647067;
    font-size: 14px;
}

.card-link {
    margin-top: auto;
    color: #176b52;
    font-size: 14px;
    font-weight: bold;
}

.card-link:hover {
    text-decoration: underline;
}

/* 5. About section */
.about-section {
    padding-top: 55px;
    padding-bottom: 55px;
    text-align: center;
}

.about-section p {
    max-width: 650px;
    margin: 0 auto 22px;
    color: #5b6470;
}

/* 6. Footer */
.site-footer {
    padding: 22px 16px;
    background-color: #163c32;
    color: #ffffff;
    text-align: center;
    font-size: 14px;
}

/* BREAKPOINT 1: Tablets */
@media screen and (min-width: 600px) {
    .container {
        padding-right: 24px;
        padding-left: 24px;
    }

    .navbar {
        flex-direction: row;
        justify-content: space-between;
        gap: 16px;
    }

    .navbar nav {
        gap: 16px;
    }

    .nav-button {
        white-space: nowrap;
    }

    .hero {
        flex-direction: row;
        align-items: center;
        gap: 28px;
        padding-top: 60px;
        padding-bottom: 65px;
    }

    .hero-content,
    .hero-image {
        flex: 1;
        min-width: 0;
    }

    .hero-image img {
        height: 350px;
    }

    .features-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
        gap: 24px;
    }
}

/* BREAKPOINT 2: Desktops */
@media screen and (min-width: 1024px) {
    .container {
        padding-right: 32px;
        padding-left: 32px;
    }

    .navbar {
        padding-top: 22px;
        padding-bottom: 22px;
    }

    .navbar nav {
        gap: 28px;
    }

    .hero {
        gap: 55px;
        padding-top: 80px;
        padding-bottom: 90px;
    }

    .hero-image img {
        height: 430px;
    }

    .features-section {
        padding-top: 75px;
        padding-bottom: 75px;
    }

    .features-grid {
        grid-template-columns: repeat(3, minmax(0, 1fr));
        gap: 28px;
    }

    .feature-card > img {
        height: 220px;
    }

    .feature-card {
        transition: transform 0.25s ease,
                    box-shadow 0.25s ease;
    }

    .feature-card:hover {
        transform: translateY(-4px);
        box-shadow: 0 10px 24px rgba(24, 60, 45, 0.12);
    }
}
4. How Flexbox and Grid are used
Section

CSS technique

Purpose

Navigation bar

Flexbox

Aligns logo, links, and button

Hero section

Flexbox

Places text and image side by side on larger screens

Feature cards

CSS Grid

Creates a responsive card layout

Card content

Flexbox

Arranges titles, descriptions, and links vertically

Responsive layout

Media queries

Changes the number of columns based on screen width

5. Expected responsive layout
Mobile view
Nature Company - MAST CSS Framework - Webflow
Below 600px: vertically stacked navigation, hero content, and one feature card per row.

Tablet view
Travel Website UIUX Design by ilias miah ✪ for Confidency on Dribbble
600px and above: horizontal hero layout and two feature cards per row.

Desktop view
Way.Farer - Adventure Travel Landing Page by Catalystco Studio | Layers
1024px and above: horizontal navigation, side-by-side hero, and three feature cards per row.

These images are visual references for the expected design, not screenshots of your running code.

6. How to run and test
Save index.html and style.css in the same folder.

Open index.html in Google Chrome.

Press F12 to open Chrome DevTools.

Press Ctrl + Shift + M to enable Device Mode.

Test the following viewport widths:

Device

Width

Expected result

Mobile

375px

One card per row

Tablet

768px

Two cards per row

Desktop

1440px

Three cards per row

Check that the navigation fits, the hero image does not overlap the text, and no horizontal scrolling appears.

7. Assignment report
Writing


Assignment 9.3 — Combine Flexbox and Grid Responsively
Objective: To create a responsive landing page using CSS Flexbox and CSS Grid.

Technologies Used: HTML5, CSS3, Google Chrome DevTools.

Implementation:

Created a header and navigation bar using Flexbox.
Designed a hero section containing text, buttons, and an image.
Added six feature cards using semantic HTML.
Used CSS Grid to arrange the feature cards into responsive columns.
Used Flexbox to align the navigation, hero content, and card content.
Added media queries at 600px and 1024px.
Converted the feature section to one column on mobile, two columns on tablets, and three columns on desktops.
Used consistent spacing, responsive images, and hover effects.
Tested the webpage at mobile, tablet, and desktop viewport sizes.
Result: The landing page adjusts to different screen sizes while maintaining proper alignment, spacing, and readability.

Conclusion: This assignment demonstrates how CSS Flexbox and CSS Grid can work together to build modern, responsive web layouts.