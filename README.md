# ToDoList #

This is a simple, interactive To Do List application created using HTML, CSS and JavaScript. It allows users to add tasks, strike them through when completed and delete tasks from the list. The application also displays the current date and time at the top.

## Features

* **Task management:** Add, complete (strike through) and remove tasks;
* **Dynamic Date and Time:** The current date and time is displayed and updated in real-time;
* **Responsive Interface:** Styled with CSS for a visually appealing and user-friendly experience;
* **Responsive Interface:** Styled with CSS for visually appealing and user-friendly experience;
* **Interactive UI:** Tasks can be marked as completed by clicking on them and individual tasks can be removed.

## Technologies Used

* **HTML:** Structure of the To-Do List and layout of the application;
* **CSS:** Styling for a clean and modern UI;
* **JavaScript:** Functionality for adding, removing and completing tasks along with displkaying the current date and time.

## How to use

1. Add a new task:
   * Type the task in the input box at the top of the page.
   * Click on the "Add" button to add it to the list.
2. Mark a task as complete:
   * Click on a task to toggle its completition. A strikethrough effect will appear and the background color will change.
3. Delete a task:
   * Click the "X" button next to a task to remove it from the list.
4. View Date and Time
   * The current date and time will be displayed at the top of the page and updated every second.
  
## Code explanation
**HTML**
The HTML file defines the structure of the to-do list app. It includes:
  * A header with the current date and time and an input field to add tasks;
  * A list <ul> to display the tasks;
  * A footer with credits.
  ```HTML
  <header>
  <div id="myDIV" class="head">
    <div id="datetime"></div>
    <h2 class="title">To Do List</h2>
    <input type="text" id="myInput" placeholder="Task" autocomplete="off">
    <span onclick="newElement()" class="addBtn">Add</span>
  </div>
  </header>
  ```
**CSS**
The CSS file is used to style the application:
  * It defines the layout of the input field, task list and buttons.
  * Includes hover effects, checked styles for completed tasks and date-time formatting.
  ```CSS
  ul li.checked {
    background: #FF6969;
    text-decoration: line-through;
  }
  ```
**JavaScript**
The JavaScript file controls the interactive functionality:
  * It allows tasks to be added to the list, removed and toggled as completed.
  * It also handles the real-time update of the current date and time.
  ```JavaScript
  function newElement() {
    var li = document.createElement("li");
    var inputValue = document.getElementById("myInput").value;
    var t = document.createTextNode(inputValue);
    li.appendChild(t);
    if (inputValue === '') {
      alert("You must write something!");
    } else {
      document.getElementById("myUL").appendChild(li);
    }
    document.getElementById("myInput").value = "";
  }
  ```

## File structure
/To-Do-List <br>
│  <br>
├── index.html <br>      
├── style.css <br>       
├── script.js <br>       
└── README.md <br>       
