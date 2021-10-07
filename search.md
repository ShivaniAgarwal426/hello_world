# search an element in an array #2495


Searching Algorithms are designed to check for an element or retrieve an element from any data structure where it is stored. 
Searching algorithms is a basic, fundamental step in computing done via step-by-step method to locate a specific data among a collection of data.

All search algorithms make use of a search key in order to complete the procedure. And they are expected to return a success or a failure status ( in boolean true or false value).


<br><br>

### Definition of Search Algorithm:
> Any algorithm which solves the search problem, namely, to retrieve information stored within some data structure, or calculated in the search space of a problem domain, either with discrete or continuous values.
 

In computer science, there are various type of search algorithms available based on the type of search operation, these algorithms are generally classified into two categories:

1. **Sequential Search:** In this, the list or array is traversed sequentially and every element is checked. 
    <br>Also known as `Linear Search`.
2. **Interval Search:**  It is much more efficient than Linear Search algorithm as they repeatedly target the center of the search structure and divide the search space in half. 
    <br>Also known as `Binary Search`.
    > **NOTE-**  <br>
    > These algorithms are specifically designed for searching in sorted data-structures.
    
    
<br><br><br><br>
           
## 1. Linear Search

   - Linear search is a very simple search algorithm. 
   - In this type of search, a sequential search is made over all items one by one. 
   - Every item is checked and if a match is found then that particular item is returned, otherwise the search continues till the end of the data collection.

 
   > **Algorithm:**
   > 
   ```bash
   Linear Search ( Array A, Value x)
   
   Step 1: Set i to 1
   Step 2: if i > n then go to step 7
   Step 3: if A[i] = x then go to step 6
   Step 4: Set i to i + 1
   Step 5: Go to Step 2
   Step 6: Print Element x Found at index i and go to step 8
   Step 7: Print element not found
   Step 8: Exit
   ```    

   <div align="center"><img src="https://user-images.githubusercontent.com/70523057/136211029-e7396a00-f18a-40f3-b8a5-8380d63574e2.gif" width="450" ></div>
     
   **Example:**
   > 
   > _Program:_
   ```bash
   <script>
   function search(arr, n, x){
   	let i;
   	for (i = 0; i < n; i++)
   		if (arr[i] == x)
   			return i;
   	return -1;
   }
   
   // Main code
   	let array = [ 10, 40, 100, 303, 6, 22 ];
   	let search_element = 6;
   	let n = array.length;
   
   	// Function call
   	let result = search(array, n, search_element);
   	(result == -1) ? document.write("Element is not present in array") : document.write("Element is present at index " + result);
   
   </script>
   ```
 
   > _Output:_  <br>
   <img src="https://user-images.githubusercontent.com/70523057/136373552-ba9e0478-a8e3-44b0-bdec-ad5bd40f649d.png" width="600" >
   
   
   **Time Complexity:**  <br>
    1. Best Case - O(1)  <br>
    2. Average Case - O(n/2)  <br>
    3. Worst Case - O(n)  <br>
  
  
  
  
## 2. Binary Search
   - Search a sorted array by repeatedly dividing the search interval in half. 
   - Begin with an interval covering the whole array. 
   - If the value of the search key is less than the item in the middle of the interval, narrow the interval to the lower half. 
   - Otherwise, narrow it to the upper half. 
   - Repeatedly check until the value is found or the interval is empty. 
  
   `NOTE:` 
   :-
   Binary search method is considered as the best searching algorithms. There are other search algorithms such as the depth-first search algorithm, breadth-first algorithm, etc. The efficiency of a search algorithm is measured by the number of times a comparison of the search key is done in the worst case.
 
  
  
     
   **Example:**
   > 
   > _Program:_
   > 
   > _Output:_
   > 
   **Time Complexity:**
  
