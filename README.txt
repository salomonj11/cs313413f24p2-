# Project 2 - Summary AKA TLDR

## Code Questions Answered
- **Does using a `LinkedList` make a difference?**
  Using `LinkedList` can improve performance during removal operations, but for iteration and summing values, the performance differences are minimal.
- **What happens if you use `list.remove(Integer.valueOf(77))`?**
  It only removes the first occurrence of `77`, while `Iterator.remove()` removes all occurrences of `77` during iteration.