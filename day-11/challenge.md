<!-- index.html -->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Codedamn Lab</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <div class="box"></div>
        <div class="box"></div>
        <div class="box span-two-columns"></div>
        <div class="box"></div>
        <div class="box"></div>
        <div class="box"></div>
    </div>
    <script src="script.js"></script>
</body>
</html>

/* style.css */


#container {
    column-count: 2;
}

.box {
    width: 100%;
    height: 100px;
    margin: 10px;
    background-color: lightblue;
}

.span-two-columns {
    column-span: all;
}

/* script.js */

function changeColumnCount(count) {
    const container = document.getElementById('container');
    container.style.columnCount = count;
}
