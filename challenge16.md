## Problem Domain
We Need Function takes BST and return second largest value .

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
       50
     /     \
    30      70
    / \    /  \
   20 40  60  80
```

```
Output :
    70

```

---
## Algorithm : 
- we need Two Function , f1 take BST as argument
- we Declare c = [0]
- and we call f2(BST, c)
- f2 takes BST and list as argument
- check if root equal none or c[0] >= 2 -> return 0
- f2(r.right, c)
- Increment count of visited nodes / c[0] += 1
- If c becomes k now, then this is the 2nd largest // if c[0] == 2 : return root.key
- f2(r.left, c)

---
## Code :
```
def secondLargest(root):
    c = [0]
    secondLargestUtil(root, c)

def secondLargestUtil(root, c):
    if root == None or c[0] >= 2:
        return 0
    secondLargestUtil(root.right, c)
    c[0] += 1
    if c[0] == 2:
        return root.key
    secondLargestUtil(root.left, c)
```

---
## big O : 
- Space : O(1)
- Time : O(n)

---
## [Back](./README.md)

---
