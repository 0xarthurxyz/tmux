# tmux (Cheat Sheet)

Read man page with all docs:

```sh
man tmux
```

Start a new session

```sh
new-session [-AdDEPX] [-c start-directory] [-e environment] [-f flags] [-F format] [-n window-name] [-s session-name] [-t group-name] [-x
             width] [-y height] [shell-command]
                   (alias: new)
             Create a new session with name session-name.
```

```sh
tmux new -s mysession
tmux new-session -s mysession
```

List all sessions:

```sh
tmux ls
```

Attach to session:

```sh
attach-session [-dErx] [-c working-directory] [-f flags] [-t target-session]
                   (alias: attach)
             If run from outside tmux, create a new client in the current terminal and attach it to target-session.  If used from inside, switch the
             current client.  If -d is specified, any other clients attached to the session are detached.  If -x is given, send SIGHUP to the parent
             process of the client as well as detaching the client, typically causing it to exit.  -f sets a comma-separated list of client flags.
```

```sh
tmux attach -t mysession
```

Rename session:

```sh
rename-session [-t target-session] new-name
                   (alias: rename)
             Rename the session to new-name.
```

```sh
tmux rename -t mysession newName
tmux rename-session -t mysession newName
```

Prefix (default): `Ctrl`+`b`

Detach from session: `Prefix` `d`

Create new window: `Prefix` `c`

Rename window: `Prefix` `,`

List all windows: `Prefix` `w`

Move pane: `Prefix` `{` (left) `}` (right)

Scroll: (Enter copy mode) `Prefix` `[` (Exit copy mode) `q`

Split vertically (left/right): `Prefix` `%`
Close pane: `Prefix` `x`

Split horizontally (top/bottom): `Prefix` `"`

Move between panes: `Prefix` arrow key

Delete session: 

```sh
tnux kill-session -t <sessionName>
```

Resize window (window with lots of dots)

```sh
tmux a -d -t <SESSION_NUM>
```

> When you attach to a session in two different terminal applications.
> You may notice that some of the window space is filled with dots. 
> That is because the session window before is smaller than the current window.

Source: [jdhao.github.io](https://jdhao.github.io/2018/10/23/tmux_questions_and_trouble_shooting/)

Resources:

- "tmux shortcuts & cheatsheet" ([gist.github.com](https://gist.github.com/MohamedAlaa/2961058))