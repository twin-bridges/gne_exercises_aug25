
### Exercise 1a

```shell
$ git branch l3-feature1

$ git checkout l3-feature1
Switched to branch 'l3-feature1'

$ git branch
* l3-feature1
  main
```

### Exercise 1b

```shell
# .git/HEAD currently points at the 'l3-feature1' branch (ref)
$ cat .git/HEAD 
ref: refs/heads/l3-feature1

# ./git/refs/heads/l3-feature1 contains the hash of the current
# commit (that this 'l3-feature1' branch points at).
$ cat .git/refs/heads/l3-feature1 
0e4e1625e2d816e6fdea526520d028e6cf7390d9

# You can see this '0e4e162' commit also in 'git log'
$ git log --oneline
0e4e162 (HEAD -> l3-feature1, origin/main, main) Fixing ex5 markdown
```

### Exercise 1c

```bash
# File that you change doesn't really matter (here I just add a new file)
$ vi ip_addresses.yaml

$ git add ip_addresses.yaml
$ git commit -m "l3-feature1: commit1"
[l3-feature1 11132d3] l3-feature1: commit1
 1 file changed, 6 insertions(+)
 create mode 100644 lesson2/ip_addresses.yaml

# I changed the same file (in order to do the second commit)
$ vi ip_addresses.yaml

$ git add ip_addresses.yaml 
$ git commit -m "l3-feature1: commit2"
[l3-feature1 51423ed] l3-feature1: commit2
 1 file changed, 1 deletion(-)

$ git log --oneline
51423ed (HEAD -> l3-feature1) l3-feature1: commit2
11132d3 l3-feature1: commit1
0e4e162 (origin/main, main) Fixing ex5 markdown
3d4297f Add README, LICENSE, very simple .gitignore
4a35d24 Add lesson1 reference solutions
717bc75 Remove lesson1/not-empty file
af1793c Updating simple.py script
ea5ac39 Adding simple.py Python script
1edae0e Initial commit of per-lesson directories
```

### Exercise 1d

```bash
# Merge l3-feature1 into 'main' (you can see 'Fast-forward' below)
# REMEMBER: Checkout the branch that you are 'merging into' and
#           then use 'git merge <the-branch-merging-from>'
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

$ git merge l3-feature1
Updating 0e4e162..51423ed
Fast-forward
 lesson2/ip_addresses.yaml | 5 +++++
 1 file changed, 5 insertions(+)
 create mode 100644 lesson2/ip_addresses.yaml
```

### Exercise 1e

```bash
# Yes, the changes from the l3-feature1 branch now exist on 'main'
$ git branch
  l3-feature1
* main

$ pwd
/home/kbyers/gne_exercises_aug25/lesson2

# I added and modified this file in 'l3-feature1'
$ cat ip_addresses.yaml 
---
- 192.168.0.0/16
- 172.16.0.0/12
- 10.0.0.0/8
- 127.0.0.0/8
```

### Exercise 1f

```bash
$ git branch
  l3-feature1
* main

$ git branch -d l3-feature1
Deleted branch l3-feature1 (was 51423ed).

$ git branch
* main
```
