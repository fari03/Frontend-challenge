<!-- index.html -->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Network Information API Lab</title>
</head>
<body>
    <button id="getNetworkInfo">Get Network Info</button>
    <div id="networkInfoContainer"></div>

    <script src="script.js"></script>
</body>
</html>

// script.js

document.addEventListener('DOMContentLoaded', function () {
    const getNetworkInfoButton = document.getElementById('getNetworkInfo');
    const networkInfoContainer = document.getElementById('networkInfoContainer');

    getNetworkInfoButton.addEventListener('click', function () {
        // Check if the Network Information API is supported
        if ('connection' in navigator) {
            const connection = navigator.connection || navigator.mozConnection || navigator.webkitConnection;

            // Retrieve network information
            const effectiveType = connection.effectiveType || 'N/A';
            const downlink = connection.downlink || 'N/A';
            const rtt = connection.rtt || 'N/A';
            const saveData = connection.saveData || 'N/A';

            // Create a string with network information
            const networkInfoString = `
                Effective Type: ${effectiveType}<br>
                Downlink: ${downlink} Mbps<br>
                RTT: ${rtt} milliseconds<br>
                Save Data: ${saveData ? 'Enabled' : 'Disabled'}
            `;

            // Set the network information as the innerHTML of the networkInfoContainer
            networkInfoContainer.innerHTML = networkInfoString;
        } else {
            // Display a message if the Network Information API is not supported
            networkInfoContainer.innerHTML = 'Network Information API is not supported in this browser.';
        }
    });
});
