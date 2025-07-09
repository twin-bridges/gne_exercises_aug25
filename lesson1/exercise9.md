### Exercise 9a

```shell
$ vi simple.py
----
# Modify 'simple.py' file
print("Hello world")
for x in range(100):
    print(x)

$ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   simple.py

no changes added to commit (use "git add" and/or "git commit -a")
```

### Exercise 9b

```diff
$ git diff
diff --git a/lesson1/simple.py b/lesson1/simple.py
index 44159b3..28ded6a 100644
--- a/lesson1/simple.py
+++ b/lesson1/simple.py
@@ -1 +1,3 @@
 print("Hello world")
+for x in range(100):
+    print(x)
```

### Exercise 9c

```shell
$ git add simple.py 

$ git commit -m "Updating simple.py script"
[main af1793c] Updating simple.py script
 1 file changed, 2 insertions(+)
```
