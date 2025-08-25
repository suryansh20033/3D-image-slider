3D image
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>3d Image</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>
    <div class="slider-container">
        <div class="slider">
            <div class="slide">
                <img src="1.jpg" >
            </div>
        
        
            <div class="slide">
                <img src="2.webp" >
            </div>
        
        
            <div class="slide">
                <img src="3.jpg" alt="slide 3" >
            </div>
        
        
            <div class="slide">
                <img src="4.jpg" alt="slide 4" >
            </div>
        </div>
        </div>
        
    </div>
        
    
</body>
</html>



/** CSS**/
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
body{
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: linear-gradient(135deg, black, #0f2027, #203a43, #2c5364);
    font-family: Arial, sans-serif;
    overflow: hidden;
}
.slider-container{
    width: 800px;
    height: 400px;
    position: relative;
    perspective: 1000px;
}

.slider{
    width: 100%;
    height: 100%;
    position: absolute;
    transform-style: preserve-3d;
    animation: rotate 15s infinite linear;
    
}
.slide{
    width: 60%;
    height: 80%;
    position: absolute;
    transform-style: preserve-3d;
    left: 20%;
    top: 10%;
    border-radius: 15px;
    overflow: hidden;
    cursor: pointer;
    box-shadow: 0 10px 30px rgba(0,0,0,0.3);
    transition: transform 1s;
    
}
.slider img{
    width: 100%;
    height: 100%;
    object-fit: cover;

}
.slide:nth-child(1){transform: rotateY(0deg) translateZ(400px);}
.slide:nth-child(2){transform: rotateY(90deg) translateZ(400px);}
.slide:nth-child(3){transform: rotateY(180deg) translateZ(400px);}
.slide:nth-child(4){transform: rotateY(270deg) translateZ(400px);}

@keyframes rotate{
    0%{transform: rotateY(0deg);}
    25%{transform: rotateY(90deg);}
    50%{transform: rotateY(180deg);}
    75%{transform: rotateY(270deg);}
    100%{transform: rotateY(360deg);}

}
/**pause aniamation on hover**/
.slider-container:hover .slider{
    animation-play-state: paused;
}
    








