# Ex03 To-Do List using JavaScript
## Date: 15-09-2025

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
### HTML
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To-Do List App</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="todo-container">
    <h1>My To-Do List</h1>
    <div class="input-section">
      <input type="text" id="taskInput" placeholder="Enter a new task...">
      <button id="addBtn">Add</button>
    </div>
    <ul id="taskList"></ul>
  </div>
  <script src="script.js"></script>
</body>
</html>
```
### CSS
```
body {
  font-family: Arial, sans-serif;
  background: #f4f4f4;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.todo-container {
  background: #fff;
  padding: 20px 30px;
  border-radius: 10px;
  box-shadow: 0px 4px 6px rgba(0,0,0,0.2);
  width: 350px;
}

h1 {
  text-align: center;
  color: #333;
}

.input-section {
  display: flex;
  justify-content: space-between;
}

#taskInput {
  width: 70%;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

#addBtn {
  padding: 8px 12px;
  background: #28a745;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

#addBtn:hover {
  background: #218838;
}

ul {
  list-style-type: none;
  padding: 0;
  margin-top: 20px;
}

li {
  padding: 10px;
  background: #f9f9f9;
  margin-bottom: 8px;
  border-radius: 5px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

li.completed {
  text-decoration: line-through;
  color: gray;
}

button.delete {
  background: red;
  border: none;
  color: white;
  padding: 5px 8px;
  border-radius: 5px;
  cursor: pointer;
}

```
### JS
```
document.getElementById("addBtn").addEventListener("click", addTask);

function addTask() {
  let taskInput = document.getElementById("taskInput");
  let taskText = taskInput.value.trim();

  if (taskText === "") {
    alert("Please enter a task!");
    return;
  }

  let li = document.createElement("li");
  li.textContent = taskText;

  li.addEventListener("click", () => {
    li.classList.toggle("completed");
  });

  let delBtn = document.createElement("button");
  delBtn.textContent = "X";
  delBtn.className = "delete";
  delBtn.addEventListener("click", (e) => {
    e.stopPropagation(); 
    li.remove();
  });

  li.appendChild(delBtn);
  document.getElementById("taskList").appendChild(li);

  taskInput.value = ""; 
}
```

## OUTPUT


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
