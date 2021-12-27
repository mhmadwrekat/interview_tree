## Problem Domain
We need function to Finding the maximum depth of a binary tree .

---
- input : tree , int
- Output : bool

---
## Edge Case :
- If Any Tree Is Empty

---
## Visual :
```
Input : 
        10
      /   \
     8     2
    / \   / 
   3   5 2   
```
21 –> 10 – 8 – 3 
23 –> 10 – 8 – 5 
14 –> 10 – 2 – 2

```
Output :

21 -> True / 23 -> True / 14 -> True
other that is False 

```

---
## Algorithm : 
- Create afunction takes tree and int as argument .
- if root is none return empty .
- Declare sum = 0 / subsum = int - tree.root.value
- If we reach a leaf node and sum becomes 0, then return True
- Otherwise check both subtrees
- return sum

---
## Code :
```
def hasPathSum(node, s):
        ans = 0
        subSum = s - node.data
        if(subSum == 0 and node.left == None and node.right == None):
            return True
        if node.left is not None:
            ans = ans or hasPathSum(node.left, subSum)
        if node.right is not None:
            ans = ans or hasPathSum(node.right, subSum)
        return ans
s = 14
if hasPathSum(root, s):
    print (True)
else:
    print (False)
```

---
## big O : 
- Space : O(1)
- Time : O(n)

---
## [Back](./README.md)

---
