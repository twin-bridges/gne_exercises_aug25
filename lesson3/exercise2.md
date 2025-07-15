
### Exercise 2a

```bash
$ git checkout -b branch-testing origin/branch-testing
branch 'branch-testing' set up to track 'origin/branch-testing'.
Switched to a new branch 'branch-testing'
```

### Exercise 2b

```bash
$ git branch
* branch-testing
  main
```

### Exercise 2c

```bash
# Here, I only show the last five commits.
$ git log --oneline
c8e9fff (HEAD -> branch-testing, origin/branch-testing, my_remote/branch-testing) Update WELCOME.md
51af644 Add WELCOME.md to branch-testing branch
05eaaf0 (main) Add lesson2 ex3 reference solution
9f0ed63 Fixing merge conflict (lesson2)
25b69b6 Prompt user for IP address in my_script.py
```

```bash
$ cat lesson3/WELCOME.md 

# Welcome to the testing branch.

```

### Exercise 2d

```bash
$ git branch -vv
* branch-testing c8e9fff [origin/branch-testing] Update WELCOME.md
  main           05eaaf0 [origin/main: behind 6] Add lesson2 ex3 reference solution

```
