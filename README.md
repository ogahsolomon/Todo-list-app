# My To-Do List 📝

A simple to-do app built with plain HTML, CSS, and JavaScript — all in one file.
Perfect for beginners: no installs, no build tools, just open and use.

## How to use it

- **Add a task** — type in the box and press **Add** (or the Enter key).
- **Check off a task** — click the **✓** button. Click again to uncheck.
- **Move a task** — use the **↑ / ↓** buttons to reorder items.
- **Archive a task** — click **📦**. It moves to the "Archived" section (hidden from the active list, but not deleted).
- **Restore** — click **↩** on an archived task to bring it back.
- **Delete forever** — click **🗑** on an archived task (asks for confirmation first).

Your tasks are saved in your browser automatically, so they're still there
the next time you open the page (as long as you use the same browser).

## How the code is organized (index.html)

1. **HTML** — the page skeleton: an input box, an "Active" list, and an "Archived" list.
2. **CSS** (inside `<style>`) — all the colors, spacing, and layout.
3. **JavaScript** (inside `<script>`) — the app logic:
   - `todos` — the list of task data (each task has an id, text, done, archived)
   - `render()` — redraws the screen from the data after every change
   - helper functions: `addTodo`, `toggleDone`, `move`, `toggleArchive`, `deleteTodo`

The main idea to learn from: the **data** (`todos`) is the source of truth,
and the screen is just a picture of that data. Every button changes the data,
then calls `render()` to update the picture.
