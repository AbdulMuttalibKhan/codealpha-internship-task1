<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title> Task1 Image Gallery</title>
  <style>
    body {
      margin: 0;
      padding: 20px;
      font-family: Arial, sans-serif;
      background-color: red;
      text-align: center;
    }

    footer {
      color: black;
      background-color: yellow;
      padding: 20px;
      margin-top: 20px;
    }

    .image-viewer {
      display: flex;
      justify-content: center;
      flex-wrap: nowrap;
      gap: 20px;
      overflow-x: auto;
      padding: 10px;
    }

    .image-viewer img {
      width: 300px;
      height: 200px;
      object-fit: cover;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
      transition: transform 0.3s ease;
    }

    .image-viewer img:hover {
      transform: scale(1.05);
    }

    .navigation {
      margin-top: 20px;
    }

    .navigation button {
      padding: 15px 30px;
      font-size: 20px;
      margin: 0 20px;
      cursor: pointer;
      background-color: white;
      color: black;
      border: none;
      border-radius: 5px;
      transition: background-color 0.3s;
    }

    .navigation button:hover {
      background-color: black;
      color: white;
    }

    .filter-buttons {
      margin: 20px;
    }

    .filter-btn {
      padding: 10px 20px;
      margin: 5px;
      font-size: 16px;
      border: none;
      border-radius: 5px;
      background-color: white;
      cursor: pointer;
      transition: 0.3s;
    }

    .filter-btn:hover, .filter-btn.active {
      background-color: black;
      color: white;
    }
  </style>
</head>
<body>

  <marquee><h1>MY First Image Gallery Internship Task 1</h1></marquee>

  <div class="filter-buttons">
    <button class="filter-btn active" data-filter="all">All</button>
    <button class="filter-btn" data-filter="nature">Nature</button>
    <button class="filter-btn" data-filter="city">City</button>
  </div>

  <div class="image-viewer">
    <!-- Animal Image -->
    <img src="https://cdn.britannica.com/94/494-050-A674AD3A/Fallow-deer-dama-dama.jpg" alt="Animal" data-category="nature">
    
    <!-- Mountain Image -->
    <img src="https://images.unsplash.com/photo-1501785888041-af3ef285b470" alt="Mountain" data-category="nature">

    <!-- Tree Image -->
    <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb" alt="Tree" data-category="nature">

    <!-- City Image -->
    <img src="https://images.unsplash.com/photo-1494526585095-c41746248156" alt="City" data-category="city">

    <!-- Another Nature Image -->
    <img src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee" alt="Forest" data-category="nature">
  </div>

  <form id="myForm">
    <input type="text" placeholder="Enter your name" required>
  </form>  

  <div class="navigation">
    <button id="submit">Submit</button>
    <button id="prevBtn">Previous</button>
    <button id="nextBtn">Next</button>
  </div>
<footer>
© 2025 NatureScape Gallery — All images featured in this gallery are provided for illustrative and educational purposes only.
 Each photograph captures the breathtaking diversity and beauty of the natural world, highlighting wildlife, towering mountains, and tranquil forest scenes. 
 Please note that all images remain the intellectual property of their respective photographers or copyright holders.
  We strive to respect and honor the creativity and effort behind each image. This collection is curated to inspire appreciation and awareness of the environment,
   encouraging viewers to foster a deeper connection with nature and promote conservation efforts worldwide. Unauthorized use or reproduction of these images
    without prior permission is strictly prohibited.
</footer>
  
  <script>
    document.getElementById('prevBtn').addEventListener('click', function () {
      alert('Going to the previous page...');
      window.location.href = 'previous.html'; 
    });

    document.getElementById('nextBtn').addEventListener('click', function () {
      alert('Going to the next page...');
      window.location.href = 'next.html';
    });
  </script>
</body>
</html>
