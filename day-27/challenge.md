<!DOCTYPE html>
<html>
	<head>
		<title>Text-Overflow Property Lab</title>
		<link rel="stylesheet" href="styles.css" />
	</head>
	<body>
		<div id="container">
			<p id="text">
				This is some long text that will overflow the container and show ellipsis when hidden.
			</p>
		</div>
		<script src="script.js"></script>
	</body>
</html>

/* styles.css */
#container {
    width: 300px;
  }
  
  #text {
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }

  
