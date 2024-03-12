# tmux

[tmux](https://github.com/tmux/tmux) is a terminal multiplexer.
It lets you switch easily between several programs in one terminal, detach them (they keep running in the background) and reattach them to a different terminal.

## Commands

- tmux kill-session -t {session_name}
  - kills the specific session

> I have an alias set in my .zshrc to kill all the tmux instances

```
alias tkill="tmux ls | awk '{print $1}'|sed 's/.$//'| xargs -t -n1 tmux kill-session -t"
```

- tmux ls
  - list all active sessions
- tmux attach-session
  - By default attaches to the last session

> Refer to [tmux cheat sheet](https://tmuxcheatsheet.com/) for a quick reference.

## Bindings

> My tmux prefix is set to C-a

- prefix + ':': open tmux command mode
  - provides tab-completion
- prefix + z: toggle fullscreen
- prefix + x: kill pane
- prefix + c: create window
- prefix + %: horizontal split
- prefix + ": vertical split
- prefix + s: display all sessions
- prefix + w: display all window
- custom:
  - prefix + r: reloads my tmux config file located at ~/.config/tmux/tmux.conf
  - prefix + p: starts pomodoro
  - prefix + C-p: opens pomodoro settings

## Plugins I use

> I use [tpm](https://github.com/tmux-plugins/tpm) (tmux plugin manager) for tmux plugin management.

- ['tmux-plugins/tpm'](https:/egithub.com/tmux-plugins/tpm)
- ['tmux-plugins/tmux-sensible'](https://github.com/tmux-plugins/tmux-sensible)
- ['olimorris/tmux-pomodoro-plus'](https://github.com/olimorris/tmux-pomodoro-plus)
  - for pomodoro in tmux status bar
- ['egel/tmux-gruvbox'](https://github.com/egel/tmux-gruvbox)
  - gruvbox theme for tmux which I patched to add the pomodoro plugin
- ['tmux-plugins/tmux-resurrect'](https://github.com/tmux-plugins/tmux-resurrect)
  - persists tmux sessions after computer restarts
- ['tmux-plugins/tmux-continuum'](https://github.com/tmux-plugins/tmux-continuum)
  - automatically saves sessions every 15 mins

## Tutorials

> Visual learner?

- [Dreams of Code](https://www.youtube.com/watch?v=DzNmUNvnB04)
- [typecraft](https://www.youtube.com/watch?v=H70lULWJeig)
- [Josean Martinez](https://www.youtube.com/watch?v=U-omALWIBos)
