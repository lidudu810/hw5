# Sort Analysis Data

## Results Table
Make sure to go out to at least 100,000 (more are welcome), and you have 10 different values (more welcome). You are welcome to go farther, but given 100,000 can take about 20 seconds using a selection sort on a fast desktop computer, and 200,000 took 77 seconds, you start having to wait much longer the more 0s you add. However, to build a clearer line, you will want more data points, and you will find merge and quick are able to handle higher numbers easier (but at a cost you will explore below). 

You are free to write a script to run the program and build your table (then copy that table built into the markdown). If you do that, please include the script into the repo.  Note: merge sort is going to be completed in the workshop for Module 06. You can start on it now, but welcome to wait.

### Table
![Alt text](Screenshot%202023-03-12%20at%2010.49.42%20PM.png)


## BigO Analysis  / Questions

### 1. Build a line chart
Build a line chart using your favorite program. Your X axis will be N increasing, and your Y access will be the numbers for each type of sort. This will create something similar to the graph in the instructions, though it won't be as smooth.

Include the image in your markdown. As a reminder, you save the image in your repo, and use [image markdown].

![Alt text](vscode-local:/Users/lidudu/Desktop/NEU/CS5008_5009/CS508/hw05-sort-comparison-main/Sorts%20Analysis.png)


### 2. Convinced?
Given the direction of the line chart, are you "convinced" of the complexity of each of the sorts? Why or why not?

The direction of the line chart and the data in the table provide convincing evidence for the time complexity of each of the sorting algorithms. Bubble sort has the highest time complexity, selection sort and insertion sort have a lower but still steep time complexity, while merge sort and quicksort have a significantly lower time complexity. This supports the expected time complexity of each algorithm, with merge sort and quicksort being the most efficient for large data sets.

### 3. Big O
Build another table that presents the best, worst, and average case for Bubble, Selection, Insertion, Merge, and Quick. You are free to use resources for this, but please reference them if you do. 

![Alt text](vscode-local:/Users/lidudu/Desktop/Screenshot%202023-03-12%20at%2011.00.20%20PM.png)
Source: GeeksforGeeks (https://www.geeksforgeeks.org/time-complexities-of-all-sorting-algorithms/)

#### 3.2 Worst Case
Provide example of arrays that generate _worst_ case for Bubble, Selection, Insertion, Merge Sorts

~Bubble Sort: An array that is sorted in reverse order would generate the worst case for bubble sort. For example, [5, 4, 3, 2, 1].

~Selection Sort: An array that is sorted in reverse order would also generate the worst case for selection sort. For example, [5, 4, 3, 2, 1].

~Insertion Sort: An array that is sorted in reverse order and has the smallest element at the end of the array would generate the worst case for insertion sort. For example, [5, 4, 3, 2, 1].

~Merge Sort: An array that is sorted in reverse order would generate the worst case for merge sort. For example, [5, 4, 3, 2, 1].

~Quick Sort: An array that is sorted in reverse order or already sorted would generate the worst case for quick sort. For example, [5, 4, 3, 2, 1] or [1, 2, 3, 4, 5].

#### 3.3 Best Case
Provide example of arrays that generate _best_ case for Bubble, Selection, Insertion, Merge Sorts 

~Bubble Sort: An array that is already sorted would generate the best case for bubble sort. For example, [1, 2, 3, 4, 5].

~Selection Sort: An array that is already sorted would generate the best case for selection sort. For example, [1, 2, 3, 4, 5].

~Insertion Sort: An array that is already sorted would generate the best case for insertion sort. For example, [1, 2, 3, 4, 5].

~Merge Sort: An array that is already sorted would generate the best case for merge sort. For example, [1, 2, 3, 4, 5].

~Quick Sort: An array that is already sorted would generate the best case for quick sort. For example, [1, 2, 3, 4, 5].

#### 3.4 Memory Considerations
Order the various sorts based on which take up the most memory when sorting to the least memory. You may have to research this, and include the mathematical notation. 

~Merge Sort: Requires additional memory proportional to input size, usually O(n) or O(log n).

~Quick Sort: Uses a stack to keep track of recursive calls, typically O(log n) in average case, up to O(n) in worst case.

~Insertion Sort: Sorts elements in place, requires only a small amount of additional memory, O(1) space complexity.

~Selection Sort: Also operates in place, requires a small amount of additional memory, O(1) space complexity.

~Bubble Sort: In-place sorting algorithm, requires minimal additional memory, O(1) space complexity.

### 4. Growth of Functions
Give the following values, place them correctly into *six* categories. Use the bullets, and feel free to cut and paste the full LatexMath we used to generate them.  

$n^2$  
$n!$  
$n\log_2n$  
$5n^2+5n$  
$10000$  
$3n$    
$100$  
$2^n$  
$100n$  
$2^{(n-1)}$
#### Categories
* factorial and exponential growth
        $n!$  -
        $2^n$
* exponential growth
        $2^{n-1}$

* quadratic growth
        $5n^2+5n$  -
        $n^2$

* logarithmic growth
        $n\log_2n$

* linear growth
        $3n$  -
        $100n$

* constant growth
        $100$ -
        $10000$


### 5. Growth of Function Language

Pair the following terms with the correct function in the table. 
* Constant, Logarithmic, Linear, Quadratic, Cubic, Exponential, Factorial

| Big $O$     |  Name  |
| ------      | ------ |
| $O(n^3)$    |  Cubic |
| $O(1)$      |  Constant |
| $O(n)$      |  Linear |
| $O(\log_2n)$ |  Logarithmic |
| $O(n^2)$    |  Quadratic |
| $O(n!)$     |  Factorial |
| $O(2^n)$    |  Exponential |



### 6. Stable vs Unstable
Look up stability as it refers to sorting. In your own words, describe one sort that is stable and one sort that isn't stable  

A stable sorting algorithm preserves the relative order of equal elements in the input array, while an unstable sorting algorithm does not. Insertion Sort is an example of a stable algorithm, while Quick Sort is an example of an unstable algorithm.

### 6.2 When stability is needed?
Explain in your own words a case in which you will want a stable algorithm over an unstable. Include an example. 

There are many cases in which stability is important. One common example is when sorting a dataset by multiple criteria. For instance, if you have a list of people that you want to sort first by last name, and then by first name, you want to make sure that people with the same last name are sorted in the correct order based on their first name. If an unstable sorting algorithm were used, the order of people with the same last name could be changed during the sorting process, resulting in an incorrect final order. In contrast, using a stable sorting algorithm ensures that the order of people with the same last name is preserved while sorting by the secondary criterion.

### 7. Gold Thief

You are planning a heist to steal a rare coin that weighs 1.0001 ounces. The problem is that the rare coin was mixed with a bunch of counter fit coins. You know the counter fit coins only weight 1.0000 ounce each. There are in total 250 coins.  You have a simple balance scale where the coins can be weighed against each other. Hint: don't think about all the coins at once, but how you can break it up into even(ish) piles. 

To find the rare coin, one algorithm that can be used is the binary search algorithm. This involves dividing the coins into two equal parts and weighing them on the balance scale. If the two parts weigh the same, then the rare coin is in one of the unweighed coins. If they don't weigh the same, then the rare coin must be in the part that weighs more. The process is then repeated on that part until the rare coin is found.

#### 7.1 Algorithm
Describe an algorithm that will help you find the coin. We encourage you to use pseudo-code, but not required.

1. Divide the 250 coins into two groups, each containing 125 coins.
2. Weigh the first group of 125 coins against the second group of 125 coins.
3. If the scales are balanced, the rare coin is in one of the remaining 125 coins. Repeat step 1 with one group of 125 coins and the remaining coins.
4. If the scales are not balanced, the rare coin is in the lighter group of coins. Repeat step 1 with the lighter group of coins and the remaining coins.


#### 7.2 Time Complexity
What is the average time complexity of your algorithm? 

The average time complexity of this algorithm is O(log₂(250)) or approximately 8 comparisons. This is because we are dividing the coins into two equal groups at each step, and the number of coins is reduced by half after each weighing. Therefore, we need at most 8 weighings to find the rare coin.


<!-- links moved to bottom for easier reading in plain text (btw, this a comment that doesn't show in the webpage generated-->
[image markdown]: https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#images