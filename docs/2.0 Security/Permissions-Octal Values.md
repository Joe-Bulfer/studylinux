- r (read): 4
- w (write): 2
- x (execute): 1 

`chmod 764 file` would mean rwx for owner, rw for group, and r for others.

umask is the default set of permissions that subtracts from 666 for files, and 777 for directories
```
umask
0002

touch file

stat -c "%a" file
664
```

`chmod` can use octal mode/numeric (like above) or symbolic.

Here we change the file permissions for owner and group to rwx
```
chmod og+rwx file
```