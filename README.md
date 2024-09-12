<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Riverstone Cottages - Your Perfect Coastal Retreat</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap');

        :root {
            --primary-color: #1a5f7a;
            --secondary-color: #57c5b6;
            --accent-color: #159895;
            --background-color: #f8f9fa;
            --text-color: #333;
            --light-text: #ffffff;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            background-color: var(--background-color);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        header {
            background-color: var(--primary-color);
            color: var(--light-text);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            z-index: 1000;
            transition: background-color 0.8s ease;
        }

        header.scrolled {
            background-color: rgba(26, 95, 122, 0.9);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .logo-container {
            display: flex;
            align-items: center;
        }

        .logo-container img {
            width: 80px;
            height: 80px;
            margin-right: 1rem;
        }

        .site-title {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--light-text);
        }

        nav ul {
            display: flex;
            list-style: none;
            margin: 0;
            padding: 0;
        }

        nav ul li {
            margin-left: 2rem;
        }

        nav a {
            color: var(--light-text);
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: var(--secondary-color);
        }

        .btn {
            background-color: var(--accent-color);
            color: var(--light-text);
            padding: 0.75rem 1.5rem;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s, transform 0.2s;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            

        }

        .btn:hover {
            background-color: var(--secondary-color);
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .hero {
            background-image: url('https://www.vrbo.com/en-ca/vacation-ideas/wp-content/uploads/3m3M7LTP806EuWJihdKwKj/f929bbba3cb3ab01482b53070668f67e/cottage-country-canada.png');
            background-size: cover;
            background-position: center;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: var(--light-text);
            position: relative;
            overflow: hidden;
            animation: zoomInOut 20s ease infinite;
        }

        @keyframes zoomInOut {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.5);
        }

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            padding: 2rem;
            animation: fadeIn 1s ease-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }

        .hero p {
            font-size: 1.4rem;
            margin-bottom: 2rem;
        }

        .cottages {
            padding: 6rem 0;
            background-color: var(--background-color);
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 3rem;
        }

        .cottage-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .cottage-card {
            background-color: #ffffff;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .cottage-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }

        .cottage-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .cottage-card-content {
            padding: 1.5rem;
        }

        .cottage-card h3 {
            font-size: 1.5rem;
            color: var(--primary-color);
            margin-bottom: 0.5rem;
        }

        .cottage-card p {
            color: var(--text-color);
            margin-bottom: 0.5rem;
        }

        .star {
            color: #ffd700;
        }

        .about {
            background-color: var(--primary-color);
            color: var(--light-text);
            padding: 6rem 0;
            text-align: center;
        }

        .about p {
            max-width: 800px;
            margin: 0 auto 2rem;
            font-size: 1.2rem;
        }

        .contact {
            padding: 6rem 0;
            background-color: var(--background-color);
        }

        .contact-info {
            background-color: #ffffff;
            border-radius: 10px;
            padding: 2rem;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 2rem;
        }

        .contact-details, .office-hours {
            padding: 1rem;
        }

        .contact-details h3, .office-hours h3 {
            color: var(--primary-color);
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
        }

        .contact-item i {
            color: var(--accent-color);
            margin-right: 1rem;
            font-size: 1.2rem;
        }

        .office-hours ul {
            list-style-type: none;
        }

        .office-hours li {
            margin-bottom: 0.5rem;
        }

        footer {
            background-color: var(--primary-color);
            color: var(--light-text);
            text-align: center;
            padding: 2rem 0;
        }

        .social-icons {
            margin-top: 1rem;
        }

        .social-icons a {
            color: var(--light-text);
            font-size: 1.5rem;
            margin: 0 0.5rem;
            transition: color 0.3s ease;
        }

        .social-icons a:hover {
            color: var(--secondary-color);
        }

        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                align-items: flex-start;
            }

            nav ul {
                margin-top: 1rem;
            }

            nav ul li {
                margin-left: 0;
                margin-right: 1rem;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero p {
                font-size: 1.2rem;
            }

            .contact-info {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-container">
            <div class="logo-container">
                <a href="#home"><img src="./WhatsApp_Image_2024-09-11_at_13.59.48_4f2b6029-removebg-preview.png" alt="Riverstone Cottages Logo"></a>
                <span class="site-title">Riverstone Cottages</span>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#cottages">Cottages</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main>
        <section id="home" class="hero">
            <div class="hero-content">
                <h1>Discover Your Perfect <span style="color: var(--secondary-color);">Coastal Retreat</span></h1>
                <p>Experience the beauty and tranquility of our handpicked seaside cottages</p>
                <a href="#cottages"><button class="btn">Find Your Stay</button></a>
            </div>
        </section>

        <section id="cottages" class="cottages">
            <div class="container">
                <h2 class="section-title">Our Cozy Cottages</h2>
                <div class="cottage-grid">
                    <div class="cottage-card">
                        <img src="https://i.pinimg.com/736x/58/79/50/58795085feb803ecb79eb817e268b1a0.jpg" alt="Rustic Cove">
                        <div class="cottage-card-content">
                            <h3>Rustic Cove</h3>
                            <p>Stunning ocean views</p>
                            <p>Coastal Village, UK</p>
                            <p>
                                <span class="star">★★★★★</span>
                                4.8 (120 reviews)
                            </p>
                            <button class="btn">View Details</button>
                        </div>
                    </div>
                    <div class="cottage-card">
                        <img src="https://i.pinimg.com/736x/58/79/50/58795085feb803ecb79eb817e268b1a0.jpg" alt="Vintage Retreat">
                        <div class="cottage-card-content">
                            <h3>Vintage Retreat</h3>
                            <p>Perched on scenic cliffs</p>
                            <p>Rocky Bay, UK</p>
                            <p>
                                <span class="star">★★★★★</span>
                                4.9 (95 reviews)
                            </p>
                            <button class="btn">View Details</button>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="about" class="about">
            <div class="container">
                <h2 class="section-title">About Riverstone Cottages</h2>
                <p>At Riverstone Cottages, we're passionate about providing unique coastal experiences. Whether you're looking for a romantic getaway or a family adventure, our carefully curated selection of cottages offers the perfect backdrop for your seaside memories.</p>
                <button class="btn">Learn More</button>
            </div>
        </section>

        <section id="contact" class="contact">
            <div class="container">
                <h2 class="section-title">Get in Touch</h2>
                <div class="contact-info">
                    <div class="contact-details">
                        <h3>Contact Information</h3>
                        <div class="contact-item">
                            <i class="fas fa-phone"></i>
                            <p>+44 123 456 7890</p>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-envelope"></i>
                            <p>info@cozycottages.com</p>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-map-marker-alt"></i>
                            <p>123 Seaside Avenue, Coastal Town, CT1 2AB</p>
                        </div>
                    </div>
                    <div class="office-hours">
                        <h3>Office Hours</h3>
                        <ul>
                            <li><i class="far fa-clock"></i> Monday - Friday: 9am - 5pm</li>
                            <li><i class="far fa-clock"></i> Saturday: 10am - 2pm</li>
                            <li><i class="far fa-clock"></i> Sunday: Closed</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <p>&copy; 2023 Riverstone Cottages. All rights reserved.</p>
            <div class="social-icons">
                <a href="#" aria-label="Facebook"><i class="fab fa-facebook"></i></a>
                <a href="#" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
                <a href="#" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
            </div>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const header = document.querySelector('header');
            const bookBtn = document.querySelector('.hero .btn');
            const viewDetailsBtns = document.querySelectorAll('.cottage-card .btn');
            const learnMoreBtn = document.querySelector('.about .btn');

            window.addEventListener('scroll', function() {
                if (window.scrollY > 50) {
                    header.classList.add('scrolled');
                } else {
                    header.classList.remove('scrolled');
                }
            });

            // bookBtn.addEventListener('click', function() {
            //     alert('Booking functionality coming soon!');
            // });

            viewDetailsBtns.forEach(btn => {
                btn.addEventListener('click', function() {
                    const cottageName = this.closest('.cottage-card').querySelector('h3').textContent;
                    alert(`You're viewing details for ${cottageName}. Full details coming soon!`);
                });
            });

            learnMoreBtn.addEventListener('click', function() {
                alert('More information about Riverstone Cottages coming soon!');
            });
        });
    </script>
</body>
</html>
