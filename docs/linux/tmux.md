# Tmux

---

## What is Tmux?
   
> Tmux is program which runs in a terminal and allows multiple other terminal programs to be run inside it.

## What Tmux stand for?

> Tmux stand for terminal multiplexer


## How tmux manages different programs?

> Each program inside tmux gets its own terminal manged by tmux, which can be accessed from the single terminal where tmux is running.


## Can a program be detached from the terminal?

> Tmux and any programs running inside it can be detached from the terminal where it is running (the outside terminal) and later reattached to the same or another terminal.

## What means tmux sessions are persistent?

> Means that programs running in tmux will continue to run even if you get disconnected.


## What are the main uses of tmux?

   * Work with multiple programs and shells together in one terminal, a bit like a window manager.
   * Protect running programs on a remote server from connection drops by running them inside tmux.
   * Allow programs running on remote server to be access from multiple different local computers.



## When the tmux server start running?

> The tmux server run automatically, when the server runs a tmux command and by default exists when there are no running programs.

## Where tmux keep its sates?

> Tmux keeps all its state in a single main process , called the tmux server. This runs in the background and manges all the programs running inside tmux and keeps track of their output.  


## How the client talks to the tmux server?

> Tmux takes over the terminal where it is run and talks to the server using a socket file in `/tmp` 

## Where programs run?

> Programs run in terminal panes, which each belong to one window


## What the window has?

> Each window has a name and one active pane by default.


## How many sessions windows are linked to? 

> Windows are linked to one or more sessions.

## How the session keep track of its windows?

> Each session has a list of windows, each with an index

## How many clients a session can attache?

> Sessions are attached to one or more clients, or are detached.


## What are the commands to use to create a session?
   * tmux
   * tmux new
   * tmux new-session  
!!! tipe
      All the three commands are used to create a session



## How to give a session a name?

> `tmux new -smysession` :  With `-s` flag you give the session a name



## How the keys are forwarded once a tmux client is attached?

> Once a tmux client is attached, any keys entered are forwarded to the program running in the active pane of the current window.


## What is the default prefix of tmux?

> `C-b`


## What happens when a tmux prefix is pressed?

> When the prefix key is pressed, tmux waits for another key press and that determines what tmux command is executed. 

## Command to show a list of all the short keys binding?

> `C-b ?`

## How to see a description of single key?

> `C-b /` 
!!! tip
      a prompt at the bottom of terminal appears

## Command to inter the interactive command prompt?

> `C-b :`


## What means detaching from the tmux?

> Detaching from a tmux session means disconnecting from the session while leaving it running in the background

## Command to detach?

> `C-b d`


## Command to reattach to the previous session?

> `tmux attach`

## Command to reattach to session by name?

> `tmux attach -tmysession` using the -t flag

## Command to list all the session that can be attached to?

> `tmux ls` (ls is an alias tmux-session)


## How to kill tmux server entirely? 
   * `:kill-server` in prompt of tmux
   * or if there are no session, windows or panes inside tmux  


## Command to create new window? 

> `C-b c` is using the key binding `new-window`



## How the pine is created?

> A pine is created by splitting a window, this done withe `split-window` command.

## Command to split the current pane horizontally?

> `C-b %`

## Command to split the current pane vertically?

> `C-b "`


## Command to rotate a pane from horizontally to vertically?

> `C-b space`


## Command to spilt horizontally or vertically a pane? (split-window)

> `split-window -v` or `split-window -h`


## Command to split the pane without living the active pane? (split-window)

> `split-window -d`

## What does this command do `split-window f`?

> Makes a new pane spanning the whole width or height of the window instead of being constrained to the size of the pane being split 


## What does this command do `split-window -b`?

> Puts the new pane to left or above of the pane being split instead of the right or below.


## How to copy using the mouse?
   * Shift + selection with the mouse
   * Shift + pressing the middle button of the mouse  


## Command to change to last window?

> `C-b l`


## Command to change to the next window?

> `C-b n`


## command to change to the previous window?

> `C-b p`


## What this command do `C-b w`?

> It is used to display a menu of all windows within the current session.

## What this command do `C-b number`?

> It prompts for a window index and change to that window

## Commands to change between the panes?
  
   * `C-b Up`
   * `C-b Down`
   * `C-b Left`
   * `C-b Right`


## What does this command do `C-b q`?

> prints the pane numbers and their size on the top the panes for a short time, pressing one of the number keys before they disappear changes the active pane to the chosen pane



## Command to display list of clients?

> `C-b D`

!!! tip
      Each client is shown in the list in the top half with its name..., entering (d, D, x or X) will detach that client


## Command to kill a window with confirmation?

> `C-b &` bounded to kill-pane and kill-session

## Command to kill only active pane?

> `C-b x` bounded to kill-pane and kill-session

## Command to rename a session?

> `C-b $`

## Command to rename a window?

> `C-b ,` bounded to rename-window


## What this command are used for `C-b {` and `C-b}`?

> Used to swipe pane, they are using `swap-window`, `wsip-pane`

## Commands to resize panes?

> `C-b C-Left`, `C-b C-Right`, `C-b C-Up` and `C-b C-Down`


## Command to make a pane temporarily take the whole window?

> `C-b z` ones takes the full window, to back tape the same command 


## Steps to copy using keys?

   * `C-b [` enter the copy mode
   * `C- Space` should very fast, used to select
   * `C-w` to copy
   *  `C-b ]` to paste in the insert mode or the command mode


## What this commands does in the copy mode `q`, `Ca` and `C-e`?

   * `q` exit the copy mode
   * `C-a` move the cursor the start of the line
   * `C-e` move the cursor the end of the line


## What this commands does in the copy mode `C-r`, `M-f` and `M-b`?

   * `C-r`  search interactively backwards
   * `M-f`, `M-b` move the cursor to the next or the previous word


## What this command do `C-b =`?

> Offer a list of buffers with a preview of their content


## What are the keys supported in the buffer mode?

   * `Enter` or `P` Paste the selected buffer
   * `d/D` delete the selected buffer

## Command to create a buffer?

> `:setb -bfoo bar` create a buffer named foo, with the content of bar


## Command to rename a buffer?
> `:setb bbuffer0 -nmybuffer` the flag -b gives the existing buffer a name and -n the new name


## What this command does `loadb -bbuffername ~/a/file`?

> load-buffer will load a buffer from a file 


## What this command does `saveb -bbuffer0 ~/saved-buffer`?
> An existing buffer can be saved to a file with `save-buffer`

## What does this command `C-b f`?
> prompts for some text and then enters tree mode with a filter to show only panes where that text appears in the visible content or title of the pane or the window name 

## Command to activate the mouse ?

> `set -g mouse on` should typed in `.tmux.conf` file


