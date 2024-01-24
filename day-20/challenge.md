<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta http-equiv="X-UA-Compatible" content="IE=edge" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>HTML/CSS Practice Challenges</title>
		<link rel="stylesheet" href="style.css" />
	</head>
	<body>
		<main>
			<div class="playground-card">
				<div class="playground-icon"></div>
				<div class="playground-info">
					<h4 class="playground-title">Playground Title</h4>
					<p class="playground-description">Playground Language & Last opened Time</p>
					<p class="collaborators">Collaborators of the playground</p>
				</div>
			</div>
		</main>
	</body>
</html>

//style.css
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap");

body {
	font-family: "Inter", sans-serif;
	background-color: #f4f4f5;
	padding: 0;
	margin: 0;
	box-sizing: border-box;
}

main {
	display: flex;
	justify-content: center;
	align-items: center;
	height: 100vh;
}

.playground-card {
	background-color: white;
	border-radius: 8px;
	box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
	display: flex;
	padding: 20px;
	width: 300px;
}

.playground-icon {
	background-color: white;
	width: 40px;
	height: 40px;
	border-radius: 50%;
	margin-right: 15px;
}

.playground-info {
	display: flex;
	flex-direction: column;
}

.playground-title {
	font-weight: 600;
	font-size: 1.5rem;
	color: #71717a;
	margin: 0;
}

.playground-description,
.collaborators {
	color: #71717a;
	margin: 0;
}

