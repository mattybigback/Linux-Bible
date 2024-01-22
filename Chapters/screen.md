# Screen
GNU Screen is a terminal multiplexer that enables a user to run multiple terminal sessions inside a single terminal window or remote terminal session. Screen allows you to create, access, and control multiple virtual windows from a single terminal. Each window runs its own shell or process independently, and windows can be split 

Screen also allows sessions to persist independently of the connection to the server. This is especially useful when connecting to a server remotely using ssh.

## Session management

### Launch a new instance of screen
```
$ screen
```
### Launch a new instance of screen
```
$ screen -S yournamehere
```
### Detach from screen session but keep it running
```
$ screen -d
```
### End currently attached screen session
```
$ exit
```
### End a detached screen session
```
$ screen -X -S <session name/id> quit
```
### List all screen sessions
```
$ screen -ls
```
## Screen commands
Screen has a built in command console that allows for control of virtual windows within a session. You can access this command console by pressing **Ctrl+a**.

|     Command    |     Description                             |
|----------------|---------------------------------------------|
|     “          |     Show list of   windows                  |
|     \<digit>   |     Switch to   window 0-9                  |
|     tab        |     Switch focus   to the next region       |
|     c          |     Create new   window and switch to it    |
|     d          |     Detach from   screen session            |
|     k          |     Kill current   window                   |
|     \|         |     Split current   region vertically       |
|     S          |     Split current   region horizontally     |
|     X          |     Kill current   region                   |
| ?              | Show all commands and their defaults        |