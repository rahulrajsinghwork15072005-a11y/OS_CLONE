# WebOS XP  
**A fully interactive Windows XP‑style desktop environment in the browser — pure HTML, CSS & vanilla JavaScript.**  
Boot up, log in, launch apps, play games, and manage files — all inside a nostalgic Y2K operating system that runs in a single file.

---

## 🎯 Overview

|                      |                                                              |
|----------------------|--------------------------------------------------------------|
| **Type**             | Browser‑based operating system simulation / portfolio        |
| **Platform**         | Web browser (Chrome, Firefox, Edge, Safari)                  |
| **Technology**       | HTML5, CSS3, vanilla JavaScript – no frameworks              |
| **Controls**         | Mouse & keyboard (drag, double‑click, keyboard shortcuts)    |
| **License**          | Personal portfolio & educational use                         |

---

## ✨ Features

### 🖥️ Desktop Experience
- **Boot sequence** – animated terminal with fake BIOS output and CLI
- **Login system** – authenticate as `rahul/rahul` or `guest/guest`
- **Authentic XP aesthetic** – teal taskbar, blue title bars, classic start menu, Bliss‑style wallpaper, system tray with clock
- **Draggable & resizable windows** – minimize, maximize, close; active/inactive title bar states
- **Desktop icons** – double‑click to open apps; right‑click context menu; custom icon creator
- **Taskbar buttons** – switch between open windows; minimize/restore
- **Start menu** – full program launcher with quick access to all apps, places, and settings
- **Lock screen** – password protection to lock the desktop

### 🎮 Built‑in Applications (15+)
| App              | Description                                                    |
|------------------|----------------------------------------------------------------|
| 📁 File Explorer  | Virtual file system (Desktop, Documents, Downloads); local folder access via File System Access API |
| 📝 Notepad        | Rich text editor with save/open to virtual FS, font selection, find & replace, word wrap, export |
| 💻 Terminal       | Full command‑line with 70+ commands, Harry Potter spells, Linux‑style utilities, easter eggs, and app launching |
| 🎨 Paint          | Canvas drawing with pen, brush, shapes, fill bucket, color picker, save as PNG |
| 🎵 Media Player   | Audio player with playlist, progress bar, volume control, play/pause/stop |
| 🖼️ Image Gallery  | Image viewer with slideshow, thumbnails, previous/next navigation |
| 📽️ Video Player   | Play local video files or playlist; progress bar, volume, playback controls |
| 🔢 Calculator     | Scientific calculator with memory, trig functions, logarithms, constants, and history |
| 📅 Calendar       | Monthly view with event add/delete (localStorage persistence) |
| 🎮 Game Hub       | 9 classic games: Snake, Tetris, Minesweeper, Memory Match, Tic‑Tac‑Toe, Flappy Bird, Pong, Wordle, 2048 |
| 📌 Sticky Notes   | Multi‑note manager with auto‑save and individual note windows |
| 🌐 Web Browser    | Retro‑styled homepage with bookmarks; opens URLs in new tab |
| 📄 Resume         | Inline resume with skills, experience, and projects; one‑click PDF download |
| 💡 Projects       | Portfolio showcase of 10 projects with live demo & GitHub links |
| ✍️ Blog           | Simple blog reader with local posts |
| ✉️ Contact        | Direct links to email, phone, LinkedIn, GitHub, and website |
| 🗑️ Recycle Bin    | Deleted items from virtual FS can be restored or permanently removed |
| ℹ️ System Info    | Simulated OS details with live CPU/RAM usage, IP, MAC, disk stats |

### 🎨 Theming & Customization
- **Wallpaper picker** – choose from XP Classic, Bliss, Azure Night, Y2K Vibes, Dark Matter, Sunset
- **Dark/Light mode toggle** – switches the entire desktop palette
- **Custom desktop icons** – create your own icons with emoji, name, color, and embedded content
- **Icon arrangement** – auto‑align all desktop icons

### 🧠 Technical Magic
- **Virtual file system** – fully persisted in `localStorage`; create, rename, delete files and folders
- **Window manager** – z‑index ordering, active/inactive states, minimize/restore animations
- **Drag & drop** – icons and windows can be moved anywhere; windows are resizable
- **Context menus** – right‑click on desktop, icons, or files for actions
- **Keyboard shortcuts** – `Ctrl+N` to open Notepad, `S` to open search, `Delete` to remove, arrow keys in games, etc.
- **Session persistence** – custom icons and calendar events survive reloads
- **Easter egg terminal** – 70+ commands including `cowsay`, `matrix`, `neofetch`, `sudo`, `konami`, `accio`, `expecto patronum`, `42`, and many more

### 🕹️ Games (all built from scratch)
| Game           | Description                                  |
|----------------|----------------------------------------------|
| Snake          | Classic snake with power‑ups and high score  |
| Tetris         | Full tetris with line clears and scoring     |
| Minesweeper    | 8×8 grid with 10 mines, timer and flags      |
| Memory Match   | Emoji card matching game with move counter   |
| Tic‑Tac‑Toe    | Play against AI (easy/medium/hard)           |
| Flappy Bird    | Flappy Bird clone with gravity and pipes     |
| Pong           | Two‑player Pong vs AI                        |
| Wordle         | 5‑letter word guessing with color feedback   |
| 2048           | Sliding tile puzzle                          |

---

## 🚀 How to Run

1. **Download or clone** the repository.
2. Open the single `a.html` (or `index.html`) file in any modern browser.
3. The boot sequence starts automatically. Wait for it, then type `startx` when prompted, or simply wait for the login screen.
4. Log in with:
   - **Username:** `rahul` / **Password:** `rahul` (or `guest`/`guest`)

> No build tools, npm, or server required — everything runs straight from the file system. (Font Awesome is loaded from CDN for icons.)

---

## 🎮 Usage

- **Desktop** – double‑click any icon to launch an app; right‑click for context menu.
- **Start menu** – click the green **Start** button, browse Programs, Places, and Settings.
- **Taskbar** – running apps appear as buttons; click to switch or minimize.
- **Terminal** – type `help` inside the terminal to see all available commands. Try `accio paint`, `lumos`, `matrix`, `neofetch`, `fortune`, or `cowsay hello`.
- **Games** – open Game Hub, select a game, and use keyboard (arrow keys, WASD) or mouse.
- **File Explorer** – manage your virtual files; supports local folder access via the modern File System Access API (where supported).
- **Lock / Unlock** – click the lock icon in the taskbar or press `Ctrl+L`.

---

## 🧠 Technical Highlights

### Architecture
- **Single‑file application** – all HTML, CSS, and JavaScript in one portable file.
- **Window manager** – custom window creation, Z‑index management, minimization, maximization, and drag/resize logic.
- **Virtual file system** – a nested object stored in `localStorage`; file operations (create, rename, delete) are mirrored across the UI.
- **Game loop** – all games use `requestAnimationFrame` or `setInterval` with delta‑time; Canvas API for rendering.
- **Terminal engine** – command parsing with history navigation, piping support, and dynamic command registration.
- **No frameworks** – everything is hand‑crafted; no React, Vue, or jQuery.

### Performance & Compatibility
- Efficient DOM manipulation: windows are created and destroyed on demand; event delegation is used where possible.
- Canvas‑based games and apps (Paint, Snake, Tetris) run smoothly at 60fps.
- Fully responsive: desktop adapts to screen size; folders arrange in a grid.
- Works offline after fonts are cached, but first load needs an internet connection for Font Awesome and Google Fonts (if any; fonts are embedded inline in the style block).

### Persistence
- User‑created desktop icons, calendar events, sticky notes, and the virtual file system are all saved to `localStorage`, surviving page reloads.
- High scores for Snake, 2048, and Tetris are preserved.

---

## 📁 File Structure

- **`a.html`** (or `index.html`) – the entire OS: HTML structure, CSS styling, and all JavaScript logic in one file.
- **`README.md`** – Documentation.

> No other files required.

---

## 🎨 Customization

You can tweak almost everything by editing the single file:

- **Credentials** – modify the `validUsers` array in the `<script>` block to change login accounts.
- **Wallpapers & themes** – add new wallpaper options in `wallpaperList` and extend the `applyWallpaper` function.
- **Terminal commands** – add new commands by extending the `handleCmd` function inside `openTerminal`.
- **Apps** – add a new icon by calling `createDesktopIcon` with the right configuration, then implement the app function (follow the pattern of `openPaint`, `openNotepad`, etc.).
- **Colors & spacing** – CSS custom properties are defined in the `<style>` block; easy to recolour the whole OS.

---

## 👤 Author

**Rahul Raj Singh**  
- GitHub: [https://github.com/rahulrajsinghwork15072005-a11y](https://github.com/rahulrajsinghwork15072005-a11y)  
- LinkedIn: [https://www.linkedin.com/in/rahul-raj-singh-57442a3b3/](https://www.linkedin.com/in/rahul-raj-singh-57442a3b3/)  
- Email: rahulrajsingh.work.15072005@gmail.com

---

## 🧾 License

This project is a portfolio piece, provided for educational and personal inspiration.  
Feel free to explore, modify, and share. No warranty.

**Have fun playing with your own browser‑based XP desktop! 🪟**  
