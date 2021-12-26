## Problem Domain
We Need Function To Mergeg Two Trees

---
- input : Two Trees
- Output : Merged tree

---
## Edge Case :
- If Any Tree Is Empty

---
## Visual :
```
Input :
    Tree 1 :               Tree 2 :
       1                       2
    /     \                  /   \
   3       2                1     3
  /                           \     \
5                               4     7

```

```
Output :
       3             
    /     \          
   4       5
  / \        \              
5    4         7                  
```

---
## Algorithm : 
- Create A Function Takes Two Tree .
- check if tree 1 is empty -> return "Empty"
- check if tree 2 is empty -> return "Empty"
- we assign r1.value += r2.value
- r1.left = function(r1.left, r2.left)
- r1.right = function(r1.right, r2.right)
- return r1

---
## Code :
```
def mergeinone(root1,root2):
        if (not root1):
           return root2
        if (not root2):
           return root1

        root1.value+=root2.value
        root1.left=mergeinone(root1.left,root2.left)
        root1.right=mergeinone(root1.right,root2.right)
        return root1
```

---
## big O : 
- Space : O(1)
- Time : O(n)

---
## [Back](./README.md)

---
