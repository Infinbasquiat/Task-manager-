# Task-manager-
A Full-featured desktop task manager with a modern dark-themed GUI built using Pythons built-in tkinter library 
# 🗂️ Python Task Manager

A modern, fully featured desktop task manager built entirely with Python's built-in `tkinter` library. No pip installs, no external packages — just Python.

![Python](https://img.shields.io/badge/Python-3.7%2B-blue?logo=python&logoColor=white)
![tkinter](https://img.shields.io/badge/GUI-tkinter-informational)
![License](https://img.shields.io/badge/License-MIT-green)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey)

---

## 📸 Overview

A dark-themed task manager with a sidebar, live search, sortable table, and a clean add/edit dialog — all built with zero dependencies.

---

## ✨ Features

- ➕ **Add, edit, and delete tasks** via a polished popup dialog
- 🔴🟡🟢 **Priority levels** — High, Medium, Low with color-coded rows
- 📅 **Due date tracking** — overdue tasks are highlighted in red automatically
- ✅ **Toggle complete / incomplete** with one click
- 🔍 **Live search** — filters your task list as you type
- 📋 **Sidebar navigation** — filter by All, Pending, Completed, High, Medium, Low
- 📊 **Live summary panel** — shows total, pending, done, and overdue counts at a glance
- 🗃️ **Sortable columns** — click any table header to sort
- 💾 **Auto-save** — all tasks saved instantly to `tasks.json`
- 🖱️ **Double-click** any row to open the edit dialog
- ⌨️ `Delete` key removes a selected task

---

## 🖥️ Requirements

- Python **3.7 or higher**
- `tkinter` — ships with Python by default on Windows and macOS

**Linux users only** — if you get `ModuleNotFoundError: No module named 'tkinter'`, run:

```bash
sudo apt install python3-tk
```

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/python-task-manager.git
cd python-task-manager
```

### 2. Run the app

```bash
python task_manager_gui.py
```

The GUI window will open immediately. No setup, no installs.

---

## 📁 Project Structure

```
python-task-manager/
├── task_manager_gui.py   # Full application — all UI and logic
├── tasks.json            # Auto-generated data file (created on first run)
├── .gitignore
├── LICENSE
└── README.md
```

---

## 🗄️ Data Format

Tasks are stored locally in `tasks.json`, created automatically when you add your first task:

```json
[
  {
    "id": 1,
    "title": "Finish project report",
    "description": "Include charts and summary section",
    "priority": "High",
    "due_date": "2026-03-01",
    "completed": false,
    "created_at": "2026-02-26 10:30"
  }
]
```

---

## 🏗️ Architecture

| Component | Description |
|---|---|
| `TaskManagerApp` | Main `tk.Tk` window — sidebar, header, table, status bar |
| `TaskDialog` | `tk.Toplevel` popup for adding and editing tasks |
| `load_tasks()` | Reads `tasks.json` on startup |
| `save_tasks()` | Writes to `tasks.json` after every change |
| `_refresh()` | Re-renders the table based on active filter + search query |

---

## ⌨️ Keyboard Shortcuts

| Key | Action |
|---|---|
| `Double-click` row | Open edit dialog |
| `Delete` | Delete selected task |
| `Enter` (in dialog) | Save task |
| `Escape` (in dialog) | Cancel |

---

## 🛠️ Built With

- [`tkinter`](https://docs.python.org/3/library/tkinter.html) — GUI framework (Python standard library)
- [`ttk`](https://docs.python.org/3/library/tkinter.ttk.html) — Themed widgets for the table
- [`json`](https://docs.python.org/3/library/json.html) — Data persistence
- [`datetime`](https://docs.python.org/3/library/datetime.html) — Due date handling and overdue detection

---

## 📄 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

## 🙋 Author

Built as a personal project to explore desktop GUI development in Python using only the standard library.

> Feel free to fork, star ⭐, and build on top of this!
