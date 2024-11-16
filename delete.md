Sure! Here is the code with comments explaining the flow and steps:

```jsx
import React, { useState } from 'react';

// Step 1: TaskManager Component (Parent Component)
// Yeh component task list ko manage karega aur task state ko store karega
const TaskManager = () => {
  // Step 2: Task state ko initialize kar rahe hain
  const [tasks, setTasks] = useState([]);  // tasks array ko store kar rahe hain, initially empty hai

  // Step 3: Function to add a new task
  const addTask = (taskName) => {
    // Naye task ko add kar rahe hain with a unique id (using Date.now()), initial completion status false
    setTasks([...tasks, { id: Date.now(), name: taskName, completed: false }]);
  };

  // Step 4: Function to toggle task completion
  const toggleTaskCompletion = (taskId) => {
    // Tasks ko map kar rahe hain aur task ke completion status ko toggle kar rahe hain (True to False or vice versa)
    const updatedTasks = tasks.map((task) =>
      task.id === taskId ? { ...task, completed: !task.completed } : task
    );
    setTasks(updatedTasks);  // Updated task list ko state mein update kar rahe hain
  };

  // Step 5: Function to delete a task
  const deleteTask = (taskId) => {
    // Task ko filter kar rahe hain aur us task ko remove kar rahe hain jiska ID delete karna hai
    const updatedTasks = tasks.filter((task) => task.id !== taskId);
    setTasks(updatedTasks);  // Updated task list ko state mein set kar rahe hain
  };

  // Step 6: Returning the UI for Task Manager
  return (
    <div>
      <h1>Task Manager</h1>
      {/* Step 7: AddTask component ko onAdd function pass kar rahe hain */}
      <AddTask onAdd={addTask} />
      {/* Step 8: TaskList component ko tasks, toggle completion aur delete function pass kar rahe hain */}
      <TaskList
        tasks={tasks}
        onToggleCompletion={toggleTaskCompletion}
        onDelete={deleteTask}
      />
    </div>
  );
};

// Step 9: AddTask Component (Child Component)
// Yeh component user ko task add karne ka option deta hai
const AddTask = ({ onAdd }) => {
  // Step 10: Task name state ko initialize kar rahe hain
  const [taskName, setTaskName] = useState("");

  // Step 11: Form submit karte waqt handleSubmit function call hoga
  const handleSubmit = (e) => {
    e.preventDefault();  // Step 12: Default form submit behavior ko rok rahe hain
    if (taskName.trim()) {
      // Step 13: Agar task name empty nahi hai, toh parent component ke onAdd function ko call kar rahe hain
      onAdd(taskName);
      setTaskName("");  // Step 14: Task add karne ke baad input field ko clear kar rahe hain
    }
  };

  return (
    <form onSubmit={handleSubmit}>
      {/* Step 15: Input field ko bind kar rahe hain taskName state ke saath */}
      <input
        type="text"
        value={taskName}
        onChange={(e) => setTaskName(e.target.value)}  // Step 16: Jab input change hoga, taskName state update hoga
        placeholder="Enter task"
      />
      <button type="submit">Add Task</button>
    </form>
  );
};

// Step 17: TaskList Component (Child Component)
// Yeh component task list ko display karne ka kaam karta hai
const TaskList = ({ tasks, onToggleCompletion, onDelete }) => {
  return (
    <ul>
      {/* Step 18: Tasks ko map kar rahe hain aur har task ke liye TaskItem component render kar rahe hain */}
      {tasks.map((task) => (
        <TaskItem
          key={task.id}
          task={task}
          onToggle={onToggleCompletion}  // Step 19: TaskItem ko onToggle function pass kar rahe hain
          onDelete={onDelete}  // Step 20: TaskItem ko onDelete function pass kar rahe hain
        />
      ))}
    </ul>
  );
};

// Step 21: TaskItem Component (Child Component)
// Yeh component ek individual task ko render karta hai
const TaskItem = ({ task, onToggle, onDelete }) => {
  return (
    <li style={{ textDecoration: task.completed ? "line-through" : "none" }}>
      {/* Step 22: Checkbox ko bind kar rahe hain task ke completion status ke saath */}
      <input
        type="checkbox"
        checked={task.completed}
        onChange={() => onToggle(task.id)}  // Step 23: Checkbox click karne par onToggle function call hoga
      />
      {task.name}  {/* Step 24: Task ka name display kar rahe hain */}
      {/* Step 25: Delete button ko add kar rahe hain jisse task delete hoga */}
      <button onClick={() => onDelete(task.id)}>Delete</button>
    </li>
  );
};

export default TaskManager;
```

### Code Flow:

1. **TaskManager** is the parent component where the main task list (`tasks`) is managed using the `useState` hook.
2. **addTask** function adds a new task to the `tasks` array with a unique ID, name, and completion status.
3. **toggleTaskCompletion** toggles the task’s `completed` status when the checkbox is clicked.
4. **deleteTask** deletes the task from the `tasks` array based on the task's ID.
5. The **AddTask** component takes user input and calls the `addTask` function to add a new task.
6. The **TaskList** component maps through the `tasks` array and renders each task using the **TaskItem** component.
7. Each **TaskItem** component shows a checkbox for completion, task name, and a delete button.
8. The **onToggle** and **onDelete** functions are passed down to handle task completion and deletion.

Let me know if you need further clarification!
