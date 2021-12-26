## Problem Domain
check if a binary tree is subtree of another binary tree

---
- input : Two Tree
- Output : Bool

---
## Edge Case :
- If Tree Is Empty

---
## Visual :
```
TREE 1 :

              26
            /   \
          10     3
        /    \     \
      4      6      3
       \
        30
```
```
TREE 2 :

          10
        /    \
      4      6
       \
        30
```

---
## Algorithm : 
- we need two function :
1. f1 take two root :
    - // Base Case
   - if r1 is None and r2 is none : return true
   - if r1 is None or r2 is None : return false
   - // Check if the data of both roots is same and data of left and right subtrees are also same
   - return (r1.data == r2.data and
            f1(r1.left , r2.left)and
            f1(r1.right, r2.right)
            )
2. f2 takes two tree(T, S)
    - // Base Case
    - if S is None -> return True
    - if T is None -> return False
    - // Check the tree with root as current node
    - if ( f1 ( T , S )) : return True
    - // IF the tree with root as current node doesn't match then try left and right subtreee one by one
    - return f2(T.left, S) or f2(T.right, S)

---
## Code :
```
def areIdentical(root1, root2):
    if root1 is None and root2 is None:
        return True
    if root1 is None or root2 is None:
        return False 
    return (root1.data == root2.data and
            areIdentical(root1.left , root2.left)and
            areIdentical(root1.right, root2.right)
            )
```

```
def isSubtree(T, S) :
    if S is None:
        return True
    if T is None:
        return False
    if (areIdentical(T, S)) :
        return True
    return isSubtree(T.left, S) or isSubtree(T.right, S)
```

---
## big O : 
- Space : O(n)
- Time : O(mn) : where m and n are number of nodes in given two trees . 

---
## [Back](./README.md)
