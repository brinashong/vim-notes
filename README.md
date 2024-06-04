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
Esc or <ctrl-c> exit insert mode
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
aw              mark a word
ab              a block with ()
aB              a block with {}
at              a block with <> tags
ib              inner block with ()
iB              inner block with {}
it              inner block with <> tags
Esc or <ctrl-c> exit visual mode
```

## Visual commands
```
>               shift text right
<               shift text left
y               yank (copy) marked text
d               delete marked text
~               switch case
u               change marked text to lowercase
U               change marked text to uppercase
```
