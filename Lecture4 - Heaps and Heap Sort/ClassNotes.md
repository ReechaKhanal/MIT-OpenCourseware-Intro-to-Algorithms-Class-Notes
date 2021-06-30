### Heaps:

   * We use heaps to implement a Priority Queue
   * And implementing a sorting algorithm, heap sort


### Priority Queue:

   * Implement a set S of elements, and each of these elements is associated with a key.
   * You queue up for something, you have certain priorities assigned:
    
          o	You want to pick Max or Min priority from the queue
          o	Delete from queue 
          o	Insert into a queue
          o	Also change priorities in the queue
    
    
   * We will further look into Asymptotic complexity of these.
   
Our GOALS from the heap:
  
    1. Insert (S, x): insert element x into the set S
    2. Max (S): return the element of S with the largest key
    3. Extract_Max (S): returns and removes the element of S with largest key
    4. Increase_Key (S, x, k): Increase the value of X's key to the new value 'k'.
    
    Similarly, a decrease key might be useful too.
    

### Heap:

   * An implementation of the Priority Queue
   * An array structure, except that you are visualizing the array as a nearly complete binary tree.
    
    
   * Example:
        
          * Array - 16, 14, 10, 8, 7, 9, 3, 2, 4, 1  [A randonly ordered array, NOT sorted]
          
          * We here have 10 elements, a binary tree would need to have 15 elements in it to be a complete binary tree. 
            Hence, comes the term "nearly complete binary tree" - becuse we want to work on general cases of an arbitary sized array,
            not only the arrays capable of making a complete binary tree.
           
          * To visualize the array as a tree:
          
                  Index 1 - root
                  Index 2, 3 - children of roow
                  Index 4, 5, 6, 7 - children of 2 and 3
                  
          * This is a heap structure
          * We have a tree representation of an array


### Heap as a Tree:

    •	Root of the tree = first element (i=1)
    •	Parent (i) = i/2
    •	Left Child (i) = 2i
    •	Right Child (i) = 2i +1


### Max Heap Property:
    
    •	The key of a node is greater than or equal to the keys of its children
          Key(Parent) >= Key(Children)


### Min Heap Property:
    
    •	The key of a node is greater than or equal to the keys of its children
          Key(Parent) <= Key(Children)
    
*********************     

Finding the biggest element will be trivially performed on a maxheap - just return the root 

Extracting might not be so simple as you will have to maintain a Max Heap property once you remove the max element.

*********************




          

    

      
