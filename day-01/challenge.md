# Day 1 Challenge: HTML Basics and Semantic Elements

## Challenge Question

Create a simple HTML page layout that includes the following semantic elements:

1. Header (`<header>`): Add the text "Page Header" inside it.
2. Navigation Bar (`<nav>`): Include an unordered list (`<ul>`) with three list items (`<li>`), each containing an anchor (`<a>`) with your three favorite links.
3. Main Content (`<main>`): Add the text "Main Content" inside it.
4. Footer (`<footer>`): Include the text "Footer" inside it.

Your HTML content should be placed inside a div with the id "container."

## Sample Solution

<!DOCTYPE html>
<html>
	<head>
		<title>Semantic HTML Structure</title>
		<link rel="stylesheet" href="style.css" />
	</head>
	<body>
		<!-- Starting writing your code below this line -->
		<div id="text-container">
			<header>
				<h1>Page Header</h1>
			</header>
			
			<nav>
				<ul>
					<li><a href="#">Link 1</a></li>
					<li><a href="#">Link 2</a></li>
					<li><a href="#">Link 3</a></li>
				</ul>
			</nav>
			
			<main>
				<p>Main Content</p>
			</main>
			
			<footer>
				<p>Footer</p>
			</footer>
		</div>
	</body>
</html>
