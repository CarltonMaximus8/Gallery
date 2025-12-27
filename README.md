# Ex.08 Design of Interactive Image Gallery
# Date:27/12/25
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
web.html
<html>
<head>
    <title>Interactive Image Gallery</title>
    <link rel="stylesheet" href="styles.css">
</head>

    <header>
        <h1>Interactive Image Gallery</h1>
    </header>
<body>


    <div class="gallery-container">
        <img id="galleryImage" src="rohit.jpg" alt="Gallery Image">
        <p id="caption">ROHIT SHARMA</p>

        <div class="buttons">
            <button onclick="prevImage()">Previous</button>
            <button onclick="nextImage()">Next</button>
        </div>
    </div>

    <footer>
                 Developed by CARLTON MAXIMUS (25006709)  &copy 2025
    </footer>

    <script src="scripts.js"></script>
</body>
</html>

styles.css
body {
    margin: 0;
    background-color: rgb(0, 162, 255);
    text-align: center;
}

header {
    background-color:yellow;
    color: black;
    padding: 5px;
    font-size: 15px;
}
.gallery-container {
    width: 450px;
    margin: 40px auto;
    background: gold;
    padding: 20px;
    border-radius: 15px;
    border: 5px solid red;

}

.gallery-container img {
    width: 100%;
    height: 300px;
    object-fit: fit;
    border-radius: 22px;
    border: 5px solid blue;
}

#caption {
    margin: 12px 0;
    font-weight: bold;
    font-size: 30px;
    
}

.buttons {
    margin-top: 5px;
}

button {
    padding: 8px 20px;
    margin: 10px;
    border:8px solid gold;
    background-color:blue;
    color: white;
    border-radius: 6px;
    cursor: pointer;
}

button:hover {
    background-color: #4338ca;
}

footer {
    position: fixed;
    bottom: 0;
    width: 100%;
    background-color:pink;
    color:black;
    padding: 10px;
    font-size: 25px;
}

scripts.js
let images = [
    {
        src: "rohit.jpg",
        caption: "ROHIT SHARMA"
    },
    {
        src: "hardik.jpg",
        caption: "HARDIK PANDYA"
    },
    {
        src: "bumrah.jpg",
        caption: "JASPRIT BUMRAH"
    },
    {
        src: "surya.jpg",
        caption: "SURYAKUMAR YADAV"
    },
    {
        src: "tilak.jpg",
        caption: "TILAK VARMA"
    },
];

let Index = 0;

function showImage() {
    document.getElementById("galleryImage").src = images[Index].src;
    document.getElementById("caption").innerText = images[Index].caption;
}

function nextImage() {
    Index++;
    if (Index >= images.length) {
        Index = 0;
    }
    showImage();
}

function prevImage() {
    Index--;
    if (Index < 0) {
        Index = images.length - 1;
    }
    showImage();
}


```
# OUTPUT:
<img width="1920" height="1080" alt="Screenshot (28)" src="https://github.com/user-attachments/assets/f1caf4aa-2524-4f9a-8580-424b710b62e1" />
<img width="1920" height="1080" alt="Screenshot (29)" src="https://github.com/user-attachments/assets/43d50a27-cf30-40ea-ab2d-9d1a473699d5" />
<img width="1920" height="1080" alt="Screenshot (30)" src="https://github.com/user-attachments/assets/652838b7-b020-48fd-b7b9-b66287e40621" />
<img width="1920" height="1080" alt="Screenshot (31)" src="https://github.com/user-attachments/assets/762c501c-dfe7-4f4a-bcd2-27f6b0f16cba" />
<img width="1920" height="1080" alt="Screenshot (32)" src="https://github.com/user-attachments/assets/6465162a-f17e-41a0-9ec4-18df0e546ed8" />

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
