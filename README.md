# SOC-26-project-31-24B0326
# MIDTERM PROJECT REPORT -(Project id-31)
Data Structures and Algorithms Learning Report (First Six Weeks)    
Name: Anshika(24b0326)       
Project Title: Data Structures and Algorithms Learning Journey      
Duration: First Six Weeks        
# Table of Contents    
1.Introduction    
2.Project Objectives    
3.Learning Methodology    
4.Topics Covered    
5.Arrays    
6.Prefix Sum    
7.Sliding Window    
8.Two Pointers    
9.Binary Search    
10.Matrix    
11.Stack    
12.Queue    
13.Recursion    
14.Backtracking      
15.One-Dimensional Dynamic Programming    
16.Binary Trees    
17.Heaps    
18.Overall Learnings      
19.Future Work    
20.Conclusion    
# 1. Introduction    
The objective of this project was to develop a strong foundation in Data Structures and Algorithms (DSA), which are fundamental to software engineering, competitive programming, and technical interviews. During the first six weeks, I focused on learning the core concepts, understanding the mathematical intuition behind algorithms, and solving problems using optimized approaches.    
Instead of memorizing solutions, I concentrated on understanding patterns that appear repeatedly across different problems. Every topic was studied theoretically before implementation, followed by solving problems of increasing difficulty.    
The project emphasized algorithm analysis, optimization techniques, and selecting the appropriate data structure based on problem constraints.

# 2. Project Objectives    
The major objectives of this project were:    
*Develop analytical thinking.    
*Learn commonly used data structures.    
*Understand algorithm design techniques.    
*Improve problem-solving efficiency.    
*Analyze time and space complexity.    
*Learn optimization strategies.      
*Build a strong base for advanced DSA topics.    

# 3. Learning Methodology
For every topic, I followed a structured learning process:    
*Study the theory.    
*Understand the brute-force solution.    
*Identify its limitations.    
*Derive an optimized approach.    
*Analyze complexity.    
*Implement the algorithm in C++.    
*Solve multiple practice problems.    
*Review mistakes and optimize further.      
This approach helped me understand not only how an algorithm works but also why it is efficient.    

# 4. Topics Covered
During the first six weeks, I studied:    
*Arrays    
*Prefix Sum      
*Sliding Window    
*Two Pointers    
*Binary Search    
*Matrix    
*Stack    
*Queue    
*Recursion    
*Backtracking      
*One-Dimensional Dynamic Programming    
*Binary Trees    
*Heaps    
Each topic introduced a new problem-solving paradigm and contributed to building a systematic approach toward solving algorithmic problems. 

# 5. Arrays
Theory    
An array is a linear data structure where elements are stored in contiguous memory locations. It provides constant-time random access and serves as the foundation for many advanced algorithms.    
Applications    
*Searching    
*Sorting    
*Prefix Sum    
*Sliding Window    
*Frequency Counting    
Complexity    
Operation          Complexity    
Access              O(1)      
Search              O(n)      
Insert/Delete       O(n)   

Generic Template
for(int i=0;i<n;i++){
    // process array[i]
}

Key Learnings
Always look for patterns instead of nested loops.
Many array problems can be optimized using hashing or prefix sums.
Constraints often determine whether an O(n²) solution is acceptable.

# 6. Prefix Sum
Theory
Prefix Sum stores cumulative sums so that range queries can be answered in constant time.
Instead of computing the sum repeatedly,
RangeSum(L,R)=Prefix[R]-Prefix[L-1]
Why it Works
The prefix array stores the total sum up to every position. Subtracting two prefix values removes the unwanted portion, leaving only the required range.
Complexity
Construction : O(n)
Query : O(1)
Template
prefix[0]=arr[0];
for(int i=1;i<n;i++)
    prefix[i]=prefix[i-1]+arr[i];

Applications
Range Sum Queries
Difference Arrays
Balanced Subarrays
Learnings
I learned that preprocessing is often worthwhile when multiple queries need to be answered efficiently.

# 7. Sliding Window
Theory
Sliding Window optimizes problems involving contiguous subarrays by maintaining a moving window instead of recomputing values.
Types
Fixed Size Window
Variable Size Window
Generic Template
int l=0;

for(int r=0;r<n;r++){

    // Add arr[r]

    while(condition){

        // Remove arr[l]

        l++;
    }
}

Complexity
O(n)
Each element enters and leaves the window at most once.
Applications
Longest Substring
Maximum Sum Subarray
Minimum Window Problems
Learnings
The biggest lesson was identifying whether a problem satisfies the properties required for a sliding window approach.
8. Two Pointers
Theory
Two Pointers process elements from two positions simultaneously to reduce unnecessary computations.
Applications
Pair Sum
Removing Duplicates
Merging Arrays
Container Problems
Template
int l=0,r=n-1;

while(l<r){

    if(condition)
        l++;
    else
        r--;
}

Complexity
O(n)
Learnings
This technique works best on sorted arrays or when the movement of pointers is monotonic.

# 9. Binary Search
Theory
Binary Search repeatedly divides the search space into two halves.
Proof of Complexity
After one iteration,
Size = n/2
After two iterations,
Size = n/4
After k iterations,
n/(2^k)=1
Therefore,
k=log₂(n)
Hence,
Time Complexity = O(log n)
Generic Template
while(low<=high){

    int mid=low+(high-low)/2;

    if(arr[mid]==target)
        return mid;

    else if(arr[mid]<target)
        low=mid+1;

    else
        high=mid-1;
}

Important Insight
Binary Search is applicable whenever the answer space is monotonic, not only on sorted arrays.
# 10. Matrix
Theory
A matrix extends arrays into two dimensions and is widely used in grid-based problems.
Topics Learned
Traversal
Spiral Order
Rotation
Diagonal Traversal
Template
for(int i=0;i<n;i++)
    for(int j=0;j<m;j++)
        process(matrix[i][j]);

Learnings
Most matrix problems become easier by visualizing movement directions and boundary conditions.

# 11. Stack
Theory
A Stack follows the Last-In-First-Out (LIFO) principle.
Applications
Parentheses Matching
Next Greater Element
Expression Evaluation
Monotonic Stack
Template
stack<int> st;

st.push(x);

st.pop();

st.top();

Learnings
Stacks simplify problems where recently processed elements need to be accessed repeatedly.

# 12. Queue
Theory
A Queue follows the First-In-First-Out (FIFO) principle.
Applications
BFS
Scheduling
Simulation
Level Order Traversal
Template
queue<int> q;

q.push(x);

q.pop();

q.front();

Learnings
Queues are essential whenever elements must be processed in the order they arrive.

# 13. Recursion
Theory
Recursion solves problems by calling the same function on smaller subproblems.
Essential Components
Base Case
Recursive Call
Return Statement
Generic Template
void solve(){

    if(base_case)
        return;

    solve(smaller_problem);
}

Learnings
Initially, recursion was challenging because of the call stack. Drawing recursion trees significantly improved my understanding.

# 14. Backtracking
Theory
Backtracking systematically explores all possibilities while undoing previous choices when necessary.
Generic Template
void solve(){

    if(answer_found)
        return;

    for(each choice){

        choose();

        solve();

        undo();
    }
}

Applications
N Queens
Sudoku
Permutations
Subsets
Learnings
The key idea is to restore the previous state before exploring another possibility.

# 15. One-Dimensional Dynamic Programming
Theory
Dynamic Programming stores solutions to previously solved subproblems, avoiding repeated computations.
Process
Recursion
↓
Memoization
↓
Tabulation
↓
Space Optimization
Generic Memoization
int solve(int n){

    if(base)
        return value;

    if(dp[n]!=-1)
        return dp[n];

    return dp[n]=...
}

Learnings
I learned to identify overlapping subproblems and define states clearly before writing transitions.

# 16. Binary Trees
Theory
Binary Trees organize data hierarchically and are naturally solved using recursion.
Topics Covered
Traversals
Height
Diameter
Balanced Trees
Lowest Common Ancestor
DFS Template
void dfs(Node* root){

    if(root==NULL)
        return;

    dfs(root->left);

    dfs(root->right);
}

Learnings
Every subtree can be treated as an independent problem, making recursive solutions intuitive.

# 17. Heaps
Theory
A Heap is a complete binary tree that efficiently supports retrieving the minimum or maximum element.
Applications
Priority Queue
Top K Elements
Merge K Lists
Template
priority_queue<int> pq;

pq.push(x);

pq.pop();

pq.top();

Complexity
Insertion : O(log n)
Deletion : O(log n)
Top : O(1)
Learnings
Heaps are highly effective when repeatedly accessing the smallest or largest element without fully sorting the data.

# 18. Overall Learnings
Throughout the six-week project, I observed several important principles:
Start with a simple brute-force solution before optimizing.
Always analyze constraints before selecting an algorithm.
Recognize recurring patterns rather than memorizing solutions.
Carefully evaluate time and space complexity.
Handle edge cases early in the implementation process.
Debug systematically using small test cases.
Consistent practice improves pattern recognition and coding speed.
These practices significantly improved my confidence in solving algorithmic problems.

# 19. Future Work
In the next phase of the project, I plan to study:
Graph Algorithms
Advanced Dynamic Programming
Disjoint Set Union
String Algorithms
Advanced Greedy Techniques
The objective is to strengthen my understanding of advanced algorithmic concepts and improve my performance in coding interviews and competitive programming.

# 20. Conclusion
The first six weeks of this project have established a strong foundation in Data Structures and Algorithms. By studying fundamental topics, implementing standard templates, analyzing algorithmic complexity, and solving diverse problems, I developed a structured and analytical approach to problem solving.
Rather than focusing solely on obtaining correct answers, I learned the importance of understanding the reasoning behind each algorithm, recognizing reusable patterns, and selecting the most efficient approach based on problem constraints. These learnings provide a solid base for the advanced topics that will be explored in the remaining phase of the project.





