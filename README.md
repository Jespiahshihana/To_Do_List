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
  <link rel="stylesheet" href="index.css">
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
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  background: linear-gradient(135deg, #975c86 0%, #742952 100%);
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.todo-container {
  background: #ffffff;
  padding: 30px 40px;
  border-radius: 15px;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
  width: 400px;
  text-align: center;
}

h1 {
  font-size: 24px;
  margin-bottom: 20px;
  color: #333;
}

.input-section {
  display: flex;
  justify-content: center;
  gap: 10px;
}

#taskInput {
  flex: 1;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 8px;
  font-size: 14px;
}

#addBtn {
  padding: 10px 15px;
  background: #9e358e;
  color: #fff;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: background 0.3s ease;
}

#addBtn:hover {
  background: #de70c1;
}

ul {
  list-style-type: none;
  padding: 0;
  margin-top: 25px;
}

li {
  padding: 12px;
  background: #f9f9f9;
  margin-bottom: 10px;
  border-radius: 8px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  transition: transform 0.2s ease;
}

li:hover {
  transform: scale(1.02);
}

li.completed {
  text-decoration: line-through;
  color: gray;
  background: #e8e8e8;
}

button.delete {
  background: #4b183c;
  border: none;
  color: white;
  padding: 5px 8px;
  border-radius: 5px;
  cursor: pointer;
  font-size: 12px;
  transition: background 0.3s ease;
}

button.delete:hover {
  background: #7e3570;
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
<img width="1689" height="794" alt="image" src="https://github.com/user-attachments/assets/ffcdf760-f7f4-4cf4-bac5-b06b03d83ebe" />


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
