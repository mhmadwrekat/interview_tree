## Problem Domain
We Need Function To Find Minimum Number In Tree .

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
        20
      /   \
     20     10
    / \    
   40   50    
```

```
Output :
    10

```

---
## Algorithm : 
- Create afunction takes tree as argument .
- if root is none return Empty
- we need to find maximum of 3 value : root / left / right
- res = root.value
- left = f(r.left)
- right = f(r.right)
- check if left < res -> res = left
- check if right < res -> res = right
- return res

---
## Code :
```
def find_min_in_BT(root):
    if root is None:
        return float('inf')
    res = root.value
    lres = find_min_in_BT(root.left)
    rres = find_min_in_BT(root.right)
    if lres < res:
        res = lres
    if rres < res:
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
