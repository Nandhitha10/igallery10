# Ex.08 Design of Interactive Image Gallery
## Date:

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
    <title>Interactive Image Gallery</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: rgba(0, 0, 0, 0.936);
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 10px;
            padding: 20px;
        }

        .gallery img {
            width: 100%;
            height: auto;
            border-radius: 0%;
            cursor: pointer;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .gallery img:hover {
            transform: scale(1.1);
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }

        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(222, 51, 151, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        .modal img {
            max-width: 90%;
            max-height: 90%;
            border-radius: 10px;
        }

        .modal-close {
            position: absolute;
            top: 20px;
            right: 30px;
            font-size: 2rem;
            color: white;
            cursor: pointer;
        }
        footer {
            text-align: center;
            font-size: 16px;
            margin-top: 40px; 
            color: burlywood;
        }

    </style>
</head>
<body>

<div class="gallery">
    <img src="Z1.png" alt="Image 1">
    <img src="Z2.png" alt="Image 2">
    <img src="z3.png" alt="Image 3">
    <img src="z4.png" alt="Image 4">
    <img src="z5.png" alt="Image 5">
    <img src="z6.png" alt="Image 6">
 

</div>

<div class="modal" id="modal">
    <span class="modal-close" id="modalClose">&times;</span>
    <img id="modalImage" src="" alt="Expanded Image">
</div>
<footer >
    Designed and developed by NANDHITHA S &copy; 2024
</footer>


<script>
    const gallery = document.querySelector('.gallery');
    const modal = document.getElementById('modal');
    const modalImage = document.getElementById('modalImage');
    const modalClose = document.getElementById('modalClose');

    gallery.addEventListener('click', (e) => {
        if (e.target.tagName === 'IMG') {
            modalImage.src = e.target.src;
            modal.style.display = 'flex';
        }
    });

    modalClose.addEventListener('click', () => {
        modal.style.display = 'none';
    });

    modal.addEventListener('click', (e) => {
        if (e.target === modal) {
            modal.style.display = 'none';
        }
    });

</script>

</body>
</html>

```
## OUTPUT:
![alt text](<Screenshot 2025-05-10 164916.png>)
 ![alt text](<Screenshot 2025-05-10 164931.png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
