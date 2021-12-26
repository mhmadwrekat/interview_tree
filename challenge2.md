## Problem Domain
we need function to invert binary tree

---
- input : Tree
- Output : invert tree

---
## Edge Case :
- If Tree Is Empty

---
## Visual :
```
Input :

               4
            /     \
           2         7
        /    \     /   \
       1      3   6     9

```

```
Output :
               4
            /     \
           7         2
        /    \     /   \
       9      6   3     1
```

---
## Algorithm : 
- Create A Function Takes Tree as Argument
- Check if root is empty return 'Empty'
- use breadth first to re order the nodes
- call the function reverse to swap the left and the right 
- call the function recursively for the root.left and root.right

---
## Code :
```
def invert(root) :
    if not root :
        return "Empty"
    root.left, root.right = root.right, root.left
    invert(root.left)
    invert(root.right)
    return root
```

---
## big O : 
- Space : O(1)
- Time : O(n)

---
## [Back](./README.md)

---