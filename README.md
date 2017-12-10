# Array-based Command Injection

In some circumstances, software will call an external command using the a
function like `execve`, which takes an array instead of a string passed to
`/bin/sh`. Sometimes, software assumes that because the command is not passed to
a shell, it is safe to include user input in the array. However, there are
several examples of commands that, when given arbitrary arguments via array, can
still grant command injection. This happens if the external command uses an
argument to make a call to another external command.

For example, some versions of `tar` include the argument `--checkpoint-action`,
which can be given the value `--checkpoint-action=exec=COMMAND` where `COMMAND`
is an arbitrary external command.

This repository attempts to document cases of array-based command injection and
give examples and constraints in various environments.
