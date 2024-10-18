# vim-notes

## Movement through text
```
h, j, k, l      move cursor left, down, up, right
gj, gk          move cursor down, up (multi-line text)
H, M, L         move to top, middle, bottom of screen
w, W            jump forward to the start of a word, WORD (can contain punctuation)
e, E            jump forward to the end of a word, WORD (can contain punctuation)
b, B            jump backward to the start of a word, WORD (can contain punctuation)
ge, gE          jump backward to the end of a word, WORD (can contain punctuation)
%               move cursor to matching character (default supported pairs: '()', '{}', '[]')
0               jump to the start of the line
^               jump to the first non-blank character of the line
$               jump to the end of the line
g_              jump to the last non-blank character of the line
gg              go to the first line of the document
G               go to the last line of the document
5gg or 5G       go to line 5
gd, gD          move to local, global declaration
fx, tx          jump to next, before next occurrence of character x
Fx, Tx          jump to the previous, after previous occurrence of character x
;               repeat previous f, t, F or T movement
,               repeat previous f, t, F or T movement, backwards
}, {            jump to next, previous paragraph (or function/block, when editing code)
zz, zt, zb      position cursor on center, top, bottom of the screen
zs, ze          position cursor at start, end of line (when wrap text is off)
<ctrl-e>        move screen down one line (without moving cursor)
<ctrl-y>        move screen up one line (without moving cursor)
<ctrl-o>        move back through the breadcrumbs. Will jump through buffers.
<ctrl-i>        move forward through the breadcrumbs
<ctrl-u>        move cursor and screen up 1/2 page
<ctrl-d>        move cursor and screen down 1/2 page
<number>|       move to column <number>
```

## Insert mode
```
i               insert before the cursor
I               insert at the beginning of the line
a               append after the cursor
A               append at the end of the line
o, O            open a new line below, above the current line
ea              append at the end of the word
<ctrl-w>        delete word before the cursor during insert mode
<ctrl-t>        indent (move right) line one shiftwidth during insert mode
<ctrl-d>        de-indent (move left) line one shiftwidth during insert mode
<ctrl-n>        insert (auto-complete) next match before the cursor during insert mode
<ctrl-p>        insert (auto-complete) previous match before the cursor during insert mode
<ctrl-r>x       insert the contents of register x
<ctrl-o>x       temporarily enter normal mode to issue one normal-mode command x
```

## Editing
```
r               replace a single character
R               replace more than one character, until ESC is pressed
J               join line below to the current one with one space in between
gJ              join line below to the current one without space in between
gwip            reflow paragraph
g~              switch case up to motion
gu              change to lowercase up to motion
gU              change to uppercase up to motion
cc              change (replace) entire line
c$ or C         change (replace) to the end of the line
ciw             change (replace) entire word
cw or ce        change (replace) to the end of the word
s               delete character and substitute text (same as cl)
S               delete line and substitute text (same as cc)
xp              transpose two letters (delete and paste)
u               undo
U               restore (undo) last changed line
<ctrl-r>        redo
.               repeat last command
```

## Visual mode
```
v               start visual mode, mark lines, then do a command (like y-yank)
V               start linewise visual mode
o               move to other end of marked area
<ctrl-v>        start visual block mode
O               move to other corner of block
vaw             mark a word
vab, va(, va)   mark a block with ()
vaB, va{, va}   mark a block with {}
va<, va>        mark a block with <> tags
vib, vi(, vi)   mark inner block with ()
viB, vi{, vi}   mark inner block with {}
vi<, vi>        mark inner block with <> tags
>               shift marked text right
<               shift marked text left
y               yank (copy) marked text
d               delete marked text
~               switch marked text case
u               change marked text to lowercase
U               change marked text to uppercase
```

## Registers
```
:reg[isters]    show registers content
"xy             yank into register x
"xp             paste contents of register x
```

## Marks and positions
```
:marks          list of marks
ma              set current position for mark A
`a              jump to position of mark A
y`a             yank text to position of mark A
`0              go to the position where Vim was previously exited
`"              go to the position when last editing this file
`.              go to the position of the last change in this file
``              go to the position before the last jump
:ju[mps]        list of jumps
<ctrl-i>        go to newer position in jump list
<ctrl-o>        go to older position in jump list
:changes        list of changes
g,              go to newer position in change list
g;              go to older position in change list
<ctrl-]>        jump to the tag under cursor
```

## Macros
```
qa              record macro a
q               stop recording macro
@a              run macro a
3@a             run macro a 3 times
@@              rerun last run macro
5@@             rerun last run macro 5 times
```

## Cut and paste
```
yy              yank (copy) a line
2yy             yank (copy) 2 lines
yw              yank (copy) the characters of the word from the cursor position to the start of the next word
yiw             yank (copy) word under the cursor
yaw             yank (copy) word under the cursor and the space after or before it
y$ or Y         yank (copy) to end of line
p               paste the clipboard after cursor
P               paste before cursor
gp              paste the clipboard after cursor and leave cursor after the new text
gP              paste before cursor and leave cursor after the new text
dd              delete a line
2dd             delete 2 lines
dw              delete the characters of the word from the cursor position to the start of the next word
diw             delete word under the cursor
daw             delete word under the cursor and the space after or before it
:3,5d           delete lines starting from 3 to 5
:.,$d           delete from the current line to the end of the file
:g/{pattern}/d  delete all lines containing pattern
:g!/{pattern}/d delete all lines not containing pattern
d$ or D         delete to the end of the line
x               delete (cut) character
"+y             copy highlighted code to system clipboard
"+p             paste code from system clipboard
```

