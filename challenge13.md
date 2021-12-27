## Problem Domain
We Need Function To Find Largest Number In Tree .

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
        10
      /   \
     20     30
    / \    
   40   50    
```

```
Output :
    50

```

---
## Algorithm : 
- Create afunction takes tree as argument .
- if root is none return Empty
- we need to find maximum of 3 value : root / left / right
- res = root.value
- left = f(r.left)
- right = f(r.right)
- check if left > res -> res = left
- check if right > res -> res = right
- return res

---
## Code :
```
def findMax(root):
    if (root == None):
        return 0
    res = root.value
    lres = findMax(root.left)
    rres = findMax(root.right)
    if (lres > res):
        res = lres
    if (rres > res):
        res = rres
    return res
```

---
## big O : 
- Space : O(1)
- Time : O(n)

---
## [Back](./README.md)

---
