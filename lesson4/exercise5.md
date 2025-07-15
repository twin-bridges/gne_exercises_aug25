
### Exercise 5a

```bash
$ git checkout -b l4-feature1 main
Switched to a new branch 'l4-feature1'

$ git branch -v
  branch-testing 51af644 Add WELCOME.md to branch-testing branch
* l4-feature1    b2069b9 Lesson4, ex2 and ex4
  main           b2069b9 [ahead 1] Lesson4, ex2 and ex4

$ git add ip_addresses.yaml 

$ git commit -m "Add broadcast address"
[l4-feature1 4c7e384] Add broadcast address
 1 file changed, 7 insertions(+)
 create mode 100644 lesson4/ip_addresses.yaml
```

### Exercise 5b

```bash
$ git push my_remote l4-feature1
Username for 'https://github.com': jupiter-calisto
Password for 'https://jupiter-calisto@github.com': 
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Compressing objects: 100% (9/9), done.
Writing objects: 100% (9/9), 1.38 KiB | 1.38 MiB/s, done.
Total 9 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote: 
remote: Create a pull request for 'l4-feature1' on GitHub by visiting:
remote:      https://github.com/jupiter-calisto/gne_exercises_aug25/pull/new/l4-feature1
remote: 
To https://github.com/jupiter-calisto/gne_exercises_aug25
 * [new branch]      l4-feature1 -> l4-feature1
```

### Exercise 5c

```bash
# Here is my example pull-request for this exercise (merged in step "5e"):
https://github.com/jupiter-calisto/gne_exercises_aug25/pull/2
```


### Exercise 5d

```bash
# Here is the example changes I committed to "l4-feature1"
https://github.com/jupiter-calisto/gne_exercises_aug25/pull/2/files
```

#### HERE ####

####### Exercise 5e #######

# Here is the "merge" commit into the "main" branch:

https://github.com/jupiter-calisto/gne_exercises/commit/82622d862ee087148a69971b3073cde01f1d56d4

