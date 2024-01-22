<!-- index.html -->

<!DOCTYPE html>
<html>
	<head>
		<title>Codedamn Lab</title>
	</head>
	<body>
		<form onsubmit="return false">
			<textarea id="comment" placeholder="Type your comment here"></textarea>
			<button id="submit">Submit</button>
		</form>
		<p id="error"></p>
		<ul id="commentList"></ul>
		<script src="script.js"></script>
	</body>
</html>

// script.js

document.addEventListener('DOMContentLoaded', function () {
    // Select form inputs and error paragraph
    const commentInput = document.getElementById('comment');
    const submitButton = document.getElementById('submit');
    const errorParagraph = document.getElementById('error');
    const commentList = document.getElementById('commentList');
  
    // Add event listener to the submit button
    submitButton.addEventListener('click', function () {
      // Empty check on comment textarea value
      const commentText = commentInput.value.trim();
      
      if (commentText === '') {
        // Display error message with the word 'error'
        errorParagraph.textContent = 'Error: Please enter a comment.';
      } else {
        // Clear error message
        errorParagraph.textContent = '';
  
        // Create a new list item and append the comment
        const newComment = document.createElement('li');
        newComment.textContent = commentText;
  
        // Append the new list item to the commentList
        commentList.appendChild(newComment);
  
        // Clear the comment textarea
        commentInput.value = '';
      }
    });
  });
  
