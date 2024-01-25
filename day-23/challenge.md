<!DOCTYPE html>
<html>
	<head>
		<title>Video Tag Lab</title>
	</head>
	<body>
		<!-- Video tag with controls -->
		<video id="video" width="320" height="240" controls>
			<source src="https://sample-videos.com/video123/mp4/720/big_buck_bunny_720p_1mb.mp4" type="video/mp4">
		</video>

		<!-- Mute Button -->
		<button id="muteButton">Mute/Unmute</button>

		<script src="script.js"></script>
	</body>
</html>

// script.js
document.addEventListener('DOMContentLoaded', () => {
    const video = document.getElementById('myVideo');
    const muteButton = document.getElementById('muteButton');

    muteButton.addEventListener('click', () => {
        // Toggle the muted property of the video
        video.muted = !video.muted;

        // Change button text based on the muted status
        muteButton.textContent = video.muted ? 'Unmute' : 'Mute';
    });
});
