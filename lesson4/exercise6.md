
### Exercise 6a

```bash
$ git pull my_remote main
From https://github.com/jupiter-calisto/gne_exercises_aug25
 * branch            main       -> FETCH_HEAD
Updating b2069b9..97dfef5
Fast-forward
 lesson4/ip_addresses.yaml | 7 +++++++
 1 file changed, 7 insertions(+)
 create mode 100644 lesson4/ip_addresses.yaml

# The first commit is the merge commit made during the pull-request.
# The second commit is the l4-feature1 commit (the actual change in the PR).
$ git log --oneline --graph --decorate
*   97dfef5 (HEAD -> main, origin/main, origin/HEAD, my_remote/main) Merge pull request #2 from jupiter-calisto/l4-feature1
|\  
| * 4c7e384 (my_remote/l4-feature1) Add broadcast address
|/  
* b2069b9 Lesson4, ex2 and ex4
* e3f66b7 Adding note into lesson1 ex5, and ex6
* 65c3d37 Remove unneeded 'lesson' directory
```

### Exercise 6b

```bash
$ git branch
  branch-testing
* l4-feature1
  main

# Note, I had to use `-D` to delete the branch (instead of `-d`) as I had 
# some additional complexity in my setup (mostly due to creating reference 
# solutions).
$ git branch -D l4-feature1
Deleted branch l4-feature1 (was 4c7e384).
```

