## Document Distance Problem

### Statement: Find the distance between two documents D1 and D2 - d(D1, D2)

### Examples where this Algorithm can be used:
    
    Suppose you are Google and you are cataloging webpages and there will be there will be
    time when you want to say two webpages are the same.
    
    You want to detect if two solutions are identical. - Cheating in classroom (Plagarism)
    
    Web Search - If I am searching for “Introduction to Algorithm”, You want to put in the top 
      the ones most similar to what I am searching for, basically ones with the least distance.
   
### Further Thought:
  
   This can be thought of as a simple decomposition of documents into words.
    
   #### Idea: To find distance look at the shared words.
   
        Document is sequence, but then it can also be thought of as a vector.
        
        D[w] = number of occurrences of the word w in D.
        
        Can be thought of a giant vector that is indexed by words, for each of them there is some 
        frequency 0 to multiple. 
        
            Example:    
                  D1 = \"the cat\"
                  D2 = \"the dog\"
    
                  D1[the] = 1
                  D1[cat] = 1
                  D1[dog] = 0
   
                  D2[the] = 1
                  D2[cat] = 0
                  D2[dog] = 1
        
        Here, we have our two vectors D1 and D2.
        
    
  #### To Solve: Now, how do we see how different these vectors are from each other.
  
        Approach 1:
          
            d(D1, D2) = D1.D2
                      = Sum(D1[w].D2[w])
            
            So, when two matches you get "1". If not, you get a "0".
            
            Higher Number - More things in Common
            
            Lower Number - Less things in Common
            
   Additional Problem: If you have a very long document with millions of words.
          
            Additionally, I have another one with half words in common – giving these two documents a very high score – let’s say 500,000.
            
            Now I have two documents with around 100 words which are identical, but their score is only 100.
            
            Doesn’t feel like a perfect measure, is not scaling very well.
   
   Solution Idea:
   
            * Divide by length of the vectors
            * Kind of brings it in scale now the big numbers dont matter now much
            
            Hence:
                
                  d(D1, D2) = (D1.D2)/|D1||D2|
                  
            This is very close to the formula for finding the angle of the vector
            
            If the angle is close to zero, the vectors are very similar. If 90 degrees  - very different
            
            
   
   Three main things we need to do:
   
        1. Decompose or split the documents into list of words
        2. Compute word frequencies or how many times each word appears
        3. Compute the dot product
        
   
   ALGORITHM:
   
     Just run through it and count the words.
                

            
        
          
   

    
