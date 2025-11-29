NVIM DUNGEON DELVER RPG
=======================

A persistent text-based RPG for learning nvim keybindings, designed to run
inside Claude Code within a terminal inside nvim.

PLAYER PREFERENCES
------------------
Screen size:       150 chars wide x 40 lines tall (max)
Lesson size:       2-4 commands per lesson (small chunks)
Lesson names:      Two words each (e.g., "Cardinal Movement", "Line Find")
Timezone:          Asia/Vientiane (ICT, UTC+7)
                   Don't run time commands - use system time, convert to +07
File format:       ASCII tables, TSV for logs

NVIM SETUP
----------
Platform:          Chromebook Crostini (Linux container)
Terminal:          :terminal (opens Claude Code)
File tree:         None yet (use built-in :Explore or add plugin later)

SAFETY RULE
-----------
Always teach "how to get back" BEFORE teaching new navigation.
Never leave user stranded away from Claude Code terminal.

SCORING PROTOCOL
----------------
Wrong answer:      Retry with NEW exercise before moving on
                   Interval drops one level (15m -> 5m)
Right answer:      Interval increases one level (5m -> 15m)
Interval levels:   5m -> 15m -> 45m -> 135m -> 405m -> MASTERED

SPACED REPETITION
-----------------
AUTO - Claude prompts reviews without asking
Reviews due when: current_time > last_reviewed + interval
Skip MASTERED skills

STATE UPDATE RULE
-----------------
Batch all state.tsv edits into a single update. List all changes first,
then apply them in one Edit tool call (not multiple calls per line).

FILE ROLES
----------
state.tsv         TSV logs:
                  - Lesson log (lesson_num, lesson_name, score, datetime, interval_before)
                  - Review schedule (lesson_num, lesson_name, last_reviewed, interval)

curriculum.txt    Static reference:
                  - Lesson plan (all floors, numbered lessons, two-word names)
                  - Inventory (mastered skills)

README.md         This file - rules and player preferences

GAME MECHANICS
--------------
Dungeon:   Rooms contain nvim puzzles. Solve with correct commands.
Character: HP (lost on mistakes), XP (gained on learning)
Floors:    1=movement, 2=operators, 3=search, 4=windows, 5+=advanced

STARTING/RESUMING
-----------------
Say: "Let's play the nvim dungeon" or "Resume my nvim RPG"
Claude reads state.tsv and curriculum.txt, continues from where you left off.
