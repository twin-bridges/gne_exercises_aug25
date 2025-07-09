### Exercise 8a

```shell
$ cd lesson1
$ vi simple.py
----
# Edit 'simple.py' file
print("Hello world")
```

### Exercise 8b

```shell
$ git add simple.py 
$ git commit -m "Adding simple.py Python script"
[main ea5ac39] Adding simple.py Python script
 1 file changed, 1 insertion(+)
 create mode 100644 lesson1/simple.py
```

### Exercise 8c

```shell
$ git log
commit ea5ac397966efe365b55a3332de1b1894cadbd5e (HEAD -> main)
Author: Kirk Byers <ktbyers@twb-tech.com>
Date:   Wed Jul 9 15:03:04 2025 -0700

    Adding simple.py Python script

commit 1edae0eb82477fc759b5bbf8952158e1021eab48
Author: Kirk Byers <ktbyers@twb-tech.com>
Date:   Wed Jul 9 14:59:52 2025 -0700

    Initial commit of per-lesson directories
```
