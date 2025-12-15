<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <title>Aastha K Thakkar - Portfolio</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>

    <link href="https://fonts.googleapis.com/css2?family=Livvic:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

    <style>
        :root{
            --text-main:   #3B2A1B;  /* the brown you like */
            --accent-gold: #C9A24D;  /* only for button / icon */

            --bg-page:     #FBF7F2;
            --bg-section:  #F5EEE6;
            --card-bg:     #FFFFFF;
            --soft-surface:#F3ECE2;
            --band-bg:     #DED2C5;
            --border-soft: #E0D3C3;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Livvic', system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            line-height: 1.6;
            color: var(--text-main);
            background: var(--bg-page);
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255,255,255,0.97);
            padding: 20px 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            z-index: 1000;
        }
        nav .container {
            max-width: 1200px;	
            margin: 0 auto;
            padding: 0 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        nav .logo {
            font-size: 22px;
            font-weight: 600;
            letter-spacing: 1px;
            color: var(--text-main);
        }
        nav ul { list-style: none; display:flex; gap:35px; }

        nav a {
            text-decoration:none;
            color: var(--text-main);
            font-size:14px;
            letter-spacing:1px;
            font-weight:700;
            text-transform:none;
            transition: text-decoration-color .3s;
        }
        nav a:hover {
            text-decoration: underline;
            text-decoration-thickness: 1px;
            text-underline-offset: 4px;
        }

        /* Hero Section */
        .hero {
            margin-top: 80px;
            padding: 100px 40px;
            text-align:center;
            background: linear-gradient(135deg,#F4EEE4 0%,#FFFFFF 100%);
        }
        .hero h1 {
            font-size:48px;
            font-weight:300;
            margin-bottom:15px;
            color:var(--text-main);
            letter-spacing:2px;
        }
        .hero .title {
            font-size:20px;
            color:var(--text-main);
            margin-bottom:40px;
            font-weight:400;
            letter-spacing:1px;
        }
        .hero .stats {
            display:flex;
            justify-content:center;
            gap:60px;
            margin-top:50px;
            flex-wrap:wrap;
        }
        .hero .stat .number {
            font-size:36px;
            font-weight:600;
            color:var(--text-main);
        }
        .hero .stat .label {
            font-size:14px;
            color:var(--text-main);
            text-transform:uppercase;
            letter-spacing:1px;
            margin-top:5px;
        }

        /* ABOUT */
        .about {
            max-width: 1100px;
            margin: 80px auto;
            padding: 0 40px;
        }
        .about-grid {
            display: grid;
            grid-template-columns: 380px 1fr;
            gap: 28px;
            align-items: center;
        }
        .about-photo {
            width: 100%;
            display:flex;
            align-items:center;
            justify-content:center;
        }
        .about-photo .photo-wrap {
            width: 100%;
            max-width: 380px;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 14px 40px rgba(0,0,0,0.08);
            background: var(--card-bg);
        }
        .about-photo img {
            display:block;
            width:100%;
            height:100%;
            object-fit:cover;
            aspect-ratio: 3 / 4;
        }
        .about-content { padding: 12px 0; }
        .about h2 {
            font-size:36px;
            font-weight:300;
            margin-bottom:16px;
            color:var(--text-main);
            letter-spacing:1.5px;
        }
        .about p {
            font-size:16px;
            line-height:1.8;
            color:var(--text-main);
            margin-bottom:14px;
        }
        .about .highlight {
            color:var(--text-main);
            font-weight:700;
        }

        /* Sections */
        section { padding: 90px 40px; }

        /* Services Section (cards) */
        .services { background:var(--bg-section); }
        .services h2 {
            text-align:center;
            font-size:36px;
            font-weight:300;
            margin-bottom:60px;
            color:var(--text-main);
            letter-spacing:1.5px;
        }

        .services-grid{
            max-width:1200px;
            margin:auto;
            display:grid;
            grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
            gap:40px;
        }
        .service-card{
            background:var(--card-bg);
            position:relative;
            height:260px;
            cursor:pointer;
            overflow:hidden;
            border-radius:16px;
            box-shadow:0 18px 45px rgba(0,0,0,.08);
            transition:.4s;
        }
        .service-card:hover{transform:translateY(-6px);}
        .service-card img{
            width:100%;
            height:100%;
            object-fit:cover;
            transition:.45s;
            display:block;
        }
        .service-card:hover img{transform:scale(1.04);}
        .band{
            position:absolute;
            bottom:0;
            width:100%;
            background:var(--band-bg);
            color:var(--text-main);
            padding:18px;
            text-align:center;
            font-weight:800;
            letter-spacing:1px;
            border-bottom-left-radius:16px;
            border-bottom-right-radius:16px;
        }

        /* Contact form block */
        .contact-form-block {
            max-width: 1000px;
            margin: 0 auto 80px;
            padding: 60px 20px 0;
            text-align: center;
        }
        .contact-form-sub {
            color: var(--text-main);
            margin-bottom: 24px;
        }
        .contact-form-email {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 30px;
            padding: 10px 18px;
            border-radius: 999px;
            background: var(--soft-surface);
            border: 1px solid var(--border-soft);
        }
        .contact-form-email .icon-wrap {
            width: 28px;
            height: 28px;
            border-radius: 50%;
            background: var(--accent-gold);
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .contact-form-email a {
            font-size: 14px;
            text-decoration: none;
            color: var(--text-main);
            font-weight: 500;
        }
        .contact-form-grid {
            max-width: 900px;
            margin: 0 auto 40px;
            display: grid;
            grid-template-columns: repeat(2, minmax(0, 1fr));
            gap: 16px 20px;
        }
        .contact-form-grid .full { grid-column: 1 / -1; }
        .contact-form-grid input,
        .contact-form-grid textarea {
            width: 100%;
            border: 1px solid var(--border-soft);
            padding: 14px 16px;
            background: var(--soft-surface);
            font-family: 'Livvic', system-ui, sans-serif;
            font-size: 14px;
            color: var(--text-main);
            outline: none;
        }
        .contact-form-grid textarea { min-height: 160px; resize: vertical; }
        .submit-row button {
            padding: 12px 26px;
            border-radius: 999px;
            border: none;
            background: var(--accent-gold);
            color: #fff;
            font-weight: 600;
            letter-spacing: 0.5px;
            cursor: pointer;
            transition: background .3s, transform .2s;
        }
        .submit-row button:hover {
            background: #B48C35;
            transform: translateY(-1px);
        }

        /* CTA Section */
        .cta {
            text-align: center;
            padding: 80px 40px;
            background: var(--bg-section);
            color: var(--text-main);
        }
        .cta h2 {
            font-size: 36px;
            font-weight: 300;
            margin-bottom: 0;
            letter-spacing: 1.5px;
        }

        /* Footer */
        footer {
            text-align:center;
            padding:40px;
            background: var(--bg-section);
            color:var(--text-main);
            font-size:14px;
        }

        /* ===== Service gallery modal ===== */
        .service-modal-overlay{
            position:fixed;
            inset:0;
            background:rgba(0,0,0,.7);
            display:none;
            align-items:center;
            justify-content:center;
            z-index:5000;
        }
        .service-modal-overlay.open{display:flex;}

        .service-modal{
            background:transparent;
            padding:0;
            border-radius:0;
            max-width:1100px;
            width:100%;
            max-height:90vh;
            position:relative;
            display:flex;
            align-items:center;
            justify-content:center;
        }

        .service-modal-close{
            position:absolute;
            top:10px;
            right:10px;
            border:none;
            width:30px;
            height:30px;
            border-radius:50%;
            cursor:pointer;
            font-size:18px;
            z-index:10;
            background:#fff;
        }

        .service-modal-image-wrap{
            width:100%;
            max-width:950px;
            max-height:78vh;
            overflow:hidden;
            border-radius:12px;
            background:#fff;
            padding:10px;
        }
        .service-modal-image-wrap img{
            width:100%;
            height:100%;
            object-fit:contain;
            display:block;
            cursor:pointer; /* so people know it's clickable to IG */
        }

        .arrow{
            position:absolute;
            top:50%;
            transform:translateY(-50%);
            background:rgba(0,0,0,.4);
            color:#fff;
            border:none;
            width:36px;
            height:36px;
            border-radius:50%;
            cursor:pointer;
            font-size:20px;
        }
        .arrow.left{left:20px;}
        .arrow.right{right:20px;}

        .caption{
            text-align:center;
            color:#fff;
            margin-top:12px;
            font-size:14px;
        }

        /* Responsive */
        @media (max-width: 1000px) {
            .about-grid { grid-template-columns: 1fr; }
            .services-grid { grid-template-columns: repeat(2,1fr); }
        }
        @media (max-width: 768px) {
            nav ul { display:none; }
            .hero h1 { font-size:32px; }
            .hero .title { font-size:16px; }
            .services-grid { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="container">
            <div class="logo">AASTHA K THAKKAR</div>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero -->
    <section class="hero" id="home">
        <h1>AASTHA K THAKKAR</h1>
        <p class="title">Luxury Social Media & Brand Experience Specialist</p>
        <div class="stats">
            <div class="stat">
                <div class="number"><span class="count" data-target="40">0</span>+</div>
                <div class="label">Brands</div>
            </div>
            <div class="stat">
                <div class="number"><span class="count" data-target="5">0</span>+</div>
                <div class="label">Industries</div>
            </div>
            <div class="stat">
                <div class="number"><span class="count" data-target="100">0</span>%</div>
                <div class="label">Dedication</div>
            </div>
        </div>
    </section>

    <!-- About -->
    <section class="about" id="about">
        <div class="about-grid">
            <div class="about-photo">
                <div class="photo-wrap">
                    <img src="Aastha.jpg" alt="Aastha Thakkar">
                </div>
            </div>
            <div class="about-content">
                <h2>About Me</h2>
                <p>I am a <span class="highlight">Social Media & Creative Strategy Specialist</span> with experience across 40+ brands in jewellery, fashion, lifestyle, wellness, and F&amp;B.</p>
                <p>My work spans end-to-end brand presence — from social media management and content strategy to model shoots, UGC/EGC production, influencer marketing and celebrity collaborations.</p>
                <p>I've led store launches, exhibition setups, and high-end shoots that shape a brand's visual identity and digital performance. My approach blends clean aesthetics with strategic storytelling, helping premium brands look elevated, cohesive and impactful online.</p>
            </div>
        </div>
    </section>

    <!-- Services -->
    <section class="services" id="services">
        <h2>My Creative Space</h2>
        <div class="services-grid">

            <!-- Social Media Management (image slider) -->
            <div class="service-card"
                 data-images="Vaarahi Silks.jpg,Tyohaar.jpg,Monginis.jpg,TBI.jpg,Neelkanth Jewellers.jpg,Zola Fahions.jpg,Harvard University.jpg,Sparkling Gold.jpg">
                <img src="Vaarahi Silks.jpg" alt="Social Media Management">
                <div class="band">Social Media Management</div>
            </div>

            <!-- Model & Celebrity Shoots--> 
            <div class="service-card"
			                 data-images="Alicia Kaur.jpg,Neetti Ateliier.jpg,Tyohaar Ms.jpg,MK Jewels.jpg,Neelkanth MS.jpg,Sunil Gold.jpg">
                <img src= "Alicia Kaur.jpg", " alt="Model & Celebrity Shoots">
                <div class="band">Model & Celebrity Shoots</div>
            </div>

            <div class="service-card"
     data-images="CC 1.jpg,CC  2.jpg,CC 3.jpg">
    <img src="CC 1.jpg" alt="Content Creation">
    <div class="band">Content Creation</div>
</div>



        </div>
    </section>

    <!-- Contact form block -->
    <section class="contact-form-block" id="contact">
        <p class="contact-form-sub">
           Let’s collaborate and build something impactful together.
        </p>

        <div class="contact-form-email">
            <div class="icon-wrap">
                <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <rect x="3" y="5" width="18" height="14" rx="2" stroke-width="1.6" stroke="currentColor"/>
                    <path d="M4 7l8 6 8-6" stroke-width="1.6" stroke="currentColor" />
                </svg>
            </div>
            <div>
                <a href="mailto:aasthathakkar107@gmail.com">aasthathakkar107@gmail.com</a>
            </div>
        </div>

        <form class="contact-form-grid">
            <input type="text" placeholder="Your Name">
            <input type="email" placeholder="Your Email">
            <input type="text" placeholder="Subject">
            <input type="tel" placeholder="Contact Phone">
            <textarea class="full" placeholder="Message"></textarea>
        </form>

        <div class="submit-row">
            <button type="submit">Send Message</button>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="cta" aria-hidden="true">
        <h2>Let's Create Something Beautiful</h2>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2024 Aastha K Thakkar. All rights reserved. • Email: aasthathakkar107@gmail.com </p>
    </footer>

    <!-- Service Slider Modal -->
    <div class="service-modal-overlay" id="sliderModal">
      <div class="service-modal">
        <button class="service-modal-close" id="closeSlider">×</button>
        <button class="arrow left" id="prevBtn">&#8249;</button>
        <button class="arrow right" id="nextBtn">&#8250;</button>

        <div class="service-modal-image-wrap">
          <img id="sliderImage" src="" alt="">
        </div>

        <div class="caption" id="sliderCaption"></div>
      </div>
    </div>

    <script>
        // Service cards: open IG if data-ig exists, else open slider.
        // Slider also supports per-slide Instagram links via data-igs.
        (function() {
            const cards = document.querySelectorAll('.service-card');
            const modal = document.getElementById('sliderModal');
            const img = document.getElementById('sliderImage');
            const caption = document.getElementById('sliderCaption');
            const closeBtn = document.getElementById('closeSlider');
            const prev = document.getElementById('prevBtn');
            const next = document.getElementById('nextBtn');

            let images = [];
            let igLinks = [];
            let index = 0;

            cards.forEach(card => {
              card.addEventListener('click', () => {
                const cardIg = card.dataset.ig && card.dataset.ig.trim();
                if (cardIg) {
                    window.open(cardIg, '_blank', 'noopener');
                    return;
                }

                images = (card.dataset.images || '')
                  .split(',')
                  .map(s => s.trim())
                  .filter(Boolean);

                igLinks = (card.dataset.igs || '')
                  .split(',')
                  .map(s => s.trim());

                if (!images.length) return;

                index = 0;
                showImage();
                modal.classList.add('open');
              });
            });

            function showImage(){
              img.src = images[index];
              caption.innerHTML = (index + 1) + ' / ' + images.length;
            }

            // Clicking image in slider opens per-slide IG link (if present)
            img.addEventListener('click', () => {
              const link = igLinks[index];
              if (link) {
                window.open(link, '_blank', 'noopener');
              }
            });

            prev.addEventListener('click', (e) => {
              e.stopPropagation();
              if (!images.length) return;
              index = (index - 1 + images.length) % images.length;
              showImage();
            });

            next.addEventListener('click', (e) => {
              e.stopPropagation();
              if (!images.length) return;
              index = (index + 1) % images.length;
              showImage();
            });

            closeBtn.addEventListener('click', () => {
              modal.classList.remove('open');
            });

            modal.addEventListener('click', (e) => {
              if (e.target === modal) {
                modal.classList.remove('open');
              }
            });
        })();

        // Hero stats animated counters
        (function () {
          const statsSection = document.querySelector('.hero .stats');
          if (!statsSection) return;

          const counters = statsSection.querySelectorAll('.count');
          let hasRun = false;

          function animateCounter(el, target, duration) {
            const startTime = performance.now();

            function update(now) {
              const progress = Math.min((now - startTime) / duration, 1);
              const value = Math.floor(target * progress);
              el.textContent = value;
              if (progress < 1) requestAnimationFrame(update);
            }

            requestAnimationFrame(update);
          }

          const observer = new IntersectionObserver(
            (entries) => {
              entries.forEach((entry) => {
                if (entry.isIntersecting && !hasRun) {
                  hasRun = true;
                  counters.forEach((counter) => {
                    const target = parseInt(counter.dataset.target, 10) || 0;
                    animateCounter(counter, target, 1200);
                  });
                  observer.unobserve(statsSection);
                }
              });
            },
            { threshold: 0.5 }
          );

          observer.observe(statsSection);
        })();
    </script>
</body>
</html>
