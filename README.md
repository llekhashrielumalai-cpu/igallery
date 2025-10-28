# Ex.08 Design of Interactive Image Gallery
## Date:15/10/2025

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
interactive.html
 <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Interactive Image Gallery</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <h1>My Interactive Image Gallery</h1>
  <h3>LEKHASHRI E(25008477)</h3>
  <div class="gallery">
    <div class="thumbnail"><img src="pic1.png" alt="Image 1" /></div>
    <div class="thumbnail"><img src="pic2.png" alt="Image 2" /></div>
    <div class="thumbnail"><img src="pic3.png" alt="Image 3" /></div>
    <div class="thumbnail"><img src="pic4.png" alt="Image 4" /></div>
    <div class="thumbnail"><img src="pic5.png" alt="Image 5" /></div>
  </div>

  <div id="lightbox" class="lightbox hidden">
    <span class="close">&times;</span>
    <img class="lightbox-img" src="" alt="Expanded view" />
  </div>

  <script src="script.js"></script>
</body>
</html>

style.css
body {
  font-family: Arial, sans-serif;
  text-align: center;
  background: #f4f4f4;
  margin: 0;
  padding: 20px;
}

h1 {
  color: #333;
}

.gallery {
  display: flex;
  flex-wrap: wrap;
  align-items: baseline;
  justify-content: center;
  gap: 15px;
  margin-top: 20px;
}

.thumbnail img {
  width: 200px;
  height: auto;
  border-radius: 8px;
  cursor: pointer;
  transition: transform 0.3s ease;
}

.thumbnail img:hover {
  transform: scale(1.05);
}

.lightbox {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.8);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.lightbox-img {
  max-width: 90%;
 max-height: 80%;
  border-radius: 10px;
}

.close {
  position: absolute;
  top: 30px;
  right: 40px;
  font-size: 40px;
  color: white;
  cursor: pointer;
}

.hidden {
  display: none;
}

script.js
const thumbnails = document.querySelectorAll('.thumbnail img');
const lightbox = document.getElementById('lightbox');
const lightboxImg = document.querySelector('.lightbox-img');
const closeBtn = document.querySelector('.close');

thumbnails.forEach(img => {
  img.addEventListener('click', () => {
    lightboxImg.src = img.src;
    lightbox.classList.remove('hidden');
  });
});

closeBtn.addEventListener('click', () => {
  lightbox.classList.add('hidden');
});
```
## OUTPUT:
![alt text](<Screenshot (36).png>)
![alt text](<Screenshot (37).png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
