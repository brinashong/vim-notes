# vim-notes

## Movement through text
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
gd              move to local declaration
gD              move to global declaration
fx              jump to next occurrence of character x
tx              jump to before next occurrence of character x
Fx              jump to the previous occurrence of character x
Tx              jump to after previous occurrence of character x
;               repeat previous f, t, F or T movement
,               repeat previous f, t, F or T movement, backwards
}               jump to next paragraph (or function/block, when editing code)
{               jump to previous paragraph (or function/block, when editing code)
zz              center cursor on screen
zt              position cursor on top of the screen
zb              position cursor on bottom of the screen
<ctrl-e>        move screen down one line (without moving cursor)
<ctrl-y>        move screen up one line (without moving cursor)
<ctrl-o>        move back through the breadcrumbs. Will jump through buffers.
<ctrl-i>        move forward through the breadcrumbs
<ctrl-u>        move cursor and screen up 1/2 page
<ctrl-d>        move cursor and screen down 1/2 page
<number>|       move to column <number>
