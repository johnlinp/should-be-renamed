# Should Have Named

This is a list of Linux related functions/tools/files that are badly named.

Pull requests are welcome.


## `kill(1)` and `kill(2)`

Better names are: `sendsignal(1)` and `sendsignal(2)`.

`kill(1)` and `kill(2)` can send much more signals than `SIGKILL`.

Moreover, `kill(1)` actually sends `SIGTERM` instead of `SIGKILL` if no signal specified.


## `/etc/passwd`

Better name is: `/etc/user`.

There are no passwords in `/etc/passwd` nowadays. The passwords are in `/etc/shadow`.

Just like `/etc/group` contains a list of groups, a file that contains a list of users should be named `/etc/user`.


## `tcpdump(1)`

Better name is: `netdump(1)`.

It can dump more protocols than TCP.
