## Insertion Sort

  For i = 1, 2, ... n
  
  IDEA:
  
       Insert A\[i] into the sorted array - where you have sorted A\[0:i-1]
       And this will be done by pairwise swaps done to the correct position.
  
  
  Worst Case Complexity: O(n^2)
  
        It could be n movements and at any step we might have to do n/2 movements or swaps
  
  - But we can take Insertion Sort and turn it into an O(nlogn) algorithm if we mix it up with binary search
  - This is called Binary Insertion Sort


Note: here the complexity is O(nlogn). - This is more of a compare complexity

  When we look at the swaps we still need to do - the complexity still needs to be O(n^2)
  
            
            
  
