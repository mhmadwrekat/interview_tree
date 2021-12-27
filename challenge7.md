## Problem Domain
Check if a Binary Tree has duplicate values .

---
- input : tree
- Output : bool

---
## Edge Case :
- If Any Tree Is Empty

---
## Visual :
```
Input :
         1
       /   \
      2     3
             \
              2               

```

```
Output :
    True                
```

---
## Algorithm : 
- Create Two Function :
- f1 Takes Tree and s as argument .
- check if tree is empty -> return "Empty"
- check If current node's data is already present -> return true
- Insert current node
- return Recursively check in left and right

---
## Code :
```
def checkDupUtil( root, s) :
    if (root == None) :
        return False
    if root.data in s:
        return True
    s.add(root.data)
    return checkDupUtil(root.left, s) or checkDupUtil(root.right, s)

```

---
## big O : 
- Space : O(1)
- Time : O(n)

---
## [Back](./README.md)

---
