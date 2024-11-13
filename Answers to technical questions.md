1) How long did you spend on the coding test?
Ans: It took me approximately 3 hours to work on both the HTML and CSS, with CSS taking a bit more time due to planning and selecting the theme, colors, and overall design.
I spent about one and a half hours on the JavaScript part, including implementing localStorage to save task data across sessions and other functionalities.
Finally, I took an additional hour to refine the design, making it look visually appealing and user-friendly. In total, it took me around 6 hours.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

 2)What was the most useful feature that was added to the latest version of your chosen language? Please include a snippet of code that shows how you've used it.
Ans: I think the most useful feature added to JavaScript in recent versions is the localStorage API.
This feature allows web applications to store data on the client side, persisting it even after the page is refreshed or the browser is closed.

here's my code snippet:
let tasks = JSON.parse(localStorage.getItem('tasks')) || [];
function addTask() {
    const title = document.getElementById('title').value;
    const description = document.getElementById('description').value;
    const dueDate = document.getElementById('dueDate').value;
    const priority = document.getElementById('priority').value;
    if (title && dueDate && priority) {
        const newTask = { title, description, dueDate, priority, completed: false };
        tasks.push(newTask); 
        localStorage.setItem('tasks', JSON.stringify(tasks)); 
        displayTasks();
    }
}
function updatePriority(index, newPriority) {
    tasks[index].priority = newPriority;
    localStorage.setItem('tasks', JSON.stringify(tasks));
    displayTasks(); 
}
function deleteTask(index) {
    tasks.splice(index, 1); 
    localStorage.setItem('tasks', JSON.stringify(tasks));
    displayTasks();
}
function toggleComplete(index) {
    tasks[index].completed = !tasks[index].completed;
    localStorage.setItem('tasks', JSON.stringify(tasks));
    displayTasks();
}

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

 3)How would you track down a performance issue in production? Have you ever had to do this?
Ans: I have not yet had the opportunity to track down a performance issue in a production environment.
But I would approach the task by Identifying Bottlenecks.
I can focus on areas of the application that are likely to cause performance issues, such as large images, heavy scripts. 
Using the Network tab in DevTools, I can pinpoint resources that take too long to load.
Or maybe Code Review and Optimization.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

4) If you had more time, what additional features or improvements would you consider adding to the task management application?
Ans: If i had more time, i think i would have tried to add some features like showing the tasks and how many of them are completed or how many of them are pending on a graph or chart, something visual.
I could have tried to make it Responsive, or I could use a signup/login feature for different users to access their work.
