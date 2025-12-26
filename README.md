# Project Responsive Web Design using Bootstrap
# Date:09.10.2025
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
```
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" href="style.css">
    <title>PharmEasy - Your Trusted Online Pharmacy</title>
    <style>
          h1,p,h2{
            color:cyan ;
          }
          body{
            border: 5px double greenyellow;
            padding: 10px;
          }
        </style>
  </head>
<body bgcolor="black"> 
  
  <header><center>
    <h1>Pharmasy</h1>
    <p >Your Trusted Online Pharmacy</p>
    </center>
  </header>

  <section>
    <h2 style="text-align:center;">Featured Products</h2>
    <div class="products">
      <div class="product-card">
        <img src="para.jpg" alt="Paracetamol">
        <p><h1>Paracetamol</h1></p>
        <h2>rs.30</h2></p>
      </div>
      <div class="product-card">
        <img src="vit.jpg" alt="Vitamin C">
        <p><h1>Vitamin C</h1></p>
        <h2>rs.20</h2>
      </div>
      <div class="product-card">
        <img src="det.jpg" alt="Detol">
        <p><h1>Detol</b></h1>
        <h2>rs.50 </h2>
      </div>
      <div class="product-card">
      <img src="Wellness Surgical Absorbent Cotton Roll.jpeg" alt="cotton roll">
      <p><h1>cotton</h1></p>
      <h2>rs.50</h2>
    </div>
    <div class="product-card">
      <img src="san.jpg" alt="hand sanitizer">
      <p><h1>sanitizer</h1></p>
      <h2>rs.60</h2>
    </div>
     <div class="product-card">
      <img src="band.jpg" alt="bandage">
      <p><h1>bandage</h1></p>
      <h2>rs.60</h2>
    </div>
    <div class="product-card">
      <img src="ors..jpeg" alt="Oral rehydration solution">
      <p><h2>ORS</b></h2>
      <h2>rs.20</h2>
    </div>
    <div class="product-card">
      <img src="amo.jpeg" alt="Amoxicilin">
      <p><h2>Amoxicilin</h1`></p>
      <h2>rs.20</h2>
    </div>
    <div class="product-card">
      <img src="sy.jpeg" alt="cough syrup">
      <p><h1>syrup</h1></p>
      <h2>rs.120</h2>
    </div>
    <div class="product-card">
      <img src="tab.jpeg" alt="cetirizin">
      <p><h1>cetrizin</h1></p>
      <h2>rs.15</h2>
    </div>
    </div>
  </section>
</body>
</html>

style.css

style
    .body {
        background-color: aqua;
    }
    .products {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px; 
      margin-top: 20px;
    }

    .product-card {
      width: 200px;
      text-align: center;
      border: 1px green;
      border-radius: 10px;
      padding: 10px;
      background-color:white
      
    }

    .product-card img {
      width: 100%;
      height: 150px;
      object-fit: cover;
      border-radius: 8px;
    }
    .products {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px; 
      margin-top: 20px;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    .button:hover {
  background-color: #45a049; /* Darker green */
  transform: scale(1.1);
    }
    .products:hover {
  transform: scale(1.1); /* Makes it pop */
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3); /* Adds shadow for depth */
}

```


# OUTPUT:
![alt text](<Screenshot (26).png>)
# RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
