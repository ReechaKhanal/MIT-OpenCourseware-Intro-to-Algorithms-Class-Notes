
## Models of Computation, Document Distance

Algorithm - Computational procedure to solve some problems
          - Takes input | solves a problem | and computes an output
          
Model of Computation Says:
          - What your computer or algorithm is allowed to do or can do
          - how much does your algorithm cost (time and space)
          
##### Two Models of Computation

1. Random Access Machines (RAM):
        
        * Basically, a giant array from 0 to  4 gigs
        * You can access anyhing in there in constant time
        * RAM is usually organized by word (the size word)
        * Word - is w bit (32 or 64 or some other number say w bits)
        * In constant time, an algorithm can :
                                        * load constant number of words from the memory
                                        * do constant number of computations on them
                                        * and stores constant number of words in locations specified of registers

2. Pointer Machines:

        * Corresponds to Object-Oriented Programming in a very simple version
        * Here, we have dynamically allocated objects
        * An object has a constant number of fields - a field could be a word or a pointer
        * Pointer is something that points (references) to another object or has a special value - null (To relate think of linked lists)
        * In python, a double linked list is just an object with three attributes
        * Now you can use this pointer in the Random-Access Machine then this pointer becomes an index in a giant table.

A Pointer Machine is actually weaker than the Random-Access Machine because you can implement a pointer machine with the Random-Access Machine.


##### Python Model:

    - Python offers both the **Random Access Machine**  perspective (coz it has arrays) and **Pointer Machine** perspective (coz it has references or pointers).
    - You can do many operations, and they are not as simple as just the Random-Access machine or just the Pointer Machine (which takes constant time for any operation).

 ##### Python List:
 
    - Called as a list but implemented like an array
    - It is basically an array:
            L[i] = L[j]  + 5         ----> O(1) time
    - Object with O(1) attributes:
            x = x.next               ----> O(1) time
    
    - L.append(x) - python does something called table doubling and hence takes O(1) time.
    - L = L1 + L2 - O(len(L1) + O(len(L2) NOT A CONSTANT TIME is basically appending one by one to L()
    
    So, one way to think about the time consumption is to think how a function in python is implemented in relation to the standard constant time functions.
    
    - x in List: Linear O(N)
    - len(L) - constant               ----> O(1) time
             - In python, lists are built with a counter built-in which is maintained as we move on with the lists
    - L.sort() - sort a list - O(NlogN)
 
##### Python List:

    - D[key] = value - O(1) constant time - with high probability
    - Key in dictionary - Constant time
    - In dictionary, most of the time we deal with constant time while playing with single key
    - Dictionary - a really effective way to solve problems
    
    
    
