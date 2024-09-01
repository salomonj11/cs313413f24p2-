Project 2 - Summary AKA TLDR

Code Questions Answered (TEST ITERATOR)
- Does using a LinkedList make a difference?
  Using LinkedList can improve performance during removal operations, but for iteration and summing values, the performance differences are minimal.
- What happens if you use list.remove(Integer.valueOf(77))?
  It only removes the first occurrence of 77, while Iterator.remove() removes all occurrences of 77 during iteration.

Code Questions Answered (TEST LIST)
- Does using a LinkedList make a difference?
  - Access Time: LinkedList is generally slower for random access (O(n)) compared to ArrayList (O(1)) due to the need to traverse nodes.
  - Insertion and Removal: LinkedList can be more efficient for insertions and removals, especially in the middle of the list or during iteration, due to its O(1) time complexity for these operations. However, ArrayList might be more efficient when access speed is critical.
  - Specific Tests: In tests like testSizeNonEmpty, testSet, and testSubList, where index-based access is key, ArrayList performs better. In tests like testRemoveObject and testRemoveAll, LinkedList might have an edge due to more efficient removals.

Code Questions Answered (TEST PERFORMANCE)

Performance Observations:

- Access Operations (testArrayListAccess and testLinkedListAccess):
  - ArrayList: Consistently provides fast access times as expected, with performance improving as the list size increases. This aligns with its O(1) access time due to direct indexing.
  - LinkedList: Performance is slower than ArrayList for access operations, especially at smaller sizes, due to the O(n) access time that requires traversing nodes.

- Add/Remove Operations (testArrayListAddRemove and testLinkedListAddRemove):
  - ArrayList: Performs poorly for add/remove operations at the start of the list for smaller sizes (10, 100) due to the need to shift elements (O(n) complexity). However, as the size increases, the time difference becomes less noticeable.
  - LinkedList: Excels in add/remove operations, particularly at larger sizes, due to its O(1) complexity for adding/removing elements at the start of the list. This efficiency is particularly noticeable as the list size increases.

Detailed Results:

- For Size 10, REPS 1,000,000:
  - ArrayList Access: 18 ms
  - LinkedList Add/Remove: 43 ms
  - LinkedList Access: 12 ms
  - ArrayList Add/Remove: 44 ms

- For Size 100, REPS 100,000:
  - ArrayList Access: 75 ms
  - LinkedList Add/Remove: 115 ms
  - LinkedList Access: 24 ms
  - ArrayList Add/Remove: 114 ms

- For Size 1,000, REPS 10,000:
  - ArrayList Access: 5 ms
  - LinkedList Add/Remove: 11 ms
  - LinkedList Access: 10 ms
  - ArrayList Add/Remove: 6 ms

- For Size 10,000, REPS 1,000:
  - ArrayList Access: 15 ms
  - LinkedList Add/Remove: 2 ms
  - LinkedList Access: 4 ms
  - ArrayList Add/Remove: 6 ms

Summary of Summary:

- ArrayList is more efficient for access operations due to its O(1) access time.
- LinkedList is more efficient for add/remove operations at the beginning of the list due to its O(1) complexity for these operations.
- As the size increases, the differences in performance for both access and add/remove operations become more pronounced, highlighting the strengths and weaknesses of each list implementation.
