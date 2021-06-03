## Peak Finding Algorithm:

    - This algorithm runs on an array of numbers, the numbers being positive or negative
    
    - AIM: To Find a Peak in the Array
        
          > For a array [a, b, c] --> element b is a peak if b >= a and b >= c
        
          > Peak here is a local property and a trivial one - you just need to look left and right.
   
 ### Problem Statement: Find if a Peak Exists
 
 #### GENERIC PEAK FINDING ALGORITHM:
 
      STEP ONE: Start from the left 
      
      STEP TWO: Walk Across the Array
      
      STEP THREE: 
      
            a. If Things are Intially Increasing Peak is a place where it starts decreasing.
            
            b. If Things are Intially Decreasing Peak is a place where it starts decreasing.
      
      
      Worst Case Time Complexity: O(N) / linear
      
#### Getting the Asymptotic Complexity of this algorithm down with divide and conquer strategy.

    ###### Binary Search Algorithm:
        
          STEP ONE: Look at the middle part and then look at the left and right in the array
          
          STEP TWO: 
          
                If array[mid] < array[mid-1]:
                        - Mid value is less than the value before it
                        - You can look towards the left half to find a peak now
                
                Else If array[mid] < array[mid+1]:
                        - Mid value is less than the value after it
                        - You can look towards the right half to find a peak
                
                Else:
                      - This is your peak
     
     
          This is an example of divide and conquer.
          
          Asymptotic Time Complexity: O(log(n))
          

NOTE: 
    For an input of 10 million difference between O(n) and O(log(n)) is a difference of 13 seconds vs 0.001 seconds.
          
