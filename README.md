<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Mohamed Ai Services</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      display: flex;
      flex-direction: column;
      min-height: 100vh;
      align-items: center;
      background-color: #f4f4f4;
    }
    header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      width: 100%;
      max-width: 1200px;
      background-color: #007BFF;
      color: white;
      padding: 20px 40px;
      box-sizing: border-box;
      box-shadow: 0 2px 6px rgba(0,0,0,0.2);
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
      user-select: none;
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
      user-select: none;
    }
    nav a:hover {
      color: #ddd;
    }
    .container {
      display: flex;
      margin-top: 20px;
      width: 80%;
      max-width: 1200px;
      box-sizing: border-box;
      flex-grow: 1;
    }
    .profile {
      flex: 1;
      text-align: center;
    }
    .profile img {
      width: 200px;
      max-width: 100%;
      border-radius: 50%;
      object-fit: cover;
    }
    .main-content {
      flex: 2;
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    .services {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 20px;
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
    .contact-form {
      display: none;
      flex-direction: column;
      margin-top: 20px;
      width: 100%;
      max-width: 400px;
      background: white;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      box-sizing: border-box;
    }
    .contact-form label {
      margin-bottom: 5px;
      font-weight: bold;
    }
    .contact-form input,
    .contact-form textarea {
      margin-bottom: 10px;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 4px;
      width: 100%;
      box-sizing: border-box;
      font-size: 1rem;
      font-family: Arial, sans-serif;
    }
    .contact-form textarea {
      resize: vertical;
      min-height: 80px;
    }
    .contact-form button {
      padding: 10px;
      background-color: #333;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 1rem;
      font-weight: bold;
    }
    .contact-form button:hover {
      background-color: #555;
    }
    footer {
      width: 100%;
      max-width: 1200px;
      background-color: #007BFF;
      color: white;
      font-weight: bold;
      padding: 20px 40px;
      box-sizing: border-box;
      box-shadow: 0 -2px 6px rgba(0,0,0,0.2);
      display: flex;
      align-items: center;
      justify-content: flex-start;
      font-size: 1rem;
      user-select: none;
      margin: 0 auto;
    }
    /* Service Detail Modal */
    #serviceModal {
      display: none; /* Hidden by default */
      position: fixed;
      z-index: 1000;
      left: 0; top: 0;
      width: 100vw;
      height: 100vh;
      background-color: rgba(0,0,0,0.7);
      overflow-y: auto;
      padding: 20px;
      box-sizing: border-box;
      justify-content: center;
      align-items: center;
    }
    #serviceModal.show {
      display: flex;
    }
    #serviceModal .modal-content {
      background: white;
      border-radius: 10px;
      max-width: 800px;
      width: 100%;
      max-height: 90vh;
      overflow-y: auto;
      padding: 20px 30px;
      box-sizing: border-box;
      position: relative;
      display: flex;
      flex-direction: column;
      gap: 15px;
    }
    #serviceModal .close-btn {
      position: absolute;
      top: 12px;
      right: 20px;
      font-size: 24px;
      font-weight: bold;
      color: #333;
      cursor: pointer;
      user-select: none;
    }
    #serviceModal h2 {
      margin-bottom: 10px;
      user-select: text;
    }
    #serviceModal textarea.description {
      width: 100%;
      min-height: 80px;
      font-size: 1rem;
      padding: 10px;
      resize: vertical;
      border: 1px solid #ccc;
      border-radius: 6px;
    }
    #serviceModal .price-packages {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
      user-select: text;
    }
    #serviceModal .price-packages div {
      background: #007BFF;
      color: white;
      padding: 8px 15px;
      border-radius: 12px;
      font-weight: 600;
      cursor: default;
    }
    #serviceModal .media-preview {
      display: flex;
      gap: 15px;
      flex-wrap: wrap;
      max-height: 300px;
      overflow-y: auto;
    }
    #serviceModal .media-preview img,
    #serviceModal .media-preview video {
      width: 150px;
      height: 100px;
      object-fit: cover;
      border-radius: 8px;
      border: 1px solid #ccc;
      cursor: pointer;
    }
    #serviceModal .upload-section {
      margin-top: 10px;
    }
    #serviceModal input[type="file"] {
      margin-bottom: 10px;
    }
    #serviceModal button.save-btn {
      align-self: flex-end;
      background-color: #007BFF;
      color: white;
      border: none;
      padding: 12px 25px;
      border-radius: 8px;
      font-size: 1rem;
      font-weight: bold;
      cursor: pointer;
      user-select: none;
      transition: background-color 0.3s ease;
    }
    #serviceModal button.save-btn:hover {
      background-color: #0056b3;
    }

    /* Responsive */
    @media (max-width: 900px) {
      #serviceModal .modal-content {
        max-width: 95vw;
      }
      .container {
        flex-direction: column;
        width: 95%;
        max-width: 95%;
      }
      .profile {
        margin-bottom: 20px;
      }
      header {
        flex-wrap: wrap;
        padding: 15px 20px;
        max-width: 100%;
      }
      nav {
        gap: 15px;
        margin-top: 10px;
        width: 100%;
        justify-content: center;
      }
      footer {
        padding: 15px 20px;
        font-size: 0.9rem;
        max-width: 100%;
      }
      #serviceModal .media-preview img,
      #serviceModal .media-preview video {
        width: 100px;
        height: 70px;
      }
    }
  </style>
</head>
<body>

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

<div class="container">
  <div class="profile">
    <img src="your-image-url.jpg" alt="Profile Picture" />
  </div>
  <div class="main-content">
    <!-- Services Section -->
    <div class="services" id="services">
      <!-- 
      Service cards: To add a new service, copy one of the <div class="service-card"> blocks and edit content inside.
      To remove a service, delete the corresponding service card block.
      -->
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

    <!-- Contact Form -->
    <div class="contact-form" id="contactForm">
      <label for="name">الاسم</label>
      <input type="text" id="name" placeholder="ادخل اسمك" />
      <label for="email">الايميل</label>
      <input type="email" id="email" placeholder="ادخل الايميل" />
      <label for="subject">الموضوع</label>
      <input type="text" id="subject" placeholder="ادخل الموضوع" />
      <label for="message">الرسالة</label>
      <textarea id="message" placeholder="ادخل رسالتك"></textarea>
      <button onclick="sendMessage()">Send Message</button>
    </div>
  </div>
</div>

<!-- Service Detail Modal -->
<div id="serviceModal" role="dialog" aria-modal="true" aria-labelledby="modalTitle">
  <div class="modal-content">
    <span class="close-btn" role="button" aria-label="Close" tabindex="0" onclick="closeServiceModal()">&times;</span>
    <h2 id="modalTitle">Service Details</h2>
    <label for="serviceDescription">الوصف:</label>
    <textarea id="serviceDescription" class="description" placeholder="اكتب وصف الخدمة هنا..."></textarea>

    <div class="price-packages" id="pricePackages">
      <!-- Price packages displayed here -->
    </div>

    <div class="upload-section">
      <label for="mediaUpload">رفع ملفات (صور، فيديو, إلخ):</label>
      <input type="file" id="mediaUpload" multiple accept="image/*,video/*" />
      <small>اختر ملفات من جهازك لعرضها هنا</small>
    </div>

    <div class="media-preview" id="mediaPreview">
      <!-- Preview of uploaded media files -->
    </div>

    <button class="save-btn" onclick="saveServiceDetails()">حفظ التعديلات</button>
  </div>
</div>

<footer>
  &copy; 2025 Mohamed Ai Services . All rights reserved.
</footer>

<script>
  // Show home (services) and hide contact form and modal
  function showHome() {
    document.getElementById('services').style.display = 'grid';
    document.getElementById('contactForm').style.display = 'none';
    closeServiceModal();
  }

  // Show contact form and hide services and modal
  function showContact() {
    document.getElementById('services').style.display = 'none';
    document.getElementById('contactForm').style.display = 'flex';
    closeServiceModal();
  }

  // Modal management
  const modal = document.getElementById('serviceModal');
  const mediaPreview = document.getElementById('mediaPreview');
  const mediaUploadInput = document.getElementById('mediaUpload');
  const pricePackagesDiv = document.getElementById('pricePackages');
  const serviceDescription = document.getElementById('serviceDescription');
  let currentServiceName = null;
  let serviceData = {};

  // Sample prices packages default
  const defaultPackages = ["Basic: $50", "Standard: $100", "Premium: $150"];

  // Helper: create preview elements
  function createPreviewElement(file) {
    const url = URL.createObjectURL(file);
    if (file.type.startsWith('image/')) {
      const img = document.createElement('img');
      img.src = url;
      img.alt = file.name;
      img.title = 'انقر للحذف';
      img.style.cursor = 'pointer';
      img.onclick = () => {
        URL.revokeObjectURL(url);
        img.remove();
        // Remove from serviceData.mediaFiles array
        serviceData.mediaFiles = serviceData.mediaFiles.filter(f => f !== file);
      };
      return img;
    } else if (file.type.startsWith('video/')) {
      const video = document.createElement('video');
      video.src = url;
      video.controls = true;
      video.title = 'انقر للحذف';
      video.onclick = () => {
        URL.revokeObjectURL(url);
        video.remove();
        serviceData.mediaFiles = serviceData.mediaFiles.filter(f => f !== file);
      };
      return video;
    }
    return null;
  }

  // Open service modal and load data
  function openServiceModal(serviceName) {
    currentServiceName = serviceName;
    modal.classList.add('show');
    document.getElementById('modalTitle').textContent = serviceName;
    // Load previous data if any
    if (!serviceData[serviceName]) {
      serviceData[serviceName] = {
        description: '',
        packages: [...defaultPackages],
        mediaFiles: []
      };
    }
    serviceDescription.value = serviceData[serviceName].description;
    // Show packages:
    pricePackagesDiv.innerHTML = '';
    serviceData[serviceName].packages.forEach(p => {
      const div = document.createElement('div');
      div.textContent = p;
      pricePackagesDiv.appendChild(div);
    });
    // Clear previous previews
    mediaPreview.innerHTML = '';
    // Show previews of previous files
    serviceData[serviceName].mediaFiles.forEach(file => {
      const el = createPreviewElement(file);
      if (el) mediaPreview.appendChild(el);
    });
    // Clear file input
    mediaUploadInput.value = '';
  }

  function closeServiceModal() {
    modal.classList.remove('show');
    currentServiceName = null;
  }

  // Save data from modal
  function saveServiceDetails() {
    if (!currentServiceName) return;

    serviceData[currentServiceName].description = serviceDescription.value.trim();

    alert('تم حفظ بيانات الخدمة: ' + currentServiceName);
    closeServiceModal();
  }

  // Handle file input change
  mediaUploadInput.addEventListener('change', (e) => {
    if (!currentServiceName) return;
    const files = Array.from(e.target.files);
    if (!serviceData[currentServiceName].mediaFiles) {
      serviceData[currentServiceName].mediaFiles = [];
    }
    files.forEach(file => {
      serviceData[currentServiceName].mediaFiles.push(file);
      const el = createPreviewElement(file);
      if (el) mediaPreview.appendChild(el);
    });
    // Clear file input for same files option
    mediaUploadInput.value = '';
  });

  // Accessibility: close modal on Escape key
  document.addEventListener('keydown', e => {
    if (e.key === 'Escape' && modal.classList.contains('show')) {
      closeServiceModal();
    }
  });

  // Initialize view
  showHome();

</script>

</body>
</html>
</content>
</create_file>

<attempt_completion>
تم تحديث الموقع ليشمل نافذة مودال لتفاصيل الخدمات تحتوي على إمكانية رفع ملفات (صور، فيديوهات، وغيرها) مباشرة من جهازك. 
هذه الملفات تُعرض في القسم الخاص بالمعاينة داخل المودال. يمكنك إضافة وصف خدمة وباقات أسعار.
جميع البيانات محفوظة مؤقتاً في ذاكرة المتصفح أثناء الجلسة ولا تُرفع إلى أي خادم (بدون تخزين دائم).

يمكنك تجربة رفع ملفات من جهازك لكل خدمة ومعاينتها بسهولة.

افتح الملف في المتصفح وجرب النقر على أي خدمة لفتح التفاصيل والرفع.

إذا تريد أي إضافة أخرى أو تعديل، أنا جاهز للمساعدة!
</attempt_completion>

# services.mohamed-ai.com
