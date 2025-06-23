<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Skip - Business Contact Page</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Montserrat:wght@700;800&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #1c2c20;
            --secondary: #2c3e50;
            --accent: #4cc9f0;
            --light: #f8f9fa;
            --dark: #39424b;
            --success: #9ff3be;
            --warning: #facc15;
            --danger: #f87101;
            --transition: all 0.3s ease;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: white;
            background: linear-gradient(rgba(28, 44, 32, 0.9), rgba(28, 44, 32, 0.9)), 
                        url('https://images.unsplash.com/photo-1497215728101-856f4ea42174?ixlib=rb-4.0.3&auto=format&fit=crop&w=1470&q=80') no-repeat center center/cover;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            overflow-x: hidden;
            position: relative;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            z-index: 2;
            position: relative;
        }

        /* Header */
        header {
            padding: 1.5rem 0;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 800;
            display: flex;
            align-items: center;
            color: white;
        }

        .logo i {
            margin-right: 10px;
            color: var(--accent);
        }

        /* Hero Section */
        .hero {
            flex: 1;
            display: flex;
            align-items: center;
            padding: 40px 0;
            text-align: center;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }

        .hero h1 {
            font-family: 'Montserrat', sans-serif;
            font-size: 4rem;
            margin-bottom: 1rem;
            text-transform: uppercase;
            letter-spacing: 3px;
            text-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
        }

        .hero h2 {
            font-size: 1.8rem;
            margin-bottom: 2rem;
            font-weight: 400;
            color: rgba(255, 255, 255, 0.9);
        }

        .tagline {
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto 40px;
            color: rgba(255, 255, 255, 0.85);
            background: rgba(0, 0, 0, 0.2);
            padding: 15px;
            border-radius: 10px;
            backdrop-filter: blur(5px);
        }

        /* Contact Cards */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            max-width: 1000px;
            margin: 0 auto;
        }

        .contact-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 30px;
            text-align: center;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.1);
            opacity: 0;
            transform: translateY(20px);
        }

        .contact-card.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .contact-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.15);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }

        .contact-icon {
            width: 80px;
            height: 80px;
            background: var(--primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            font-size: 2rem;
            color: white;
            transition: var(--transition);
        }

        .contact-card:hover .contact-icon {
            background: var(--accent);
            transform: scale(1.1);
        }

        .contact-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: white;
        }

        .contact-card p {
            color: rgba(255, 255, 255, 0.8);
            margin-bottom: 20px;
        }

        .contact-link {
            display: inline-block;
            padding: 10px 20px;
            background: rgba(255, 255, 255, 0.15);
            color: white;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
        }

        .contact-link:hover {
            background: var(--accent);
            transform: translateY(-3px);
        }

        /* Footer */
        footer {
            padding: 40px 0 20px;
            text-align: center;
            color: rgba(255, 255, 255, 0.7);
            margin-top: 40px;
        }

        .copyright {
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* Particles Background */
        #particles-js {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: 1;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 3rem;
            }
            
            .hero h2 {
                font-size: 1.5rem;
            }
            
            .contact-grid {
                grid-template-columns: 1fr;
                max-width: 400px;
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .logo {
                font-size: 1.5rem;
            }
            
            .contact-icon {
                width: 70px;
                height: 70px;
                font-size: 1.7rem;
            }
        }
    </style>
</head>
<body>
    <!-- Particles Background -->
    <div id="particles-js"></div>
    
    <!-- Header -->
    <header>
        <div class="container">
            <nav class="navbar">
                <div class="logo">
                    <i class="fas fa-palette"></i>
                    Skip
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Skip</h1>
                <h2>Ad in hand</h2>
                <p class="tagline">From business to brand — let's make it happent.</p>
                
                <div class="contact-grid">
                    <!-- Instagram Card -->
                    <div class="contact-card" id="card1">
                        <div class="contact-icon">
                            <i class="fab fa-instagram"></i>
                        </div>
                        <h3>Instagram</h3>
                        <p>Follow us for updates</p>
                        <a href="https://www.instagram.com/skipad1nhand/" class="contact-link" target="_blank">Visit</a>
                    </div>
                    
                    <!-- WhatsApp Card -->
                    <div class="contact-card" id="card2">
                        <div class="contact-icon">
                            <i class="fab fa-whatsapp"></i>
                        </div>
                        <h3>WhatsApp</h3>
                        <p>Chat with us directly</p>
                        <a href="https://wa.me/919709355498" class="contact-link" target="_blank">Message</a>
                    </div>
                    
                    <!-- Gmail Card -->
                    <div class="contact-card" id="card3">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <h3>Gmail</h3>
                        <p>Send us an email</p>
                        <a href="mailto:skipad1nhand@gmail.com" class="contact-link">Email Us</a>
                    </div>
                    
                    <!-- Website Card -->
                    <div class="contact-card" id="card4">
                        <div class="contact-icon">
                            <i class="fas fa-globe"></i>
                        </div>
                        <h3>Website</h3>
                        <p>Visit our online store</p>
                        <a href="https://theskip.myshopify.com" class="contact-link" target="_blank">Explore</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2023 Skip. All rights reserved.</p>
            <div class="copyright">
                <p>Designed with passion for creative solutions</p>
            </div>
        </div>
    </footer>

    <!-- Particles.js -->
    <script src="https://cdn.jsdelivr.net/particles.js/2.0.0/particles.min.js"></script>
    
    <script>
        // Initialize particles background
        particlesJS("particles-js", {
            particles: {
                number: { value: 30, density: { enable: true, value_area: 800 } },
                color: { value: "#4cc9f0" },
                shape: { type: "circle" },
                opacity: { value: 0.3, random: true },
                size: { value: 3, random: true },
                line_linked: {
                    enable: true,
                    distance: 150,
                    color: "#ffffff",
                    opacity: 0.1,
                    width: 1
                },
                move: {
                    enable: true,
                    speed: 1,
                    direction: "none",
                    random: true,
                    straight: false,
                    out_mode: "out",
                    bounce: false
                }
            },
            interactivity: {
                detect_on: "canvas",
                events: {
                    onhover: { enable: true, mode: "grab" },
                    onclick: { enable: true, mode: "push" },
                    resize: true
                }
            },
            retina_detect: true
        });

        // Simple animation on page load
        document.addEventListener('DOMContentLoaded', function() {
            // Animate the main heading
            const heading = document.querySelector('.hero h1');
            heading.style.transform = 'translateY(0)';
            heading.style.opacity = '1';
            
            // Animate tagline
            setTimeout(() => {
                const tagline = document.querySelector('.tagline');
                tagline.style.opacity = '1';
                tagline.style.transform = 'translateY(0)';
            }, 300);
            
            // Animate cards with delays
            const cards = document.querySelectorAll('.contact-card');
            cards.forEach((card, index) => {
                setTimeout(() => {
                    card.classList.add('visible');
                }, 500 + (index * 150));
            });
        });
        
        // Add click animation to cards
        document.querySelectorAll('.contact-card').forEach(card => {
            card.addEventListener('click', function() {
                this.style.transform = 'scale(0.95)';
                setTimeout(() => {
                    this.style.transform = '';
                }, 300);
            });
        });
    </script>
</body>
</html>
