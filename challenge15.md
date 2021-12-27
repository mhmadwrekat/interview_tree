## Problem Domain
We Need Function To Check its BT or BST .

---
- input : tree
- Output : str

---
## Edge Case :
- If Any Tree Is Empty

---
## Visual :
```
Input : 
        4
      /   \
     2     5
    / \    
   1   3    
```

```
Output :
    If BST Return True
    If BT Return False

```

---
## Algorithm : 
- Create Function take tree and left = None and right = None
- if root is none return true
- if left != None and root.value <= left.value -> Return False
- if right != None and root.value >= right.value -> Return False
- Check recursively for every node .
    - return f(root.left, l, root) and f(root.right, root , right)

---
## Code :
```
def isBST(root, l = None, r = None):
    if (root == None) :
        return True
    if (l != None and root.data <= l.data) :
        return False
    if (r != None and root.data >= r.data) :
        return False
    return isBST(root.left, l, root) and isBST(root.right, root, r)
```

---
## big O : 
- Space : O(1)
- Time : O(n)

---
## [Back](./README.md)

---
