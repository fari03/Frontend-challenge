<!doctype HTML>
<html>
    <head>
        <title>Web Storage Lab</title>
    </head>
    <body>
        <div id="localStorage-setup">
            <input type="text" id="storageKey" placeholder="Enter value" />
            <button id="setStorage">Save to localStorage</button>
        </div>

        <div id="localStorage-retrieve">
            <div id="output"></div>
            <button id="getStorage">Retrieve from localStorage</button>
        </div>

        <script src='script.js'></script>
    </body>
</html>
// script.js
document.getElementById('setStorage').addEventListener('click', function() {
    // Retrieve input value
    const inputValue = document.getElementById('storageKey').value;

    // Save to localStorage with key 'myKey'
    localStorage.setItem('myKey', inputValue);
});

document.getElementById('getStorage').addEventListener('click', function() {
    // Retrieve value from localStorage using key 'myKey'
    const storedValue = localStorage.getItem('myKey');

    // Display the retrieved value in the 'output' div
    document.getElementById('output').textContent = storedValue || 'No data found';
});


