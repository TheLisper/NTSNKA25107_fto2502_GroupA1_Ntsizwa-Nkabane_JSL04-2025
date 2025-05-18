# JSL04 Project Brief: Dynamic Task Display & Modal View

## Overview

In this project,  display tasks from the **given initial data** on the DOM using JavaScript. Tasks should be placed into the correct **Kanban board columns** based on their status, and clicking a task should open a **modal** where users can view and modify task details. The project emphasizes **DOM manipulation, event handling, modular JavaScript structure, and responsive UI implementation.**

## Before You Begin

**Check the project user stories in your student dashboard and the updated Figma Design** before you start building.

## Figma Design Link

Check the updated Figma Design: [Figma Link](https://www.figma.com/design/y7bFCUYL5ZHfPeojACBXg2/Challenges-%7C-JSL?node-id=0-1&p=f&t=Ki0CZk0RAjrk9Fhs-0)

## Key Objectives

### Dynamic Task Display & Interaction

- Dynamically generate **task elements** from the given initial data and insert them into the DOM.
- Ensure tasks are placed in the **correct columns** ("To Do", "In Progress", "Done") based on their status.
- Clicking a task should **open a modal** displaying its details.
- The modal should include:
  - **Editable input fields** for the task title and description.
  - **A select dropdown** showing the current status with other status options available.
  - **A close button** that allows users to exit the modal easily.

### Design & Responsiveness

- Ensure the **modal matches the Figma design**, including a **backdrop effect** for focus.
- Implement a **fully responsive modal** that works on both desktop and mobile devices.

### Code Structure & Maintainability

- Structure JavaScript using **modular, single-responsibility functions**.
- Use **descriptive and meaningful variable and function names** for clarity.
- Add **JSDoc comments** to major functions, describing their purpose, parameters, and return values for better documentation.

## Expected Outcome

A fully functional **dynamic task board** where tasks appear under the correct columns, and users can **open a modal to view/edit** task details. The project will follow **clean, well-documented, and maintainable code practices**, ensuring a professional and scalable implementation.

# Kanban Task Board – Script.js Explanation

## Overview

The `script.js` file is the core of the Kanban Task Board project. It dynamically manages tasks, renders them into the correct columns, and provides a modal interface for viewing and editing task details. All DOM manipulation and event handling are performed through modular, well-commented JavaScript functions.

---

## How `script.js` Works

### 1. Initial Task Data

- The script defines an `initialTasks` array containing task objects.
- Each task has an `id`, `title`, `description`, and `status` (`todo`, `doing`, or `done`).

### 2. Rendering Tasks

- The `renderTasks(tasks)` function:
  - Clears all `.tasks-container` elements in the DOM.
  - Iterates through the `tasks` array and creates a task card for each task.
  - Appends each card to the correct column based on its `status`.
  - Updates the column headers to show the current count of tasks.

### 3. Modal Functionality

- Clicking a task card calls `openModal(taskId)`:
  - Dynamically creates a modal if it doesn't exist.
  - Populates the modal fields with the selected task's data.
  - Shows the modal with a backdrop effect.
  - Sets up event listeners to save changes when fields are edited.

- The modal allows users to:
  - Edit the task title and description.
  - Change the task status via a dropdown.
  - Close the modal with a button or by clicking the backdrop.

- Changes are saved back to the `initialTasks` array and the board is re-rendered.

### 4. Code Structure

- All major functions are modular and have a single responsibility:
  - `renderTasks(tasks)` – Renders all tasks.
  - `createModal()` – Creates the modal structure if needed.
  - `openModal(taskId)` – Opens and populates the modal for a specific task.
  - `saveModal()` – Saves changes from the modal to the task array.
  - `closeModal()` – Hides the modal and resets the state.

- Variable and function names are descriptive for clarity.
- Inline comments explain the purpose of each function and key logic.

---

## Usage

1. Open `index.html` in your browser.
2. Tasks are rendered dynamically into their columns.
3. Click any task to open the modal and edit its details.
4. Changes are saved automatically and reflected on the board.

---

## Key Points

- **No hardcoded tasks in HTML:** All tasks are rendered by JavaScript.
- **Fully interactive:** Edit, move, and update tasks in real time.
- **Responsive design:** Modal and board adapt to desktop and mobile screens.
- **Maintainable code:** Modular functions and clear comments for easy updates.

---

## Example: Opening and Editing a Task

When you click a task:
- `openModal(taskId)` is called.
- The modal appears with the task's current details.
- Edit the fields; changes are saved on blur or status change.
- The board updates to reflect your edits.

---

For more details, see the comments in `script.js`.
