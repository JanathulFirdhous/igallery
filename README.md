# Ex.08 Design of Interactive Image Gallery
## Date:14.12.2024

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
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Photo Gallery of Actors</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: pink;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .gallery-container {
            text-align: center;
            max-width: 650px; 
        }

        .gallery {
            display: flex;
            flex-wrap: wrap; 
            justify-content: center; 
            overflow: hidden;
        }

        .gallery-item {
            width: 150px; 
            height: 150px; 
            margin: 10px; 
            transition: transform 0.5s ease-in-out;
        }

        .controls {
            margin-top: 20px;
        }

        button {
            padding: 20px 40px; 
            margin: 0 10px;
            border: none;
            border-radius: 4px;
            background-color: #28a745;
            color: white;
            font-size: 18px; 
            cursor: pointer;
        }

        button:hover {
            background-color: pink;
        }
    </style>
</head>
<body>
    <div class="gallery-container">
        <h1>Interactive Photo Gallery of Actors</h1>
        <div class="gallery">
            <img src="maran.png" alt="Image 1" class="gallery-item">
            <img src="sk.png" alt="Image 2" class="gallery-item">
            <img src="saman.png" alt="Image 3" class="gallery-item">
            <img src="devar.png" alt="Image 4" class="gallery-item">
            <img src="bommi.png" alt="Image 5" class="gallery-item">
            <img src="ajith.png" alt="Image 6" class="gallery-item">
            <img src="rash.png" alt="Image 7" class="gallery-item">
            <img src="surya.png" alt="Image 8" class="gallery-item">
        </div>
        <div class="controls">
            <button onclick="prevImage()">Prev</button>
            <button onclick="nextImage()">Next</button>
        </div>
    </div>
    <script>
        let currentIndex = 0;

        function showImage(index) {
            const gallery = document.querySelector('.gallery');
            gallery.style.transform = `translateX(${-index * 170}px)`; 
        }

        function prevImage() {
            const totalImages = document.querySelectorAll('.gallery-item').length;
            currentIndex = (currentIndex > 0) ? currentIndex - 1 : totalImages - 1;
            showImage(currentIndex);
        }

        function nextImage() {
            const totalImages = document.querySelectorAll('.gallery-item').length;
            currentIndex = (currentIndex < totalImages - 1) ? currentIndex + 1 : 0;
            showImage(currentIndex);
        }
    </script>
</body>
</html>
```
## OUTPUT:
![alt text](jannath/igalleryapp/static/g01.png)


## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
