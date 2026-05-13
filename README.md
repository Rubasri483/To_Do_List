# Ex03 To-Do List using JavaScript
## Date: 13-05-2026

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
## HTML
```html
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Todo Application</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<div class="container">
    <h1>Todo Application</h1>

    <div class="todo-input">
        <input type="text" id="taskInput" placeholder="Enter your task">
        <button onclick="addTask()">Add</button>
    </div>

    <ul id="taskList"></ul>

    <div class="buttons">
        <button onclick="clearTasks()">Clear All</button>
    </div>
</div>

<script src="script.js"></script>
</body>
</html>
```
## CSS
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

body {
    background-image: url("todo1.jpg");
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center ;
}   

.container {
    width: 400px;
    background: white;
    padding: 25px;
    border-radius: 15px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.2);}
h1 {
    text-align: center;
    margin-bottom: 20px;
    color: #333;
}

.todo-input {
    display: flex;
    gap: 10px;
    margin-bottom: 20px;
}

.todo-input input {
    flex: 1;
    padding: 10px;
    border: 2px solid #4facfe;
        border-radius: 8px;
}

.todo-input button,
.buttons button {
    padding: 10px 15px;
    border: none;
    background: #4facfe;
    color: white;
    border-radius: 8px;
    cursor: pointer;
    transition: 0.3s;
}

.todo-input button:hover,
.buttons button:hover {
    background: #0077ff;
}

ul {
    list-style: none;
}
li {
    background: #f1f1f1;
    margin-bottom: 10px;
    padding: 10px;
    border-radius: 8px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.completed {
    text-decoration: line-through;
    color: gray;
}

.task-buttons button {
    margin-left: 5px;
    padding: 5px 10px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

.complete-btn {
    background: green;
    color: white;
}

.delete-btn {
    background: red;
    color: white;
}
```
## Javascript
```javascript

let taskList = document.getElementById("taskList");

function addTask() {
    let taskInput = document.getElementById("taskInput");
    let taskText = taskInput.value.trim();

    if (taskText === "") {
        alert("Please enter a task");
        return;
    }

    let li = document.createElement("li");

    let span = document.createElement("span");
    span.textContent = taskText;

    let buttonDiv = document.createElement("div");
    buttonDiv.classList.add("task-buttons");

    let completeBtn = document.createElement("button");
    completeBtn.textContent = "Done";
    completeBtn.classList.add("complete-btn");

    completeBtn.onclick = function() {
        span.classList.toggle("completed");
    };

    let deleteBtn = document.createElement("button");
    deleteBtn.textContent = "Delete";
    deleteBtn.classList.add("delete-btn");

    deleteBtn.onclick = function() {
        li.remove();
    };

    buttonDiv.appendChild(completeBtn);
    buttonDiv.appendChild(deleteBtn);

    li.appendChild(span);
    li.appendChild(buttonDiv);

    taskList.appendChild(li);

    taskInput.value = "";
}

function clearTasks() {
    taskList.innerHTML = "";
}

```

## OUTPUT
<img width="1365" height="633" alt="image" src="https://github.com/user-attachments/assets/8c494b75-c6a7-42d8-a1f4-45698714431a" />


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
