# Nvim Dungeon Curriculum

Your learning journey through the dungeon. Commands you've mastered are in your inventory. Upcoming challenges preview what's ahead.

---

## Mastered Skills (Inventory)

*Empty - your adventure begins!*

---

## Current Floor: 1 - The Basics

### Queued Lessons

#### 1.1 The Cardinal Movements
The foundation of all nvim navigation.
```
h - move left one character
j - move down one line
k - move up one line
l - move right one character
```
**Why hjkl?** On the ADM-3A terminal where vi was created, these keys had arrows printed on them. Keeping your fingers on the home row is faster than reaching for arrow keys.

#### 1.2 Entering Insert Mode
To actually type text, you must enter insert mode.
```
i - insert before cursor
a - append after cursor
I - insert at beginning of line
A - append at end of line
```
**Escape** returns you to normal mode. In nvim, you can also use `Ctrl-[` or `Ctrl-c`.

#### 1.3 Saving and Quitting
Essential for not losing your work (or escaping the dungeon).
```
:w    - write (save) the file
:q    - quit (fails if unsaved changes)
:wq   - write and quit
:q!   - quit without saving (force)
ZZ    - write and quit (shortcut)
```

#### 1.4 Word Movement
Moving faster than one character at a time.
```
w - move to start of next word
b - move back to start of word
e - move to end of word
W/B/E - same but for WORDS (whitespace-delimited)
```

#### 1.5 Line Movement
Navigating within and between lines.
```
0  - move to first column of line
^  - move to first non-blank character
$  - move to end of line
gg - go to first line of file
G  - go to last line of file
5G - go to line 5 (or any number)
```

---

## Floor 2 - Operators and Text Objects (Preview)

#### 2.1 The Delete Operator
```
x  - delete character under cursor
dd - delete entire line
dw - delete to start of next word
d$ - delete to end of line
D  - delete to end of line (shortcut for d$)
```

#### 2.2 The Change Operator
```
cc - change entire line
cw - change word
c$ - change to end of line
C  - change to end of line (shortcut)
```

#### 2.3 Copy and Paste
```
yy - yank (copy) line
yw - yank word
p  - paste after cursor
P  - paste before cursor
```

#### 2.4 Text Objects
```
iw - inner word
aw - a word (includes surrounding space)
i" - inner quotes
a" - a quoted string (includes quotes)
i( - inner parentheses
a( - a parenthesized block
```

---

## Floor 3 - Search and Navigate (Preview)

#### 3.1 Searching
```
/pattern  - search forward
?pattern  - search backward
n         - next match
N         - previous match
*         - search for word under cursor (forward)
#         - search for word under cursor (backward)
```

#### 3.2 Find in Line
```
f{char} - find character forward in line
F{char} - find character backward in line
t{char} - till character (stop before it)
T{char} - till character backward
;       - repeat last f/F/t/T
,       - repeat last f/F/t/T in reverse
```

---

## Floor 4 - Windows and Buffers (Preview)

```
:split or :sp  - horizontal split
:vsplit or :vs - vertical split
Ctrl-w h/j/k/l - move between windows
:e filename    - edit file in current window
:bn / :bp      - next/previous buffer
:ls            - list buffers
```

---

## Floor 5+ - Advanced (Far Preview)

- Macros (q, @)
- Marks (m, ', `)
- Registers (", @)
- Visual mode (v, V, Ctrl-v)
- Substitution (:s, :g)
- Folding (zo, zc, zM, zR)
- And deeper mysteries...

---

## Quick Reference Card

Print this section for offline use:

### Movement
| Key | Action |
|-----|--------|
| h/j/k/l | left/down/up/right |
| w/b/e | word forward/back/end |
| 0/^/$ | line start/first-char/end |
| gg/G | file start/end |

### Editing
| Key | Action |
|-----|--------|
| i/a | insert/append |
| o/O | new line below/above |
| x/X | delete char forward/back |
| dd/yy/p | delete/yank/paste line |

### Commands
| Key | Action |
|-----|--------|
| :w | save |
| :q | quit |
| :wq | save and quit |
| u | undo |
| Ctrl-r | redo |
