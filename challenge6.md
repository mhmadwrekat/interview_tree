## Problem Domain
We Need Function To check if the binary tree is univalued or not .

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
    /     \             
   1       1              
  /                       
1                            

```

```
Output :
    True                
```

---
## Algorithm : 
- Create A Function Takes Tree as argument .
- check if tree is empty -> return "Empty"
- check if r.left not equal None and root.value not equal left.value -> Return False
- check if r.right not equal None and root.value not equal right.value -> Return False
- return function(r.left) and function(r.right)

---
## Code :
```
def isUnivalTree(root):
	if (not root):
		return True
	if (root.left != None and root.data != root.left.data):
		return False
	if (root.right != None and root.data != root.right.data):
		return False
	return isUnivalTree(root.left) and isUnivalTree(root.right)
```

---
## big O : 
- Space : O(1)
- Time : O(n)

---
## [Back](./README.md)

---
