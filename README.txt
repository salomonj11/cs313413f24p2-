# Project 2 - Summary AKA TLDR

## Code Questions Answered (TEST ITERATOR)
- **Does using a `LinkedList` make a difference?**
  Using `LinkedList` can improve performance during removal operations, but for iteration and summing values, the performance differences are minimal.
- **What happens if you use `list.remove(Integer.valueOf(77))`?**
  It only removes the first occurrence of `77`, while `Iterator.remove()` removes all occurrences of `77` during iteration.

## Code Questions Answered (TEST LIST)
- **Does using a `LinkedList` make a difference?**
  - **Access Time**: `LinkedList` is generally slower for random access (O(n)) compared to `ArrayList` (O(1)) due to the need to traverse nodes.
  - **Insertion and Removal**: `LinkedList` can be more efficient for insertions and removals, especially in the middle of the list or during iteration, due to its O(1) time complexity for these operations. However, `ArrayList` might be more efficient when access speed is critical.
  - **Specific Tests**: In tests like `testSizeNonEmpty()`, `testSet()`, and `testSubList()`, where index-based access is key, `ArrayList` performs better. In tests like `testRemoveObject()` and `testRemoveAll()`, `LinkedList` might have an edge due to more efficient removals.