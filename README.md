<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no" />
  <title>mohamedattia.com - Digital Services for Sale</title>
  <style>
    /* Import Google Font */
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap');

    /* Reset & base */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Poppins', sans-serif;
    }

    body {
      background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
      color: #fff;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 20px 15px;
      max-width: 350px;
      margin: 0 auto;
      user-select: none;
    }

    header {
      width: 100%;
      text-align: center;
      margin-bottom: 25px;
      border-bottom: 2px solid #39ff14;
      padding-bottom: 12px;
    }

    header h1 {
      font-weight: 600;
      font-size: 1.8rem;
      letter-spacing: 0.07em;
      color: #39ff14;
      text-shadow: 0 0 6px #39ff14, 0 0 10px #39ff14;
    }

    header p {
      font-weight: 300;
      font-size: 1rem;
      color: #a7d129;
      margin-top: 4px;
      font-style: italic;
    }

    main {
      width: 100%;
      flex-grow: 1;
    }

    .services-list {
      display: flex;
      flex-direction: column;
      gap: 16px;
    }

    .service-card {
      background: rgba(57, 255, 20, 0.1);
      border: 1.5px solid #39ff14;
      border-radius: 12px;
      padding: 16px 18px;
      transition: background 0.3s ease;
      cursor: pointer;
      box-shadow: 0 0 8px #39ff14a1;
    }

    .service-card:hover {
      background: rgba(57, 255, 20, 0.25);
      box-shadow: 0 0 15px #39ff14dd;
    }

    .service-title {
      font-size: 1.3rem;
      font-weight: 600;
      color: #eaffac;
      margin-bottom: 6px;
      text-shadow: 0 0 5px #39ff14bb;
    }

    .service-desc {
      font-weight: 300;
      font-size: 0.92rem;
      color: #c8f442;
      margin-bottom: 12px;
      min-height: 44px;
      line-height: 1.2em;
    }

    .service-price {
      font-weight: 600;
      font-size: 1.1rem;
      color: #39ff14;
      margin-bottom: 12px;
      text-shadow: 0 0 4px #39ff14aa;
    }

    .buy-btn {
      background: #39ff14;
      border: none;
      border-radius: 8px;
      padding: 8px 15px;
      font-weight: 600;
      font-size: 0.95rem;
      color: #0f2027;
      box-shadow: 0 0 8px #39ff14cc;
      transition: background 0.3s ease;
      width: 100%;
      cursor: pointer;
    }

    .buy-btn:hover {
      background: #a7d129;
      box-shadow: 0 0 15px #a7d129dd;
    }

    footer {
      margin-top: 30px;
      width: 100%;
      text-align: center;
      font-weight: 300;
      font-size: 0.85rem;
      color: #69f04ccc;
      border-top: 1px solid #39ff1477;
      padding-top: 10px;
      user-select: text;
    }

    /* Mobile fit for max-height 600px */
    @media (max-height: 600px) {
      body {
        padding: 15px 10px;
      }

      header h1 {
        font-size: 1.6rem;
      }

      .service-title {
        font-size: 1.15rem;
      }

      .service-desc {
        font-size: 0.85rem;
      }

      .service-price {
        font-size: 1rem;
      }

      .buy-btn {
        font-size: 0.9rem;
        padding: 7px 12px;
      }

      footer {
        font-size: 0.75rem;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>mohamedattia.com</h1>
    <p>Your Digital Services Marketplace</p>
  </header>

  <main>
    <section class="services-list">
      <!-- Service Card 1 -->
      <article class="service-card" tabindex="0" role="button" aria-pressed="false" onclick="buyService('Logo Design', 49)">
        <div class="service-title">Professional Logo Design</div>
        <div class="service-desc">Custom logos tailored for your brand identity to make it stand out.</div>
        <div class="service-price">$49</div>
        <button class="buy-btn" type="button" aria-label="Buy Professional Logo Design for 49 dollars">Buy Now</button>
      </article>

      <!-- Service Card 2 -->
      <article class="service-card" tabindex="0" role="button" aria-pressed="false" onclick="buyService('Website Development', 199)">
        <div class="service-title">Responsive Website Development</div>
        <div class="service-desc">Modern, mobile-friendly websites to showcase your business or portfolio.</div>
        <div class="service-price">$199</div>
        <button class="buy-btn" type="button" aria-label="Buy Responsive Website Development for 199 dollars">Buy Now</button>
      </article>

      <!-- Service Card 3 -->
      <article class="service-card" tabindex="0" role="button" aria-pressed="false" onclick="buyService('SEO Optimization', 99)">
        <div class="service-title">SEO Optimization</div>
        <div class="service-desc">Improve your search engine ranking and increase your site traffic organically.</div>
        <div class="service-price">$99</div>
        <button class="buy-btn" type="button" aria-label="Buy SEO Optimization for 99 dollars">Buy Now</button>
      </article>

      <!-- Service Card 4 -->
      <article class="service-card" tabindex="0" role="button" aria-pressed="false" onclick="buyService('Social Media Marketing', 149)">
        <div class="service-title">Social Media Marketing</div>
        <div class="service-desc">Boost your brand visibility and engage with your audience on social platforms.</div>
        <div class="service-price">$149</div>
        <button class="buy-btn" type="button" aria-label="Buy Social Media Marketing for 149 dollars">Buy Now</button>
      </article>

      <!-- Service Card 5 -->
      <article class="service-card" tabindex="0" role="button" aria-pressed="false" onclick="buyService('Ebook Writing', 89)">
        <div class="service-title">Ebook Writing</div>
        <div class="service-desc">Professional, well-researched ebooks to establish your authority and engage readers.</div>
        <div class="service-price">$89</div>
        <button class="buy-btn" type="button" aria-label="Buy Ebook Writing for 89 dollars">Buy Now</button>
      </article>
    </section>
  </main>

  <footer>
    &copy; <span id="year"></span> mohamedattia.com | Contact: info@mohamedattia.com
  </footer>

  <script>
    // Set current year in footer
    document.getElementById('year').textContent = new Date().getFullYear();

    // Buy button click handler
    function buyService(serviceName, price) {
      // Placeholder for actual payment or contact flow
      alert('Thank you for choosing "' + serviceName + '" for $' + price + '.\\nPlease contact info@mohamedattia.com to proceed with your order.');
    }

    // Allow keyboard accessibility for service cards
    const cards = document.querySelectorAll('.service-card');
    cards.forEach(card => {
      card.addEventListener('keydown', e => {
        if (e.key === 'Enter' || e.key === ' ') {
          e.preventDefault();
          const title = card.querySelector('.service-title').textContent;
          const priceText = card.querySelector('.service-price').textContent;
          const price = priceText.replace('$', '').trim();
          buyService(title, price);
        }
      });
    });
  </script>
</body>
</html>
</content>
</create_file>
# services.mohamed-ai.com
