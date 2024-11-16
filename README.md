<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Photo Gallery</title>
</head>
<body>
    <div class="gallery">
        <figure tabindex="0" onmouseover="imageHover(this)" onmouseleave="imageLeave(this)" onfocus="imageFocus(this)" onblur="imageBlur(this)">
            <img src="image1.jpg" alt="Description of image 1">
            <figcaption>Image 1</figcaption>
        </figure>
        <figure tabindex="0" onmouseover="imageHover(this)" onmouseleave="imageLeave(this)" onfocus="imageFocus(this)" onblur="imageBlur(this)">
            <img src="image2.jpg" alt="Description of image 2">
            <figcaption>Image 2</figcaption>
        </figure>
        <figure tabindex="0" onmouseover="imageHover(this)" onmouseleave="imageLeave(this)" onfocus="imageFocus(this)" onblur="imageBlur(this)">
            <img src="image3.jpg" alt="Description of image 3">
            <figcaption>Image 3</figcaption>
        </figure>
        <figure tabindex="0" onmouseover="imageHover(this)" onmouseleave="imageLeave(this)" onfocus="imageFocus(this)" onblur="imageBlur(this)">
            <img src="image4.jpg" alt="Description of image 4">
            <figcaption>Image 4</figcaption>
        </figure>
        <figure tabindex="0" onmouseover="imageHover(this)" onmouseleave="imageLeave(this)" onfocus="imageFocus(this)" onblur="imageBlur(this)">
            <img src="image5.jpg" alt="Description of image 5">
            <figcaption>Image 5</figcaption>
        </figure>
        <figure tabindex="0" onmouseover="imageHover(this)" onmouseleave="imageLeave(this)" onfocus="imageFocus(this)" onblur="imageBlur(this)">
            <img src="image6.jpg" alt="Description of image 6">
            <figcaption>Image 6</figcaption>
        </figure>
    </div>
    
    <script>
        // Fonction de gestion du survol de l'image
        function imageHover(element) {
            console.log("Hovered over: " + element.querySelector('img').alt);
        }

        // Fonction de gestion de la sortie du survol
        function imageLeave(element) {
            console.log("Left image: " + element.querySelector('img').alt);
        }

        // Fonction de gestion de la mise au point de l'image
        function imageFocus(element) {
            console.log("Focused on: " + element.querySelector('img').alt);
        }

        // Fonction de gestion de la perte du focus de l'image
        function imageBlur(element) {
            console.log("Blurred on: " + element.querySelector('img').alt);
        }

        // Ajouter l'attribut tabindex à chaque image (si non ajouté manuellement)
        window.onload = function() {
            let figures = document.querySelectorAll('figure');
            figures.forEach(function(figure) {
                figure.setAttribute('tabindex', '0');
            });
        }
    </script>
</body>
</html>
