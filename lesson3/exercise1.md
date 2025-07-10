
### Exercise 1a

```bash
# Make sure I am outside of the existing 'gne_exercises_aug25' directory.
$ pwd
/home/kbyers
```

```bash
$ git clone https://github.com/twin-bridges/gne_exercises_aug25 remotes_gne_exercises
Cloning into 'remotes_gne_exercises'...
remote: Enumerating objects: 81, done.
remote: Counting objects: 100% (81/81), done.
remote: Compressing objects: 100% (51/51), done.
remote: Total 81 (delta 30), reused 75 (delta 24), pack-reused 0 (from 0)
Receiving objects: 100% (81/81), 15.05 KiB | 5.02 MiB/s, done.
Resolving deltas: 100% (30/30), done.
```

### Exercise 1b

```bash
$ cd remotes_gne_exercises/

$ git remote -v
origin	https://github.com/twin-bridges/gne_exercises_aug25 (fetch)
origin	https://github.com/twin-bridges/gne_exercises_aug25 (push)
```

### Exercise 1c

```bash
$ git remote add my_remote https://github.com/twin-bridges/gne_exercises_aug25
```

```bash
$ git remote -v
my_remote	https://github.com/twin-bridges/gne_exercises_aug25 (fetch)
my_remote	https://github.com/twin-bridges/gne_exercises_aug25 (push)
origin	https://github.com/twin-bridges/gne_exercises_aug25 (fetch)
origin	https://github.com/twin-bridges/gne_exercises_aug25 (push)
```

### Exercise 1d

```bash
$ git fetch my_remote
From https://github.com/twin-bridges/gne_exercises_aug25
 * [new branch]      branch-testing -> my_remote/branch-testing
 * [new branch]      main           -> my_remote/main
```

```bash
$ git branch -r
  my_remote/l4-testing
  my_remote/main
  origin/HEAD -> origin/main
  origin/l4-testing
  origin/main
```

