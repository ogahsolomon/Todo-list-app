# My Todo List 📝

A modern, minimal to-do app in a single HTML file. No frameworks, no build step.

## Features

- **Pill composer** — type and click the purple **+** (works great on touch devices, no Enter key needed)
- **Circle checkboxes** — checking a task strikes it through and auto-archives it after 800 ms
- **Undo toast** — archive/delete actions show a 5-second undo bar at the bottom
- **Notes** — each task can have a note (📝 button, or click a note preview to expand it)
- **Timestamps** — every task shows a faint "Created …" / "Edited …" subscript (hover for exact dates)
- **Quick edit** — double-click a title to rename it (or use the ✏️ button)
- **Drag to reorder** — grab any active task and drop it where you want
- **Filters** — All / Active / Done
- **Archive** — collapsible section (closed by default); restore with ↩, delete permanently with 🗑
- **Persistence** — everything is saved in your browser's localStorage
- **Dark mode** — 🌙 button in the header; your choice is remembered, and first-time visitors get their system preference automatically

## Design

- Inter font for text, **Fraunces** serif for the large display heading
- Light (`#f6f7fb`) and dark (`#12131a`) themes, 480px card with 24px rounded corners
- Purple accent `#7c5cff`, soft shadows, subtle animations
- All colors are CSS variables in `:root` / `:root[data-theme="dark"]` — easy to re-theme

## Try it

Open `index.html` in any browser. That's it.

## Code tour (index.html)

1. **HTML** — the card: composer, filters, active list, collapsible archive, undo toast
2. **CSS** — design tokens in `:root`, then one block per component
3. **JavaScript** — a single `todos` array is the source of truth
   (`{ id, title, note, done, archived, createdAt }`). Every button mutates the
   data, saves to localStorage, and calls `render()` to rebuild the lists.
