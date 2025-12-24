# Project Responsive Web Design using Bootstrap
# Date:
# AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

## Step 5:
Create a HTML file and include the needed Bootstrap components.

## Step 6:
Publish the website in the LocalHost.

# PROGRAM :
home.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Dribbble Clone - Shots</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" />
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #f8f9fa;
    }
    .shot-card {
      transition: transform 0.3s ease;
    }
    .shot-card:hover {
      transform: scale(1.05);
      box-shadow: 0 8px 16px rgba(0,0,0,0.15);
    }
    .search-bar {
      max-width: 500px;
      margin: 30px auto;
    }
    .category-badge {
      cursor: pointer;
      margin: 0 5px 10px 0;
    }
    .category-badge.active {
      background-color: #6f42c1;
      color: white;
    }
  </style>
</head>
<body>

  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container">
      <a class="navbar-brand fw-bold" href="index.html">dribbble</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item"><a class="nav-link" href="main.html">Home</a></li>
          <li class="nav-item"><a class="nav-link active" href="shots.html">Shots</a></li>
          <li class="nav-item"><a class="nav-link" href="about.html">About</a></li>
          <li class="nav-item"><a class="nav-link" href="login.html">Login</a></li>
          <li class="nav-item"><a class="btn btn-dark ms-2" href="signup.html">Sign up</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Search and filter -->
  <div class="search-bar text-center">
    <input
      type="text"
      id="searchInput"
      class="form-control"
      placeholder="Search shots by title or category..."
      oninput="filterShots()"
    />
  </div>

  <div class="container">
    <!-- Category filter badges -->
    <div class="mb-3 text-center" id="categoryFilters">
      <span class="badge bg-secondary category-badge active" onclick="filterByCategory('all')">All</span>
      <span class="badge bg-secondary category-badge" onclick="filterByCategory('UI')">UI</span>
      <span class="badge bg-secondary category-badge" onclick="filterByCategory('Illustration')">Illustration</span>
      <span class="badge bg-secondary category-badge" onclick="filterByCategory('Branding')">Branding</span>
      <span class="badge bg-secondary category-badge" onclick="filterByCategory('Animation')">Animation</span>
    </div>

    <!-- Shots grid -->
    <div class="row" id="shotsContainer">

      <!-- Sample shot cards (can add more) -->
      <div class="col-md-4 mb-4 shot-item" data-title="Dark Mode Dashboard" data-category="UI">
        <div class="card shot-card shadow-sm">
          <img src="darkmodedashboard.png" class="card-img-top" alt="Dark Mode Dashboard" />
          <div class="card-body">
            <h5 class="card-title">Dark Mode Dashboard</h5>
            <p class="card-text"><small class="text-muted">Category: UI</small></p>
          </div>
        </div>
      </div>

      <div class="col-md-4 mb-4 shot-item" data-title="Abstract Illustration" data-category="Illustration">
        <div class="card shot-card shadow-sm">
          <img src="abstract illustration.avif" class="card-img-top" alt="Abstract Illustration" />
          <div class="card-body">
            <h5 class="card-title">Abstract Illustration</h5>
            <p class="card-text"><small class="text-muted">Category: Illustration</small></p>
          </div>
        </div>
      </div>

      <div class="col-md-4 mb-4 shot-item" data-title="Branding for Startup" data-category="Branding">
        <div class="card shot-card shadow-sm">
          <img src="Branding for startup ].png" class="card-img-top" alt="Branding for Startup" />
          <div class="card-body">
            <h5 class="card-title">Branding for Startup</h5>
            <p class="card-text"><small class="text-muted">Category: Branding</small></p>
          </div>
        </div>
      </div>

      <div class="col-md-4 mb-4 shot-item" data-title="Smooth Loading Animation" data-category="Animation">
        <div class="card shot-card shadow-sm">
          <img src="smooth loading animation 2.gif" class="card-img-top" alt="Smooth Loading Animation" />
          <div class="card-body">
            <h5 class="card-title">Smooth Loading Animation</h5>
            <p class="card-text"><small class="text-muted">Category: Animation</small></p>
          </div>
        </div>
      </div>

      <div class="col-md-4 mb-4 shot-item" data-title="Mobile App UI" data-category="UI">
        <div class="card shot-card shadow-sm">
          <img src="mobile app UI.png" class="card-img-top" alt="Mobile App UI" />
          <div class="card-body">
            <h5 class="card-title">Mobile App UI</h5>
            <p class="card-text"><small class="text-muted">Category: UI</small></p>
          </div>
        </div>
      </div>

      <div class="col-md-4 mb-4 shot-item" data-title="Logo Animation" data-category="Animation">
        <div class="card shot-card shadow-sm">
          <img src="logo animation.webp" class="card-img-top" alt="Logo Animation" />
          <div class="card-body">
            <h5 class="card-title">Logo Animation</h5>
            <p class="card-text"><small class="text-muted">Category: Animation</small></p>
          </div>
        </div>
      </div>

    </div>
  </div>

  <!-- Footer -->
  <footer class="footer bg-dark text-white py-4 text-center mt-5">
    <div class="container">
      <p class="mb-0">&copy; 2025 Dribbble Clone. Designed using Bootstrap.</p>
    </div>
  </footer>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
  <script>
    const shots = document.querySelectorAll('.shot-item');
    const categoryBadges = document.querySelectorAll('.category-badge');
    let activeCategory = 'all';

    function filterShots() {
      const searchText = document.getElementById('searchInput').value.toLowerCase();

      shots.forEach(shot => {
        const title = shot.getAttribute('data-title').toLowerCase();
        const category = shot.getAttribute('data-category').toLowerCase();
        const matchesCategory = (activeCategory === 'all') || (category === activeCategory);
        const matchesSearch = title.includes(searchText) || category.includes(searchText);

        if (matchesCategory && matchesSearch) {
          shot.style.display = '';
        } else {
          shot.style.display = 'none';
        }
      });
    }

    function filterByCategory(category) {
      activeCategory = category.toLowerCase();

      categoryBadges.forEach(badge => {
        badge.classList.toggle('active', badge.textContent.toLowerCase() === activeCategory);
      });

      filterShots();
    }
  </script>
</body>
</html>

signup.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Dribbble Clone - Sign Up</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"/>
  <style>
    body {
      background-color: #f8f9fa;
      font-family: 'Segoe UI', sans-serif;
    }
    .signup-container {
      max-width: 500px;
      margin: 80px auto;
      background: white;
      padding: 40px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
  </style>
</head>
<body>
  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container">
      <a class="navbar-brand fw-bold" href="index.html">dribbble</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
            <li class="nav-item"><a class="nav-link" href="main.html">Home</a></li>
          <li class="nav-item"><a class="nav-link" href="shots.html">Shots</a></li>
          <li class="nav-item"><a class="nav-link" href="about.html">About</a></li>
          <li class="nav-item"><a class="nav-link" href="login.html">Login</a></li>
          <li class="nav-item"><a class="btn btn-dark ms-2 active" href="signup.html">Sign up</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Signup Form -->
  <div class="signup-container">
    <h3 class="text-center mb-4">Create Your Account</h3>
    <form onsubmit="return validateSignupForm()">
      <div class="mb-3">
        <label for="name" class="form-label">Full Name</label>
        <input type="text" class="form-control" id="name" placeholder="John Doe" required />
      </div>
      <div class="mb-3">
        <label for="email" class="form-label">Email address</label>
        <input type="email" class="form-control" id="email" placeholder="name@example.com" required />
      </div>
      <div class="mb-3">
        <label for="password" class="form-label">Password</label>
        <input type="password" class="form-control" id="password" placeholder="Create password" required />
      </div>
      <div class="mb-3">
        <label for="confirmPassword" class="form-label">Confirm Password</label>
        <input type="password" class="form-control" id="confirmPassword" placeholder="Re-enter password" required />
      </div>
      <div class="d-grid">
        <button type="submit" class="btn btn-primary">Sign Up</button>
      </div>
    </form>
    <p class="text-center mt-3">Already have an account? <a href="login.html">Login</a></p>
  </div>

  <!-- Footer -->
  <footer class="footer bg-dark text-white mt-5 py-4 text-center">
    <div class="container">
      <p class="mb-0">&copy; 2025 Dribbble Clone. All rights reserved.</p>
    </div>
  </footer>

  <!-- Scripts -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
  <script>
    function validateSignupForm() {
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const password = document.getElementById('password').value;
      const confirmPassword = document.getElementById('confirmPassword').value;

      if (!name || !email || !password || !confirmPassword) {
        alert("Please fill in all fields.");
        return false;
      }

      if (password !== confirmPassword) {
        alert("Passwords do not match.");
        return false;
      }

      alert("Signup successful! (Demo only)");
      return false; // Prevent form submission in demo
    }
  </script>
</body>
</html>

login.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Dribbble Clone - Login</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"/>
  <style>
    body {
      background-color: #f0f2f5;
      font-family: 'Segoe UI', sans-serif;
    }
    .login-container {
      max-width: 400px;
      margin: 80px auto;
      background: white;
      padding: 40px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
  </style>
</head>
<body>
  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container">
      <a class="navbar-brand fw-bold" href="index.html">dribbble</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
            <li class="nav-item"><a class="nav-link" href="main.html">Home</a></li>
          <li class="nav-item"><a class="nav-link" href="shots.html">Shots</a></li>
          <li class="nav-item"><a class="nav-link" href="about.html">About</a></li>
          <li class="nav-item"><a class="nav-link active" href="login.html">Login</a></li>
          <li class="nav-item"><a class="btn btn-dark ms-2" href="signup.html">Sign up</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Login Form -->
  <div class="login-container">
    <h3 class="text-center mb-4">Login to Your Account</h3>
    <form onsubmit="return validateLoginForm()">
      <div class="mb-3">
        <label for="email" class="form-label">Email address</label>
        <input type="email" class="form-control" id="email" placeholder="name@example.com" required />
      </div>
      <div class="mb-3">
        <label for="password" class="form-label">Password</label>
        <input type="password" class="form-control" id="password" placeholder="••••••••" required />
      </div>
      <div class="d-grid">
        <button type="submit" class="btn btn-primary">Login</button>
      </div>
    </form>
    <p class="text-center mt-3">Don't have an account? <a href="signup.html">Sign up</a></p>
  </div>

  <!-- Footer -->
  <footer class="footer bg-dark text-white mt-5 py-4 text-center">
    <div class="container">
      <p class="mb-0">&copy; 2025 Dribbble Clone. All rights reserved.</p>
    </div>
  </footer>

  <!-- Scripts -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
  <script>
    function validateLoginForm() {
      const email = document.getElementById('email').value;
      const password = document.getElementById('password').value;

      if (!email || !password) {
        alert("Please fill in all fields.");
        return false;
      }

      alert("Login successful! (Demo only)");
      return false; // Prevent form submission in demo
    }
  </script>
</body>
</html>

# OUTPUT:
<img width="816" height="297" alt="image" src="https://github.com/user-attachments/assets/8b5bf796-1a6c-43c0-b461-11518d3af995" />
<img width="801" height="428" alt="image" src="https://github.com/user-attachments/assets/67a832bb-0856-4899-9aa7-b092ce45004b" />
<img width="811" height="431" alt="image" src="https://github.com/user-attachments/assets/5b243961-82de-4138-9b2f-729ecc7a6464" />
<img width="796" height="416" alt="image" src="https://github.com/user-attachments/assets/01a97ae6-4fb2-414f-ae95-7c1b755d646e" />

# RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
