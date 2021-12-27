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
        1
      /   \
     2     3
    / \   / \
   4   5 6   7
          \
           8

```

```
Output :
Sum = 4 + 5 + 8 + 7 = 24            
```

---
## Algorithm : 
- Create afunction takes tree as argument .
- if root is none return empty .
- we define global total
- if r.left and r.right is None -> total += r.value
- f(r.left)
- f(r.right)

---
## Code :
```
def leafSum(root):
    global total
    if root is None:
        return
    if (root.left is None and root.right is None):
        total += root.value
    leafSum(root.left)
    leafSum(root.right)
```

---
## big O : 
- Space : O(1)
- Time : O(n)

---
## [Back](./README.md)

---
