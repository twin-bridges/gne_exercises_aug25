### Exercise 10a

```shell
$ git rm not-empty 
rm 'lesson1/not-empty'

$ git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	deleted:    not-empty

```

### Exercise 10b

```shell
$ ls
simple.py
```

### Exercise 10c

```shell
$ git commit -m "Remove lesson1/not-empty file"
[main 717bc75] Remove lesson1/not-empty file
 1 file changed, 0 insertions(+), 0 deletions(-)
 delete mode 100644 lesson1/not-empty
```

### Exercise 10d

```shell
$ git log --oneline
717bc75 (HEAD -> main) Remove lesson1/not-empty file
af1793c Updating simple.py script
ea5ac39 Adding simple.py Python script
1edae0e Initial commit of per-lesson directories
```
