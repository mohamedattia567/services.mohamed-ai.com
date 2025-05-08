<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Mohamed Ai Services</title>
  <style>
    html, body {
      height: 100%;
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
      display: flex;
      flex-direction: column;
    }
    body {
      min-height: 100vh;
      box-sizing: border-box;
    }
    #page-wrapper {
      flex: 1;
      display: flex;
      flex-direction: column;
      max-width: 1200px;
      width: 100%;
      margin: 0 auto;
    }
    header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      background-color: #007BFF;
      color: white;
      padding: 20px 40px;
      box-sizing: border-box;
      box-shadow: 0 2px 6px rgba(0,0,0,0.2);
      user-select: none;
    }
    .header-left {
      display: flex;
      align-items: center;
      gap: 15px;
    }
    .header-left img {
      height: 50px;
      width: 50px;
      border-radius: 50%;
      object-fit: cover;
      border: 2px solid white;
    }
    header h1 {
      margin: 0;
      font-size: 1.8rem;
    }
    nav {
      display: flex;
      gap: 30px;
    }
    nav a {
      color: white;
      text-decoration: none;
      cursor: pointer;
      font-weight: bold;
      font-size: 1.1rem;
      transition: color 0.3s ease;
    }
    nav a:hover {
      color: #ddd;
    }
    main {
      flex: 1;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 20px;
      box-sizing: border-box;
      background-color: #f4f4f4;
    }
    .services {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 20px;
      width: 100%;
      max-width: 900px;
    }
    .service-card {
      background: white;
      border: 1px solid #ccc;
      border-radius: 8px;
      padding: 10px;
      text-align: center;
      cursor: pointer;
      transition: transform 0.2s;
      user-select: none;
    }
    .service-card:hover {
      transform: scale(1.05);
      box-shadow: 0 0 8px rgba(0,0,0,0.15);
    }
    .service-card img {
      width: 100%;
      height: 100px;
      object-fit: cover;
      border-radius: 6px;
    }
    .service-card h3 {
      margin: 10px 0 5px 0;
    }
    .service-card p {
      margin: 0;
      color: #444;
      font-weight: bold;
    }
    footer {
      background-color: #007BFF;
      color: white;
      font-weight: bold;
      padding: 20px 40px;
      box-sizing: border-box;
      box-shadow: 0 -2px 6px rgba(0,0,0,0.2);
      font-size: 1rem;
      user-select: none;
      text-align: left;
      max-width: 1200px;
      width: 100%;
      margin: 0 auto;
    }
    /* Responsive adjustments */
    @media (max-width: 800px) {
      nav {
        gap: 15px;
      }
      footer, header {
        padding: 15px 20px;
      }
      .services {
        max-width: 100%;
      }
    }
  </style>
</head>
<body>
  <div id="page-wrapper">
    <header>
      <div class="header-left">
        <img src="your-profile-image.jpg" alt="Profile Image" />
        <h1>Mohamed Ai Services</h1>
      </div>
      <nav>
        <a onclick="showHome()">Home</a>
        <a onclick="showContact()">Contact Me</a>
      </nav>
    </header>

    <main>
      <div class="services" id="services">
        <div class="service-card" tabindex="0" onclick="openServiceModal('Service 1')">
          <img src="service1-image.jpg" alt="Service 1" />
          <h3>Service 1</h3>
          <p>$100</p>
        </div>
        <div class="service-card" tabindex="0" onclick="openServiceModal('Service 2')">
          <img src="service2-image.jpg" alt="Service 2" />
          <h3>Service 2</h3>
          <p>$150</p>
        </div>
        <div class="service-card" tabindex="0" onclick="openServiceModal('Service 3')">
          <img src="service3-image.jpg" alt="Service 3" />
          <h3>Service 3</h3>
          <p>$99</p>
        </div>
        <div class="service-card" tabindex="0" onclick="openServiceModal('Service 4')">
          <img src="service4-image.jpg" alt="Service 4" />
          <h3>Service 4</h3>
          <p>$200</p>
        </div>
        <div class="service-card" tabindex="0" onclick="openServiceModal('Service 5')">
          <img src="service5-image.jpg" alt="Service 5" />
          <h3>Service 5</h3>
          <p>$120</p>
        </div>
        <div class="service-card" tabindex="0" onclick="openServiceModal('Service 6')">
          <img src="service6-image.jpg" alt="Service 6" />
          <h3>Service 6</h3>
          <p>$180</p>
        </div>
      </div>
    </main>

    <footer>
      &copy; 2025 Mohamed Ai Services . All rights reserved.
    </footer>
  </div>

  <!-- Modal and other scripts omitted for brevity - you can include them as needed -->

  <script>
    // These functions come from previous code and can be included if you want the service modal and contact form
    function showHome() {
      document.getElementById('services').style.display = 'grid';
    }
    function showContact() {
      // No contact form in this layout
      alert('يرجى تعديل الكود لإضافة صفحة الاتصال إذا رغبت بذلك.');
    }
    function openServiceModal(serviceName) {
      alert('عرض تفاصيل الخدمة: ' + serviceName);
      // Implement modal or details as needed
    }
  </script>
</body>
</html>
</content>
</create_file>

