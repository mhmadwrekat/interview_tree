## Problem Domain
we need function takes two tree as argument and check if they are the same or not .

---
- input : Two Tree
- Output : bool

---
## Edge Case :
- If any of the Tree Is Empty

---
## Visual :
```
Input :

   1              1
 /   \         /     \
2     3       2       3

```

```
Output :
    True
```

---
## Algorithm : 
- Create A Function Takes Two Tree as Argument
- Check if any of two tree is empty return 'Empty'
- check if t1.value != t2.value -> return false
- return the function with(t1.right, t2.right) and function with(t1.left, t2.left)

---
## Code :
```
def isSame(t1, t2) :
    if not t1 and not t2 :
        return "Empty"
    if not t1 or not t2 :
        return "Empty"
    if t1.val != t2.val :
        return False
    return isSame(t1.right, t2.right) and isSame(t1.left, t2.left)
```

---
## big O : 
- Space : O(1)
- Time : O(n)

---
## [Back](./README.md)

---