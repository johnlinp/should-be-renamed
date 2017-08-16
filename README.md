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


## `ulimit(1)`

Better name is: `sysconf(1)`

The default behavior of `ulimit(1)` is getting/setting file size, but it can deal with more system configurations than that.

In addition to that, the prefix "u" means "user", but it only affect the current session instead of all the sessions of the user.


## `wc(1)`

Better name is: `count(1)`.

`wc(1)` stands for "word count", but it can count words, newlines, bytes, etc.


## `atoi(3)`

Better name is: `str2int(3)`.

If `atoi(3)` was named `str2int(3)`, this [StackOverflow question](https://stackoverflow.com/questions/2909768/where-did-the-name-atoi-come-from) won't exist.


## `/etc/exports`

Better name is: `/etc/nfs.exports`.

It's not clear that `/etc/exports` belongs to NFS unless you check out `man 5 exports`.


## `top(1)`

Better name is: `proc(1)`

`top(1)` can display the processes information with the top usage of CPU/Memory. However, the name "top" is unclear because it can be interpreted as "top files in a filesystem", "top network transfer" or anything.

Furthermore, if you press "R" key in `top(1)`, it reverse the sorting order and make it `bottom(1)` :P

Therefore, `proc(1)` is clearer because it does nothing more than displaying process information.

[Wikipedia](https://en.wikipedia.org/wiki/Top_%28software%29) says "top" is short for "Table Of Process". But I don't think that is the original design.
