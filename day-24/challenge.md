<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>Zoe's To-Do App</title>
		<link rel="stylesheet" href="style.css" />
	</head>
	<body>
		<input type="text" id="taskInput" placeholder="New task..." />
		<button onclick="addTask()">Add Task</button>
		<div>
			<button onclick="filterTasks('all')">Show All</button>
			<button onclick="filterTasks('completed')">Show Completed</button>
			<button onclick="filterTasks('incomplete')">Show Incomplete</button>
		</div>
		<ul id="taskList"></ul>

		<script src="index.js"></script>
	</body>
</html>

//script.js
function addTask() {
    let taskText = document.getElementById("taskInput").value;
    if (taskText === "") return;

    let li = document.createElement("li");
    li.textContent = taskText;
    li.addEventListener("click", markCompleted);

    document.getElementById("taskList").appendChild(li);
    document.getElementById("taskInput").value = "";
}

function markCompleted(event) {
    event.target.classList.toggle("completed");
}

function filterTasks(filter) {
    let tasks = document.getElementById("taskList").children;

    for (let i = 0; i < tasks.length; i++) {
        switch (filter) {
            case "all":
                tasks[i].style.display = "";
                break;
            case "completed":
                tasks[i].classList.contains("completed")
                    ? (tasks[i].style.display = "")
                    : (tasks[i].style.display = "none");
                break;
            case "incomplete":
                !tasks[i].classList.contains("completed")
                    ? (tasks[i].style.display = "")
                    : (tasks[i].style.display = "none");
                break;
        }
    }
}

