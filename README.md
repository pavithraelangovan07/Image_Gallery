# Ex.08 Design of Interactive Image Gallery
## DATE:8/11/2025

## AIM
  To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS

## Step 1:

Clone the github repository and create Django admin interface

## Step 2:

Change settings.py file to allow request from all hosts.

## Step 3:

Use CSS for positioning and styling.

## Step 4:

Write JavaScript program for implementing interactivit

## Step 5:

Validate the HTML and CSS code

## Step 6:

Publish the website in the given URL.

## PROGRAM
gallery.html
 ```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Interactive Image Gallery</title>

  <!-- Link to CSS -->
  <link rel="stylesheet" href="styles.css" />
</head>
<body>

  <h1 class="title">🌅 My Interactive Image Gallery 🌙</h1>

  <!-- Gallery Section -->
  <div class="gallery">
    <img src="images/beach.jpeg" alt="Beach" class="gallery-item">
    <img src="images/rain.jpeg" alt="Rain" class="gallery-item">
    <img src="images/moon.jpeg" alt="Moon" class="gallery-item">
    <img src="images/sun.jpeg" alt="Sun" class="gallery-item">
    <img src="images/road.jpeg" alt="Road" class="gallery-item">
    <img src="images/mountain.jpeg" alt="Mountain" class="gallery-item">
  </div>

  <!-- Fullscreen Image Popup -->
  <div id="popup" class="popup">
    <span class="close">&times;</span>
    <img class="popup-content" id="popup-img">
    <div id="caption"></div>
  </div>

  <footer>
    <h3>Designed and Developed by pavithra</h3>
  </footer>

  <!-- JavaScript for Interactivity -->
  <script>
    const popup = document.getElementById("popup");
    const popupImg = document.getElementById("popup-img");
    const captionText = document.getElementById("caption");
    const close = document.getElementsByClassName("close")[0];

    document.querySelectorAll(".gallery-item").forEach(img => {
      img.addEventListener("click", () => {
        popup.style.display = "block";
        popupImg.src = img.src;
        captionText.innerHTML = img.alt;
      });
    });

    close.onclick = function() {
      popup.style.display = "none";
    }

    popup.onclick = function(e) {
      if (e.target === popup) popup.style.display = "none";
    }
  </script>

</body>
</html>
```
Styles.css

```
/* General Page Style */
body {
  font-family: Arial, sans-serif;
  background: #f0f0f0;
  margin: 0;
  padding: 0;
}

/* Title */
.title {
  text-align: center;
  margin-top: 20px;
  color: #333;
}

/* Gallery Grid */
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 15px;
  padding: 20px;
}

/* Gallery Images */
.gallery-item {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  cursor: pointer;
}

/* Hover Effect */
.gallery-item:hover {
  transform: scale(1.05);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
}

/* Popup Background */
.popup {
  display: none;
  position: fixed;
  z-index: 1000;
  padding-top: 60px;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgba(0,0,0,0.9);
}

/* Popup Image */
.popup-content {
  margin: auto;
  display: block;
  max-width: 80%;
  max-height: 80%;
  border-radius: 10px;
}

/* Caption */
#caption {
  text-align: center;
  color: #ccc;
  font-size: 18px;
  padding: 10px 0;
}

/* Close Button */
.close {
  position: absolute;
  top: 20px;
  right: 35px;
  color: white;
  font-size: 40px;
  font-weight: bold;
  cursor: pointer;
}

.close:hover {
  color: #bbb;
}

/* Footer */
footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 10px;
  margin-top: 20px;
}

```

## OUTPUT
<img width="1031" height="542" alt="Screenshot 2025-11-09 195431" src="https://github.com/user-attachments/assets/c9e9dc81-7f94-4c06-9dcb-3cc097b5c253" />



<img width="1884" height="1083" alt="Screenshot 2025-10-29 051200" src="https://github.com/user-attachments/assets/7a2481ef-c6c7-4ad1-be02-cf805d46cc85" />

<img width="1915" height="1080" alt="Screenshot 2025-10-29 051213" src="https://github.com/user-attachments/assets/564daa3f-d360-4d47-99d7-5fc116e9fa83" />

## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
