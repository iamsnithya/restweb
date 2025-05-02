# Ex.07 Restaurant Website
## Date: 01/05/2025

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:

    <!DOCTYPE html>
    <html lang="en">
    <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lemon Restaurant</title>
    <style>
        /* Reset styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
        }
        
        /* Header styles */
        header {
            background-color: rgba(0, 0, 0, 0.8);
            position: fixed;
            width: 100%;
            z-index: 100;
            padding: 15px 0;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo-icon {
            width: 40px;
            height: 40px;
            margin-right: 10px;
        }
        
        .logo-text {
            color: #fff;
            font-size: 28px;
            font-weight: 700;
            letter-spacing: 1px;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 30px;
        }
        
        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-size: 16px;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: #e74c3c;
        }
        
        /* Hero section */
        .hero {
            height: 100vh;
            background-image: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), url('https://source.unsplash.com/random/1600x900/?restaurant,food');
            background-size: cover;
            background-position: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 20px;
            color: #fff;
        }
        
        .hero h1 {
            font-size: 4rem;
            margin-bottom: 20px;
            font-weight: 700;
        }
        
        .hero p {
            font-size: 1.5rem;
            max-width: 800px;
            margin-bottom: 40px;
        }
        
        .btn {
            display: inline-block;
            background-color: #e74c3c;
            color: #fff;
            padding: 15px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-size: 1.1rem;
            font-weight: 600;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #c0392b;
        }
        
        /* Featured section */
        .featured {
            padding: 80px 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 60px;
            color: #333;
        }
        
        .dishes {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .dish {
            background-color: #fff;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        
        .dish:hover {
            transform: translateY(-10px);
        }
        
        .dish img {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }
        
        .dish-info {
            padding: 20px;
        }
        
        .dish-info h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
        }
        
        .dish-info p {
            color: #666;
            margin-bottom: 15px;
        }
        
        .price {
            font-weight: 700;
            color: #e74c3c;
            font-size: 1.2rem;
        }
        
        /* About section */
        .about {
            background-color: #f9f9f9;
            padding: 80px 20px;
        }
        
        .about-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }
        
        .about-img {
            width: 100%;
            height: 400px;
            object-fit: cover;
            border-radius: 10px;
        }
        
        .about-info h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }
        
        .about-info p {
            margin-bottom: 20px;
            color: #666;
        }
        
        /* Footer */
        footer {
            background-color: #333;
            color: #fff;
            padding: 50px 20px;
            text-align: center;
        }
        
        .footer-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
        }
        
        .footer-section h3 {
            margin-bottom: 20px;
            font-size: 1.3rem;
        }
        
        .footer-section p {
            margin-bottom: 10px;
            color: #ccc;
        }
        
        .social-icons {
            display: flex;
            justify-content: center;
            margin-top: 20px;
        }
        
        .social-icons a {
            color: #fff;
            margin: 0 10px;
            font-size: 1.5rem;
        }
        
        .copyright {
            margin-top: 30px;
            color: #ccc;
            font-size: 0.9rem;
        }
        
        /* Media queries */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
            
            .about-container {
                grid-template-columns: 1fr;
            }
            
            .header-container {
                flex-direction: column;
            }
            
            nav ul {
                margin-top: 20px;
            }
            
            nav ul li {
                margin: 0 10px;
            }
        }
    </style>
    </head>
    <body>
    <!-- Header -->
    <header>
        <div class="header-container">
            <div class="logo">
                <svg class="logo-icon" viewBox="0 0 60 60" xmlns="http://www.w3.org/2000/svg">
                    <circle cx="30" cy="30" r="25" fill="#e74c3c"/>
                    <path d="M20,20 C25,15 35,15 40,20 C45,25 45,35 40,40 C35,45 25,45 20,40 C15,35 15,25 20,20 Z" fill="#fff"/>
                    <circle cx="30" cy="30" r="5" fill="#e74c3c"/>
                </svg>
                <div class="logo-text">Lemon Restaurant</div>
            </div>
            <nav>
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">Menu</a></li>
                    <li><a href="#">About</a></li>
                    <li><a href="#">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <h1>Extraordinary Experience</h1>
        <p>Discover our chef's seasonal creations crafted from the finest locally-sourced ingredients for a truly unforgettable dining experience.</p>
        <a href="#" class="btn">Explore Our Menu</a>
    </section>

    <!-- Featured Dishes -->
    <section class="featured">
        <h2 class="section-title">Our Signature Dishes</h2>
        <div class="dishes">
            <div class="dish">
                <img src="https://ik.imagekit.io/0tydz7atd/Pasta-pomodoro_.webp?updatedAt=1746159138325" alt="Pasta Dish">
                <div class="dish-info">
                    <h3>Artisanal Pasta Pomodoro</h3>
                    <p>House-made pasta tossed with San Marzano tomatoes, fresh basil, and aged Parmigiano-Reggiano.</p>
                    <div class="price">Rs.1,760</div>
                </div>
            </div>
            <div class="dish">
                <img src="https://ik.imagekit.io/0tydz7atd/grass-fed-ribeye-steak-scaled.jpeg?updatedAt=1746159261762" alt="Steak Dish">
                <div class="dish-info">
                    <h3>Grass-Fed Ribeye</h3>
                    <p>28-day aged prime cut served with truffle mashed potatoes and seasonal vegetables.</p>
                    <div class="price">Rs.3,360</div>
                </div>
            </div>
            <div class="dish">
                <img src="https://ik.imagekit.io/0tydz7atd/grilled-mediterranean-sea-bass-with-garlic-spinach-and-zucchini-noodles-bqubsZGieG.webp?updatedAt=1746159274858" alt="Seafood Dish">
                <div class="dish-info">
                    <h3>Mediterranean Sea Bass</h3>
                    <p>Sustainably caught sea bass with lemon herb butter, saffron risotto, and grilled asparagus.</p>
                    <div class="price">Rs.2,880</div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about">
        <div class="about-container">
            <img src="https://ik.imagekit.io/0tydz7atd/top-20-pure-vegetarian-restaurants-in-delhi-ncr.jpg?updatedAt=1746159579191" alt="Chef" class="about-img">
            <div class="about-info">
                <h2>Our Lemon Story</h2>
                <p>Founded in 2015, Culinary Bliss began with a simple mission: to create extraordinary dining experiences that celebrate the richness of local ingredients and the art of fine cooking.</p>
                <p>Our executive chef, with over 20 years of experience in renowned kitchens across Europe and Asia, brings a unique perspective to every dish, blending traditional techniques with modern innovation.</p>
                <p>We take pride in working directly with local farmers and artisans to source the freshest ingredients, ensuring that every plate tells a story of quality, sustainability, and passion.</p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-container">
            <div class="footer-section">
                <h3>Location</h3>
                <p>123 Gourmet Street</p>
                <p>Culinary District</p>
                <p>Foodie City, FC 12345</p>
            </div>
            <div class="footer-section">
                <h3>Hours</h3>
                <p>Monday - Thursday: 5pm - 10pm</p>
                <p>Friday - Saturday: 5pm - 11pm</p>
                <p>Sunday: 4pm - 9pm</p>
            </div>
            <div class="footer-section">
                <h3>Contact</h3>
                <p>Email: info@Lemon.com</p>
                <p>Phone: (123) 456-7890</p>
                <div class="social-icons">
                    <!-- Simple icons using text -->
                    <a href="#">FB</a>
                    <a href="#">IG</a>
                    <a href="#">TW</a>
                </div>
            </div>
        </div>
        <div class="copyright">
            &copy; 2025 Lemon res. All rights reserved.
        </div>
    </footer>
    </body>
    </html>

## OUTPUT:

![web 1st](https://github.com/user-attachments/assets/c81b22cd-ee08-48c0-8a1a-6bc79c38bd6f)
![web 2nd](https://github.com/user-attachments/assets/1a583ff0-c406-401d-9c9b-d4a23e3620c3)
![web 3rd](https://github.com/user-attachments/assets/2f27dc4f-3908-4d83-a0bb-da36884d37b1)




## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
