## Problem Domain
We need function to Finding the maximum depth of a binary tree .

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
    3    
```

---
## Algorithm : 
- Create afunction takes tree as argument .
- if root is none return empty .
- Get the depth of the left and right subtree using recursion.
- left = f(r.left)
- right = f(r.right)
- check if left > right -> return left+1 
- else that -> return right+1
- if r.left and r.right is None -> total += r.value
- f(r.left)
- f(r.right)

---
## Code :
```
def maxDepth(node):
    if node is None:
        return -1 ;
    else :
        lDepth = maxDepth(node.left)
        rDepth = maxDepth(node.right)
        if (lDepth > rDepth):
            return lDepth+1
        else:
            return rDepth+1
```

---
## big O : 
- Space : O(1)
- Time : O(n)

---
## [Back](./README.md)

---
