# tmux (Cheat Sheet)

Start a new session

```sh
tmux new -s mysession
	    ^session name
```

Show all sessions:

```sh
tmux ls
```

Attach to session:

```sh
tmux attach -t mysession
```

Detach from session:`Ctrl`+`b` `d`

Scroll: (Enter copy mode) `Ctrl`+`b` `[ (Exit copy mode) `q`

Split vertically (left/right): `Ctrl`+`b` `%`
Close pane: `Ctrl`+`b` `x`

Split horizontally (top/bottom): `Ctrl`+`b` `"`"

Move between panes: `Ctrl`+`b` arrow keys
