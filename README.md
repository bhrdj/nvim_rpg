# Nvim Dungeon Delver RPG

A persistent text-based RPG for learning nvim keybindings and commands, designed to run inside Claude Code within a terminal inside nvim.

## How It Works

This RPG teaches nvim skills through dungeon exploration. Each room, puzzle, or encounter is solved using actual nvim commands. The game state persists across Claude sessions via markdown files.

### Starting/Resuming a Game

When starting Claude, say something like:
- "Let's continue the nvim dungeon"
- "Resume my nvim RPG"
- "Read nvim_rpg/state01.md and continue the game"

Claude will read the state file(s) and resume from where you left off.

## File Roles

### `state01.md` (and `state02.md`, etc.)
- **Purpose**: Complete game history and current status
- **Contains**: Your location, inventory, HP, completed challenges, and full narrative log
- **Rotation**: When a state file exceeds ~11,000 characters, the older history gets summarized and moved to the next numbered file, keeping recent events intact

### `curriculum.md`
- **Purpose**: Learning tracker and reference
- **Contains**:
  - Skills you've mastered (with the nvim commands)
  - Skills queued for upcoming challenges
  - Detailed explanations you can read offline or print
- **Use**: Read ahead if you want to move faster, or review commands you've learned

### `README.md` (this file)
- **Purpose**: Explains the system mechanics
- **Contains**: How to start/resume, file purposes, game rules

## Game Mechanics

### The Dungeon
- Rooms contain nvim-themed puzzles and encounters
- Doors unlock with correct keybinding knowledge
- Monsters are defeated by executing the right commands
- Treasure chests contain new command knowledge

### Your Character
- **HP**: Health points, lost when you make mistakes
- **XP**: Experience gained by learning new commands
- **Inventory**: Commands you've mastered (can use freely)
- **Location**: Current room in the dungeon

### Challenges
Each challenge teaches a specific nvim concept:
- Movement (h/j/k/l, w/b/e, gg/G, etc.)
- Editing (i/a/o, d/c/y, p, etc.)
- Navigation (/, ?, *, #, etc.)
- Advanced (macros, marks, registers, etc.)

### Difficulty Progression
- **Floor 1**: Basic movement and insert mode
- **Floor 2**: Text objects and operators
- **Floor 3**: Search and navigation
- **Floor 4**: Windows and buffers
- **Floor 5+**: Advanced techniques

## Tips

1. **Practice in real nvim**: After learning a command in-game, try it in your actual nvim session
2. **Read ahead**: Check curriculum.md to preview upcoming skills
3. **Take notes**: The curriculum serves as your reference sheet
4. **Commit progress**: Optionally commit state files to preserve across machines

---

*Ready to delve? Just ask Claude to start or continue your adventure!*
