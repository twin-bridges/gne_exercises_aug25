
### Exercise 3b

```bash
# You can see that I am on the 'main' branch in the 'commit'
$ git add my_script.py 
$ git commit -m "Adding my_script.py"
[main 1feaab6] Adding my_script.py
 1 file changed, 3 insertions(+)
 create mode 100644 lesson2/my_script.py
```

### Exercise 3c

```bash
$ git branch
* main

# Create and checkout the 'l3-feature3' branch
$ git checkout -b l3-feature3 main
Switched to a new branch 'l3-feature3

$ git branch
* l3-feature3
  main

$ vi my_script.py
```

### Exercise 3d

```bash
$ git add my_script.py 

$ git commit -m "Changing IP address in my_script.py"
[l3-feature3 8eadc5c] Changing IP address in my_script.py
 1 file changed, 1 insertion(+), 1 deletion(-)
```

### Exercise 3e/3f

```bash
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

$ vi my_script.py

# Once again can see that I am on 'main' branch from the 'commit' command
$ git add my_script.py 

$ git commit -m "Prompt user for IP address in my_script.py"
[main 25b69b6] Prompt user for IP address in my_script.py
 1 file changed, 1 insertion(+), 1 deletion(-)
```

### Exercise 3g

```bash
$ git branch
  l3-feature3
* main
```

```bash
# Merge conflict!
$ git merge l3-feature3
Auto-merging lesson2/my_script.py
CONFLICT (content): Merge conflict in lesson2/my_script.py
Automatic merge failed; fix conflicts and then commit the result.
```

```python
# I here resolved the merge conflict by editing the 'my_script.py' file to be:
ip_addr = input("Enter IP address: ")
if not ip_addr:
    ip_addr = "10.1.1.1"
for octet in ip_addr.split("."):
    print(octet)
```

```bash
$ git add my_script.py 
$ git commit -m "Fixing merge conflict (lesson2)"
[main 9f0ed63] Fixing merge conflict (lesson2)
```

### Exercise 3h

```bash
$ git log --oneline --graph --decorate
*   9f0ed63 (HEAD -> main) Fixing merge conflict (lesson2)
|\  
| * 8eadc5c (l3-feature3) Changing IP address in my_script.py
* | 25b69b6 Prompt user for IP address in my_script.py
|/  
* 1feaab6 Adding my_script.py
* f2cb4ef (origin/main) Lesson2 exercises
*   cabbf18 Merge branch 'l3-feature2'
|\  
| * e975a60 l3-feature2: commit2
| * 4da9aa6 l3-feature2: commit1
* | 2755c6a Commit in 'main' to force a 3-way merge
|/  
* 51423ed l3-feature1: commit2
* 11132d3 l3-feature1: commit1
```

### Exercise 3i

```bash
$ git branch
  l3-feature3
* main

$ git branch -d l3-feature3
Deleted branch l3-feature3 (was 8eadc5c).

$ git branch
* main
```

