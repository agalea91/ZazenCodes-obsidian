---
date: 2024-03-08
tags:
    - cheat-sheet
hubs:
    - "[[linux]]"
    - "[[macos]]"
urls:
    - https://gist.github.com/MohamedAlaa/2961058
    - https://tmuxcheatsheet.com/
---

# Tmux Cheat Sheet

## Outside tmux

New session
```bash
tmux
tmux new -s myname
```

Attach to existing session
```bash
tmux a
tmux a -t myname
```

List, kill sessions
```bash
tmux ls
tmux kill-session -t myname
```

## Inside tmux

Commands below must be proceeded by the bind key. The default is CTRL-b. My bind key is "CTRL-a".

```
# Help
?   list all shortcuts

# Panes
%   vertical split
"   horizontal split
o   swap panes
;   toggle last active pane
q   show pane numbers
x   kill pane
+   break pane into window (e.g. to select text by mouse to copy)
-   restore pane from window
⍽   space - toggle between layouts
{   move the current pane left
}   move the current pane right
z   toggle pane zoom
CTRL-

# Windows
c   create window
w   list windows
n   next window
p   previous window
f   find window
,   name window
&   kill window

# Sessions
s   list sessions
$   name session
```

