## Emacs

### **Learning objectives:**

### What is Emacs?
- Extensible, customizable, self-documenting, real-time editor

### Who is Richard Stallman
- `R.S` is a free software movement activists who launched `GNU project`, developed `GNU Emacs` and wrote `GNU General Public License`

### How to open and save files
- **`C-x C-f`**		find file
- **`C-x C-s`**		save file
- **`M-x recover-this-file`**	auto save

### What is a buffer and how to switch from one to the other
- A buffer is an object that a file’s text is held in
- **`C-x C-b`**		lists all buffers
- To switch between buffers **`C-x C-f`** to find the new file
- **`C-x b`**			allows to find a buffer
- **`C-X 2`**			create two windows
- **`C-x o`**			moves from one window to another

### How to use the mark and the point to set the region
- Mark is a previous cursor position
- **`C-SPC`**			Set mark to current location
- **`C-x	C-x`**		Swap point and mark
- **`C-u	C-SPC`**		cycle through 16 mark rings
- Mark and point together delineate a region

### How to cut and paste lines and regions
- **`C-k	M-k`**		kill until the end of line/sentence
- **`C-y`**			yank (paste)
- **`M-y`**			yanks back earlier kills of text
- **`M-d`**			kill next word
- **`M-k`**			kill to end of sentence

### How to search forward and backward
- **`C-s	C-r`**		forward / reverse search
- **`M %`**			query replace
- **`C M s`**			regex search

### How to invoke commands by name
- **`M-x name`**		invokes a command by its name

### How to undo
- **`C-/	C-_	C-x u`**	undo

### How to cancel half-entered commands
- **`C-g`**			stop safely

### How to quit Emacs
- **`C-x C-c`**		exit 
- **`C-z`**			exit Emacs temporarily

### Insert and Delete
- **`C-k	M-k`**		kill until the end of line/sentence
- **`C-y`**			yank (paste)
- **`M-y`**			yanks back earlier kills of text

### Important Move-Around Commands
- **`C-f`**			forward one character
- **`C-b`**			backward one character
- **`M-f`**			forward one word
- **`i`**			insert into file
- **`C-n`**			move next line
- **`C-p`**			move previous line
- **`C-a`**			move beginning of line
- **`C-e`**			move end of line
- **`M-a`**			move beginning of sentence
- **`M-e`**			move end of sentence
- **`C-x 1`**			leave only one window