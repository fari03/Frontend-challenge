<!DOCTYPE html>
<html>
  <head>
    <title>Specificity in CSS</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <p class="p-text">Paragraph 1</p>
    <p class="p-text" style="color: blue;">Paragraph 2</p>
    <p class="p-text">Paragraph 3</p>
  </body>
</html>

/* styles.css */
.p-text {
    color: red; /* Original rule */
  }
  
  p.p-text {
    color: green; /* Increased specificity with the element selector */
  }
  
