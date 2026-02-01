# VI / VIM Cheat Sheet

*Built for operators. Maintained in the open.*

Essential VI / VIM commands for safely editing files and YAML on any system.
Focused on the minimum needed to work confidently in terminals, bastions, and restricted environments.

---

## Modes

i     → insert mode (start editing)

Esc   → command mode (always your escape hatch)

---

## Save & Exit

:w      # save

:q      # quit

:wq     # save and quit

:q!     # quit without saving

---

## Navigation

h       # move left

j       # move down

k       # move up

l       # move right


0       # start of line

$       # end of line

gg      # top of file

G       # bottom of file


/<text> # search for text

n       # next match

N       # previous match


## Editing

dd      # delete current line

yy      # copy (yank) current line

p       # paste below cursor

u       # undo

Ctrl+r  # redo


## Visual Mode

v       # visual (character selection)

V       # visual line selection


## Indentation (YAML-safe)

>>      # indent line

<<      # unindent line


## YAML Survival Rules

 ✔ Use spaces only (no tabs)
 
 ✔ Be consistent with indentation (commonly 2 spaces)
 
 ✔ Indentation defines structure
 
 ✔ When in doubt, align with the parent key

## Operator Tips

 - If something feels wrong, press Esc repeatedly.
   
 - If you're stuck, :q! is always an option.
   
 - Practice basic movements until they are muscle memory.
