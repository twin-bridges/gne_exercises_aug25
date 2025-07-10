
### Exercise 2a

```bash
# Create and checkout the 'l3-feature2' branch using a single command.
$ git checkout -b l3-feature2 main
Switched to a new branch 'l3-feature2'

$ git branch
* l3-feature2
  main
```

### Exercise 2b

```bash
$ vi ip_addresses.yaml 
$ git add ip_addresses.yaml 
$ git commit -m "l3-feature2: commit1"
[l3-feature2 4da9aa6] l3-feature2: commit1
 1 file changed, 1 insertion(+), 1 deletion(-)

$ vi ip_addresses.yaml 
$ git add ip_addresses.yaml 
$ git commit -m "l3-feature2: commit2"
[l3-feature2 e975a60] l3-feature2: commit2
 1 file changed, 1 insertion(+)

# I am only showing the last 5 commits
$ git log --oneline
e975a60 (HEAD -> l3-feature2) l3-feature2: commit2
4da9aa6 l3-feature2: commit1
51423ed (main) l3-feature1: commit2
11132d3 l3-feature1: commit1
0e4e162 (origin/main) Fixing ex5 markdown
```

### Exercise 2c

```bash
$ git checkout main
Switched to branch 'main'

$ vi mcast_bcast.yml 
$ git add mcast_bcast.yml 
$ git commit -m "Commit in 'main' to force a 3-way merge"
[main 2755c6a] Commit in 'main' to force a 3-way merge
 1 file changed, 3 insertions(+)
 create mode 100644 lesson2/mcast_bcast.yml
```

### Exercise 2d

```bash
# Verify on branch 'main'
$ git branch
  l3-feature2
* main
```

```bash
# Merge l3-feature2 into 'main' ('ort' strategy is a 3-way merge here)
$ git merge l3-feature2
Merge made by the 'ort' strategy.
 lesson2/ip_addresses.yaml | 3 ++-
 1 file changed, 2 insertions(+), 1 deletion(-)

# The merge immediately drops me into an editor (I just do "<esc>" and then
# ":wq" to save this in vim).

Merge branch 'l3-feature2'
# Please enter a commit message to explain why this merge is necessary,
# especially if it merges an updated upstream into a topic branch.
#
# Lines starting with '#' will be ignored, and an empty message aborts
# the commit.
```

### Exercise 2e

```bash
# Yes, the l3-feature2 changes now exist on 'main'
$ git branch
  l3-feature2
* main
```

```bash
$ pwd
/home/kbyers/gne_exercises_aug25/lesson2

# For some reason, I used .yaml for one file and .yml for the other :-)
$ ls -al *.y*
-rw-r--r--. 1 kbyers kbyers 80 Jul 10 09:03 ip_addresses.yaml
-rw-r--r--. 1 kbyers kbyers 39 Jul  9 15:54 mcast_bcast.yml
```

```yaml
$ cat ip_addresses.yaml 
---
- 192.168.0.0/16
- 172.16.0.0/12
- 10.0.0.0/8
- 127.0.0.1/32
- 127.0.0.2/32
```

```bash
# Only the last 6 commits are shown.
$ git log --oneline
cabbf18 (HEAD -> main) Merge branch 'l3-feature2'
2755c6a Commit in 'main' to force a 3-way merge
e975a60 (l3-feature2) l3-feature2: commit2
4da9aa6 l3-feature2: commit1
51423ed l3-feature1: commit2
11132d3 l3-feature1: commit1
```

### Exercise 2f

```bash
$ git branch
  l3-feature2
* main

$ git branch -d l3-feature2
Deleted branch l3-feature2 (was e975a60).
```

