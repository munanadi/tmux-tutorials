### Tmux - Terminal Multiplexer

```
sudo apt install tmux
```

The leader key is something that you press and follow it up with different keys to do magical stuff.
The default leader key is `Ctrl b` (`<C-b>`), however this can be remapped.

This can be useful if you accedentially drop sessions or close your terminal. Everything will be as it was.

> The `tmux.conf` goes in the `HOME` dir and should be renamed as `.tmux.conf`

#### Panes

Sections of a window. 
- `prefix "`  To open a vertical split
- `prefix %`  To open a horizontal split

`prefix z` to toggle zooms between a focussed pane.

#### Windows

-`prefix c` creates a new window
-`prefix p` navigates to the previous window
-`prefix n` navigates to the next window

`*` would represent the window we are currenly in.

> `prefix #` where # is the number of the window, used to switch between windows

-`prefix &` closes the current window
-`prefix ,` to rename the current window

> To get out of tmux and not close sessioins, we do `prefix d` to disconnect from the sessions

#### To list sessions

`tmux ls` would list all the sessions, first thing would be the target number to connect to the session.

`prefix $` to rename sessions from the normal numbers assinged to names as you wish.



Reconnecting to sessions can be done using

- `tmux attach (a) -t #` where # is the number or name assigned to a session

#### To switch between all sessions

`prefix s` and you can get previews all sessions that are active too.

#### Remaps can be done to change leader

> `.tmux.conf` in the base `HOME` directory will house these remaps. 

This file doesnt exist be default and needs to be creted to add cofigs

- Remap `prefix` to `Ctrl a` for easier access
- `Alt arrows` to switch between window panes
- `Shift arrrows` to swtich between windows
- Mouse can be used to enter a secific pane or even to rearrange
- `prefix h/v` to create horizontal or vertical splits
- `prefix r` will source the file to directly apply any changes that are done to the config files

##### Copy stuff from tmux terminals

 - `prefix [` to enter copy mode.
 - This will put your cursor where you can move around freely
 - Now start copying with `Ctrl space` and move around to copy, shown by highlighted text
 - `Ctrl w` to stop copying
 - `prefix ]` to paste the thing you have copied.

 > Holding down `Shft` and selecting text seems to be able to copy to thhe systems clipboard, Then I can use `Ctrl Shft v` to paste stuff outside tmux.

### Toggle between

- `prefix + l` switch to last window
- `prefix + L` switch to last session
