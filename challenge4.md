## Problem Domain
we need function tree as argument and check is symmetric or mirror (is mirror) .

---
- input : Tree
- Output : bool

---
## Edge Case :
- If Tree Is Empty

---
## Visual :
```
Input :

               1
            /     \
           2         2
        /    \     /   \
       3      4   4     3

```

```
Output :
    True
```

---
```
Input :

        1
     /     \
   2         2
     \         \
      3         3

```

```
Output :
    False
```

---
## Algorithm : 
- Create A Function Takes tree .
- inside f1 create f2 takes two argument .
- check if tree is empty -> return "Empty"
- check if r1 and r2 is not none ->
- check if r1.val equal r2.val -> return f2(r1.left, r2.right) and f2(r1.right, r2.left)
- return False
- f1 -> return f1(root, root)

---
## Code :
```
def symmetric(tree) :
    def mirror(r1, r2) :
        if r1 is None and r2 is None :
            return "Empty
        if (r1 is not None and r2 is not None) :
            if r1.val == r2.val :
                return (mirror(r1.left, r2.right) and mirror(r1.right, r2.left) )
        return False

    return mirror(tree.root, tree.root)
```

---
## big O : 
- Space : O(1)
- Time : O(n)

---
## [Back](./README.md)

---
