# python
python -c 'import pty; pty.spawn("/bin/bash")'

python3 -c 'import pty; pty.spawn("/bin/bash")'
# bash :"bash: no job control in this shell"
script /dev/null -c bash

Ctrl + Z

stty raw -echo; fg

reset

export TERM=xterm / export TERM=xterm-256color


export SHELL=bash

# TTY shell
python3 -c 'import pty; pty.spawn("/bin/bash")'
