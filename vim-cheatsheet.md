# Vim cheatsheet

Modes
Normal: esc
Insert: i
Visual: v

Move cursor
h j k l

Move cursor by word
w b e

Find
f

Go to matching ( { [
%

Go to beginning of line
0

Go to end of line
$

Find next occurrence of word under the cursor
*

Find previous occurrence of word under the cursor
#

Go to beginning of file
gg

Go to end of file
G

Go to line 3
3G

Search
/

  Go to next occurance
  n

  Go to previous occurance
  N

Insert line below
o

Insert line above
O

Remove character under cursor
x

Remove character to the left of cursor
X

Delete a word (and copy it)
dw

Delete two words
d2w

Delete a line
dd

Repeat previous command
.

Undo
u

Redo
ctlr + R

Save
:w

Quit
:q

Quit without saving
:q!

## Resource
http://www.openvim.com/tutorial.html

Vim for Atom
https://atom.io/packages/vim-mode
and ex-mode in Atom
https://atom.io/packages/ex-mode

Mapping jj to Command mode in Atom
https://github.com/atom/vim-mode/issues/128

To find and replace all occurrences of "rug" with "bug", enter:
:%s/rug/bug/g

And on current line only:
:s/rug/bug/g

Case insensitive:
:%s/rug/bug/gi

From line 3 to 7:
:3,7s/rug/bug/g
