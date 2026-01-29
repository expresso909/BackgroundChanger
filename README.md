# BackgroundChanger

// Html File - [
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <link rel="stylesheet" href="style.css" />
    <link rel="stylesheet" href="../styles.css" />
    <title>JavaScript Background Color Switcher</title>
  </head>
  <body>
    <nav>
      <a href="/" aria-current="page">Home</a>
      <a target="_blank" href="https://www.youtube.com/@chaiaurcode"
        >Youtube channel</a
      >
    </nav>
    <div class="canvas">
      <!-- <a
        style="
          background-color: #fff;
          padding: 10px 30px;
          border-radius: 8px;
          color: #212121;
          text-decoration: none;
          border: 2px solid #212121;
        "
        href="../index.html"
        >Back to Home Page</a
      > -->
      <h1>Color Scheme Switcher</h1>
      <span class="button" id="grey"></span>
      <span class="button" id="white"></span>
      <span class="button" id="blue"></span>
      <span class="button" id="lavender"></span>
      <span class="button" id="Cyan"></span>
      <span class="button" id="Orange"></span>
      <span class="button" id="Neon"></span>
      <span class="button" id="Magnite"></span>
      <span class="button" id="yellow"></span>
      <h2>
        Try clicking on one of the colors above
        <span>to change the background color of this page!</span>
      </h2>
    </div>
    <script src="chaiaurcode.js"></script>
  </body>
</html> 
]
// CSS File -[
html {
  margin: 0;
}

span {
  display: block;
}
.canvas {
  margin: 100px auto 100px;
  width: 80%;
  text-align: center;
}

.button {
  width: 100px;
  height: 100px;
  border: solid black 2px;
  display: inline-block;
}

#grey {
  background: grey;
}

#white {
  background: white;
}
#blue {
  background: blue;
}
#yellow {
  background: yellow;
}
#lavender {
  background: lavender;
}
#red{
  background: red;
}
#Neon {
  background: rgb(152, 243, 5);
}
#Cyan {
  background: rgb(5, 160, 250);
}
#Magnite {
  background: rgba(165, 74, 218, 0.281);
}
#Orange {
  background: rgb(250, 82, 4);
} 
]
Java Script File - [
const buttons = document.querySelectorAll('.button');
const body = document.querySelector('body');

buttons.forEach(function(button) {
  console.log(button); // each HTMLSpanElement

  button.addEventListener('click', function () {
    if (button.id === 'Neon') body.style.backgroundColor = 'rgb(152,243,5)'; // (This is wriiten for the Color "Neon" which doesnot exist in CSS)
    if (button.id === 'Magnite') body.style.backgroundColor = 'rgba(165, 74, 218, 0.281)';  // (This is wriiten for the Color "Magnite" which doesnot exist in CSS)

    body.style.backgroundColor = button.id;

  });
});
]
