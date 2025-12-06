<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>flavin jaiker - Personal Profile</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700&family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link rel="stylesheet" href="css/style.css">
    <link rel="stylesheet" href="css/animations.css">
</head>
<body>
    <header class="hero-section">
        <div class="container hero-content">
            <div class="hero-text">
                <h1 class="fade-in-up">flavin jaiker</h1>
                <p class="fade-in-up delay-1">Age: 19</p>
                <p class="bio fade-in-up delay-2">
                    A passionate and energetic individual constantly exploring new technologies and creative challenges. 
                    I thrive on learning and building, always seeking opportunities to innovate and make a positive impact.
                </p>
                <div class="social-links fade-in-up delay-3">
                    <a href="#" target="_blank" aria-label="LinkedIn"><i class="fab fa-linkedin"></i></a>
                    <a href="#" target="_blank" aria-label="GitHub"><i class="fab fa-github"></i></a>
                    <a href="#" target="_blank" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
                    <a href="https://www.instagram.com/fantastic_flavin_007/" target="_blank" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
                </div>
            </div>
            <div class="hero-image-container fade-in-right">
                <img src="img/image.png" alt="Derek Ronald's Professional Photo" class="profile-photo">
                <div class="photo-overlay"></div>
            </div>
        </div>
    </header>

    <main>
        <section class="section about-me">
            <div class="container reveal">
                <h2 class="section-title">About Me</h2>
                <p>
                    I'm a keen enthusiast in web development, constantly honing my skills in front-end technologies like React and Vue, and dabbling in back-end with Node.js. Beyond coding, I love playing basketball, exploring new music, and diving into sci-fi novels. I believe in continuous self-improvement and embracing challenges.
                </p>
            </div>
        </section>

        <section class="section skills-interests bg-gradient-light">
            <div class="container reveal">
                <h2 class="section-title">Skills & Interests</h2>
                <div class="content-grid">
                    <div class="card glassmorphism hover-grow">
                        <h3>Skills</h3>
                        <ul>
                            <li>Web Development (HTML, CSS, JavaScript)</li>
                            <li>Front-end Frameworks (React, Vue.js - basic)</li>
                            <li>UI/UX Design Principles</li>
                            <li>Problem Solving</li>
                            <li>Version Control (Git)</li>
                        </ul>
                    </div>
                    <div class="card glassmorphism hover-grow">
                        <h3>Interests</h3>
                        <ul>
                            <li>Basketball & Sports Analytics</li>
                            <li>Electronic Music Production</li>
                            <li>Science Fiction Literature</li>
                            <li>Coding Challenges</li>
                            <li>Learning New Languages</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact section with EmailJS form -->
        <section class="section contact">
            <div class="container reveal">
                <h2 class="section-title">Get in Touch</h2>
                <p>I'm always open to connecting and discussing new ideas or opportunities. Feel free to reach out!</p>

                <form id="contactForm">
                    <input type="text" name="name" id="name" placeholder="Your Name *" required>
                    <input type="email" name="email" id="email" placeholder="Your Email *" required>
                    <input type="text" name="title" id="title" placeholder="Subject *" required>
                    <textarea name="message" id="message" placeholder="Your Message *" rows="5" required></textarea>
                    <button type="submit" class="btn primary-btn hover-swing">Send Message</button>
                </form>

                <p id="formStatus"></p>
            </div>
        </section>
    </main>

    <footer class="footer">
        <div class="container">
            <p>&copy; <span id="current-year"></span> Derek Ronald. All rights reserved.</p>
        </div>
    </footer>

    <script src="js/main.js"></script>

    <!-- EmailJS scripts -->
    <script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>
    <script>
      (function() {
        emailjs.init({
          publicKey: "MfTzm2fHCZ2WX0B_r"  // Public Key
        });
      })();

      const form = document.getElementById('contactForm');
      const statusEl = document.getElementById('formStatus');

      form.addEventListener('submit', function(e) {
        e.preventDefault();
        statusEl.textContent = "Sending...";

        emailjs.sendForm(
          "service_djxirt5",    // Service ID
          "template_6yyqdju",   // Template ID
          "#contactForm"
        ).then(() => {
          statusEl.textContent = "Message sent successfully! ✅";
          form.reset();
        }).catch((error) => {
          console.log(error);
          statusEl.textContent = "Failed to send. Please try again.";
        });
      });
    </script>
</body>
</html>
