## Problem Domain
Breadth First 

---
- input : tree
- Output : List

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
    / \    
   4   5    
```

```
Output :
[1, 2, 3, 4, 5]

```

---
## Algorithm : 
- Create afunction takes tree and int as argument .
- queue = Queue()
- output = []
- if root is none return empty .
- Else -> queue.enqueue(tree.root)
- while not queue.is_empty() :
- front equal enqueue.dequeue()
- output.append(front.value)
- check if front.left -> queue.enqueue(front.left)
- check if front.right -> queue.enqueue(front.right)
- return output

---
## Code :
```
def breadth_first(tree):
    queue=Queue()
    final_output = []
    if  tree.root:
            queue.enqueue(tree.root)
    else:
        return "there is no root "

    while not queue.is_empty():
        front=queue.dequeue()
        final_output.append(front.value)
        if front.left :
                queue.enqueue(front.left)
        if front.right :
                queue.enqueue(front.right)
    return final_output
```

---
## big O : 
- Space : O(1)
- Time : O(n)

---
## [Back](./README.md)

---
