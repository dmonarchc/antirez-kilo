# antirez-kilo

A small, minimalistic text editor written in C, based on [Build Your Own Text Editor](https://viewsourcecode.org/snaptoken/kilo/). This project is a faithful implementation of the `kilo` editor originally created by [Salvatore Sanfilippo](https://github.com/antirez/kilo), but developed from scratch as part of a learning experience.

## 📜 About

This editor is built line-by-line following the guide by [snaptoken](https://viewsourcecode.org/snaptoken/kilo/). It introduces core text editor features such as:

- Raw mode terminal handling
- Text buffer and cursor movement
- Scrolling and screen rendering
- Syntax highlighting
- Saving to file
- Searching text
- Efficient redrawing using escape sequences

## 🔧 Features

| Feature              | Status   |
|----------------------|----------|
| Basic editing        | ✅ Done   |
| File loading/saving  | ✅ Done   |
| Scrolling            | ✅ Done   |
| Syntax highlighting  | ✅ Done   |
| Search functionality | ✅ Done   |
| Raw mode terminal    | ✅ Done   |
| Line numbering       | ✅ Done   |
| Status bar           | ✅ Done   |
| Keyboard shortcuts   | ✅ Done   |

> This implementation aims to be readable and modular, ideal for learning purposes or extending further.

## 🚀 Getting Started

### Requirements

- GCC or Clang (tested with GCC)
- Unix-like OS (Linux, macOS, WSL, etc.)
- Make (optional)

### Compilation

You can compile manually:

```bash
gcc -o kilo kilo.c -Wall -Wextra -pedantic -std=c99
```

Or use the provided `Makefile`:

```bash
make
```

### Running

```bash
./kilo filename.txt
```

If the file doesn’t exist, it will be created upon saving.

### Exiting

Press `Ctrl-Q` to quit. If there are unsaved changes, the program will prompt for confirmation.

## ⌨️ Keyboard Shortcuts

| Shortcut     | Action                     |
|--------------|----------------------------|
| `Ctrl-Q`     | Quit the editor            |
| `Ctrl-S`     | Save the file              |
| Arrow Keys   | Move the cursor            |
| `Page Up/Down` | Scroll faster           |
| `Home/End`   | Jump to beginning/end      |
| `Ctrl-F`     | Search within the file     |
| `Ctrl-H`     | Backspace (delete left)    |
| `Enter`      | Insert new line            |
| `Backspace`  | Delete character           |

## 🧪 Testing

Manual testing is currently in use. Here's how you can verify behavior:

1. **Startup Test:**

   ```bash
   ./kilo testfile.txt
   ```

   Confirm the terminal switches to raw mode and displays a status bar.

2. **Edit & Save Test:**

   - Type some text.
   - Press `Ctrl-S`.
   - Confirm `testfile.txt` is created or updated.

3. **Search Test:**

   - Press `Ctrl-F` and type a keyword.
   - Confirm the match is highlighted and navigation is possible.

4. **Syntax Highlighting Test:**

   - Open a `.c` or `.h` file.
   - Confirm that syntax is colorized properly.

> Note: A future enhancement will add unit tests and CI with GitHub Actions.

## 🗂️ Project Structure

```
.
├── kilo.c           # Main source file
├── kilo.h           # Header definitions (optional if split)
├── Makefile         # For building the project
└── README.md        # This file
```

## 📚 Reference

- [Build Your Own Text Editor](https://viewsourcecode.org/snaptoken/kilo/)
- [antirez/kilo](https://github.com/antirez/kilo)

## 🧠 Author

- [@dmonarchc](https://github.com/dmonarchc)

## 📜 License

MIT License — see [LICENSE](LICENSE) file for details.

