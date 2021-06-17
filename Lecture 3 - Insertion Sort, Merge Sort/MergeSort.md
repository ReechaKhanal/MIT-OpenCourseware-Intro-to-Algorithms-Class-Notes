## Merge Sort:


- A divide and conquer algorithm:

      - Divide into smaller arrays
      - Compare, swap and merge

- From a top level:
      
      - Merge is going to assume we have two sorted arrays and merge it togehter.
      - Can utilize the two-pointer algorithm to merge
      - Most of the work will be done in merging part of the code
      - Rest of the body will just be a recursive call


- Here:

      - the merge step complexity - O(n)
      - Recursion takes O(log(n)) complexity

      - Total complexity O(nlog(n))
      
Note:

  In a recursion tree like this:
          Number of depth - 1 + log(n)
          Number of leaves - n
          Complexity: O(nlogn)
    
