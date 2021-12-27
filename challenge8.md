## Problem Domain
We need function that return Sum of all nodes in a binary tree .

---
- input : tree
- Output : int

---
## Edge Case :
- If Any Tree Is Empty

---
## Visual :
```
Input :
          15
       /      \
      10      20
    /   \   /   \
    8   12  16   25  

```

```
Output :
    106              
```

---
## Algorithm : 
- Create afunction takes tree as argument .
- if root is none return empty .
- return root.value + func(root.left) + func(root.right)

---
## Code :
```
def addBT(root):
    if (root == None):
        return 0
    return (root.value + addBT(root.left) +
                       addBT(root.right))
```

---
## big O : 
- Space : O(1)
- Time : O(n)

---
## [Back](./README.md)

---
