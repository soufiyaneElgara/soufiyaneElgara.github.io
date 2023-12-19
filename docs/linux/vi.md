# Vi 
---

## Waht is Vi 

> **Vi** is a text editor that's been around for a long time and remains a powerful and widely used tool, especially in Unix-based systems.

## What are the modes existing in Vi? (04)
   * Normal Mode
   * Insert Mode (i)
   * Visual Mode (v)
   * Ex Mode (:)

## What "normal mode" do?

> Navigate the structure of the file

## What "insert mode" do ?

> Editing the file

## What "visual mode" do?

> Highlight portions of the file to manipulate at one 

## What "ex mode" do?
> Command mode

## Command to scroll the window down?

> `Ctrl + e` or use the arrows

## Command to scroll the window up?

> `Ctrl + y` or use the arrows

## One single command to move the cursor to the top of the window?
>  `H`

## One single command to move the cursor to the middle of the window?

> `M`

## One single command to move the cursor the bottom of the window?

> `L``

## What does `gg` do?

> Go to the top of a file

## What does `G` do?

> Go to the end of the file  

## What are the components of the secret sauce?
   * Text objects and motions
   * The DOT command
   * macros

## What are the text objects?
   * `w` word
   * `s` sentence
   * `p` paragraph
   * `t` tag

## What are the motions in vim?

   * `a` all
   * `i` in 
   * `f` search forward
   * `F` search backward

## What are the essential commands?

   * `d` delete
   * `y` yank
   * `c` change
   * `v` visual selection


## Describe what this command does, `dw` `daw` `cw` `caw`?

   * `dw` delete the word starting from the position of the cursor
   * `daw` delete all the word, doesn't mutter the position of cursor in the word
   * `cw` delete and put you in the insert mode starting from the position of the cursor.
   * `caw`: deleting the all word ind puts you in the insert mode


## Describe what this command does, `yi)` `di)` `va'`?
   * `yi)` yank all text inside parentheses
   * `di)` delete inside parentheses
   * `va'` select all inside '

## What DOT command do?

> The dot (.) command repeat the last command

## What this commands does `dd/yy` `D/C` `^/$` `I/A` `o/O` `p/P` ?

   * `dd/yy` (delete/yank) the current line
   * `D/C`   (delete/change) all line the end of it
   * `^/$`   move to the (beginning/end) of the line
   * `I/A`   move to the (beginning/end) of the line and insert
   * `o/O`   insert new line (above/below) the current  
   * `p/P`   paste (below/above)


## What this commands does `u` `Ctrl+ r` `b` `w` ?

   * `u`       undo
   * `Ctrl+ r` redo
   * `b`       backward by a word
   * `w`       forward by a word


## Command to select a line?

>  `Shift v`

## Command to back 2 minutes in time?

> `:earlier 2m`

## Command to delete current paragraph?

> `dap`

## Command to yank current paragraph?

> `yap`

## Command to append to current word?

> `ea`

## Command to delete the current function?
> `daf`

## Command to yank current function?
>  `yaf`

## What this commands do `dif` `yif`?
   
   * `dif`  delete current inner function
   * `dif`  yank current inner function


## What we called `!`?

> They called magic wands or bang bang


## What uses of the magic wands (!)?

> Magic wands are mnemonic device for using the exclamation point (!) to send the current line, section or page to any command that can be run from the shell and replace those lines with the output if that command.

## What are the three types of magic wands?

   * Line wand
   * Section wand
   * Line number wand

## What is the most fastest and common way to extend vi?

> It is the Line wand

## How to execute the line wand? 

> Just spam bang twice(!!) to send the current line to the shell command or replace the current line with the output of utility command like date, cal or any text that comes out of any command

## What are the commands to send a line to `bash` `Calc` `python3`?

Just type on the key board :
   * For bash    : !!bash  
   * for Cal     : !!bc
   * for python3!: !!python3

## How to select a section wand?

> Just type `!}`

## Command to sort a section and send it to bash?

   * `!}sort`
   * `!}bash` 

## What is a lined number wand?

> Lined number wand is just a larger version of the section wand but allows blank lines to be included.

## How to do a lined number wand?

> Start with bang (type only one bang) and follow it up with a colon and the line after the last line that you want to include fore example: 
>  type `!`, than type `:` only : colon will appear than add the line number after that one you want to include

## Give the steps to comment a section with on space?
   
   * Put the cursor where you want start commenting
   * type `!}` you will select that section, and in the output remove the (!)
   * then type `s/^/# /g`
   * the full command is `:.,.+10s/^/# /g` you can not add the (g)

## Explain this line of code? `:.,.+10s/^/# /g`

   * `.` dote stand for the current position
   * `+10` ten lines plus from the current position
   * `s` substation 
   * `^` the beginning of the line
   * `g` means change everything similar in that line 



## Give the steps to comment a section with spaces on it?  

   * put the cursor on the line you want to start from
   * type only one bang (!)
   * type after colon (:) plus the line after the last line that you want to include.
   * The pup of an we line showing the full path of the selected section, type after what you want `bash/pandoc` or `s/^.#` (to comment make sure to delete ! before)


## What this command do `h` `j` `k` `l`?

   * `h` : move cursor left
   * `j` : move cursor down
   * `k` : move cursor up
   * `l` : move cursor right

## What this command do `H` `M` `L`? 

   * `H` : move to top of screen
   * `M` : move to middle of screen
   * `L` : move to bottom of screen

## What this command do `w` `e` `b`?

   * `w` : jump forwards to start of a word
   * `e` : jump forwards to end of a word
   * `b` : jump backwards to start of a word

## What this commands do `0` `$` `}` `{` ?

   * `0` : jump to the start of the line
   * `$` : jump to the end of the line
   * `}` : jump to next paragraph
   * `{` : jump to previous paragraph

## What this commands do `zz` `zt` `zb` `C-e` `C-y`?

   * `zz`: centre cursor on screen
   * `zt`: position cursor on top of the screen
   * `zb`: position cursor on bottom of the screen
   * `Ctrl + e` : move screen down
   * `Ctrl + y` : move screen up one line

## What this command do `i`, `I`, `a`, `A`, `o`, `O`, `ea`?

   * `i`: insert before the cursor
   * `I`: insert at the beginning of the line
   * `a`: insert (append) after the cursor
   * `A`: insert (append) at the end of the line
   * `o`: append (open) a new line below the current line
   * `O`: append (open) a new line above the current line
   * `ea`: insert (append) at the end of the word

## What this commands do `C-h` `Ctrl-w` `C-j` `C-t` `C-d` `C-n` `C-p`?

   * `Ctrl + h` : delete the character before the cursor during insert mode
   * `Ctrl + w` : delete word before the cursor during insert mode
   * `Ctrl + j` : begin new line during insert mode
   * `Ctrl + t` : indent (move to right) line one shift width during insert mode
   * `Ctrl + d` : de-indent (move to left) line one shift width during insert mode
   * `Ctrl + n` : insert (auto-complete) next match before the cursor during insert mode
   * `Ctrl + p` : insert (auto-complete) previous match before the cursor during insert mode


## What this commands do `r` `R` `J` `gJ`? 

   * `r` : replace a single character
   * `R` : replace more than one character, until `Esc` is pressed
   * `J` : join line below to the current one with one space in between
   * `gJ`: join line below to the current one without space in between

## What this commands do `~` `cc` `C` `ciw`, `cw` ?

   * `~` : change to lower or upper case
   * `cc` : change (replace) entire line
   * `C` : change (replace) to the end of the line
   * `ciw` : change (replace) entire word
   * `cw`: change (replace) t the end of word

## What this commands do `s` `S` `u` `C-r` `.`?
   * `s` : delete character and substitute text
   * `S` :delete line and substitute text (same as cc)
   * `u` : undo
   * `Ctrl + r` : redo
   * `.` : repeat last command

## Command to mark text (visual mode)? (02)

   * `v` : start visual mode, mark lines , then do a command (like y-yank)
   * `V` : start Line-wise visual mode

## What this commands in the visual mode `>` `<` `y` `d` `~` `u` `U`?

   * `>` : shift text right
   * `<` : shift text left
   * `y` : yank (copy) marked text
   * `d` : delete marked text
   * `~` : switch case
   * `u` : change marked text to lower case
   * `U` : change marked text to uppercase


## Command to start a macro?

> `qa` : record macro a (a is the name)

## Command to stop recording a macro?

> `q`  : stop recording macro

## Command to run a macro?
   
   * `@`  : run macro a
   * `@@` : rerun last run macro

## Command same as `:wq`?

> `ZZ`

## Command same as `:q!`?

> `ZQ` 

## Command to delete from the current position into a certain word?

> `d/searchedWord`

## Command to yank from the current position into a certain word?
>  `y/searchedWord`

## What this commands do `D/d$` `dap` `daf`?

   * `D` `d$` delete into the end of file
   * `dap` delete all paragraph
   * `daf`  delete all function

## Command to delete only what inside the function ?

> `def`

## Command to show where you are?

> `Ctrl+ g`

## what this commands do `:%` `:12`?

   * `:%` moves you to the last line
   * `:12` moves you to line 12

## Command to copy the whole file?

> `y :%` y is a command flowed by :%

## Command to delete from current position into the last line?

> `:.,%d`

## Command to select all lines of a paragraph? using!

> `!}`
