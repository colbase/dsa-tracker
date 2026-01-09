# 🚀 DSA Mastery Guide: Complete Learning Roadmap

> **Your comprehensive guide to mastering Data Structures and Algorithms from zero to hero**

---

## 📋 Table of Contents

1. [Phase 1: Foundation & Basics](#phase-1-foundation--basics)
2. [Phase 2: Core Data Structures](#phase-2-core-data-structures)
3. [Phase 3: Algorithm Paradigms](#phase-3-algorithm-paradigms)
4. [Phase 4: Advanced Topics](#phase-4-advanced-topics)
5. [Phase 5: Practice Strategy & Problem Lists](#phase-5-practice-strategy--problem-lists)

---

# Phase 1: Foundation & Basics

> **Duration:** 2-3 weeks | **Goal:** Build a solid programming and mathematical foundation

---

## 1.1 Programming Language Proficiency

### Choose Your Language
Pick **ONE** language and master it completely. Recommended options:

| Language | Pros | Best For |
|----------|------|----------|
| **Python** | Easy syntax, great for interviews | Beginners, quick prototyping |
| **C++** | STL library, fastest execution | Competitive programming |
| **Java** | Strong OOP, widely used | Enterprise interviews |
| **JavaScript** | Great for web devs | Frontend/Full-stack roles |

### Core Language Concepts to Master

#### 1. Basic Syntax & Control Flow
- [ ] Variables and data types (int, float, string, boolean)
- [ ] Operators (arithmetic, logical, bitwise, comparison)
- [ ] Conditional statements (if, else, else if, switch)
- [ ] Loops (for, while, do-while, foreach)
- [ ] Break, continue, and nested loops

#### 2. Functions & Methods
- [ ] Function declaration and definition
- [ ] Parameters and arguments (by value vs by reference)
- [ ] Return types and multiple returns
- [ ] Recursion basics
- [ ] Lambda functions / Anonymous functions

#### 3. Built-in Data Structures
- [ ] Arrays (static vs dynamic)
- [ ] Strings and string manipulation
- [ ] Lists / ArrayLists / Vectors
- [ ] Dictionaries / HashMaps / Objects
- [ ] Sets and their operations

#### 4. Object-Oriented Programming (OOP)
- [ ] Classes and objects
- [ ] Constructors and destructors
- [ ] Encapsulation (public, private, protected)
- [ ] Inheritance and polymorphism
- [ ] Abstraction and interfaces

---

## 1.2 Mathematics for DSA

### 1.2.1 Number Theory

#### Prime Numbers
```
Definition: A number > 1 that has no positive divisors other than 1 and itself

Key Concepts:
- Prime checking: O(√n) complexity
- Sieve of Eratosthenes: Find all primes up to n in O(n log log n)
- Prime factorization
```

**Essential Problems:**
1. Check if a number is prime
2. Find all primes up to N (Sieve of Eratosthenes)
3. Count prime factors of a number
4. Find GCD and LCM of two numbers

#### GCD and LCM
```
GCD (Greatest Common Divisor): Largest number that divides both a and b
- Euclidean Algorithm: GCD(a, b) = GCD(b, a % b), base case: GCD(a, 0) = a

LCM (Least Common Multiple): Smallest number divisible by both a and b
- LCM(a, b) = (a × b) / GCD(a, b)
```

#### Modular Arithmetic
```
Key Properties:
- (a + b) % m = ((a % m) + (b % m)) % m
- (a - b) % m = ((a % m) - (b % m) + m) % m
- (a × b) % m = ((a % m) × (b % m)) % m
- (a / b) % m = (a × b^(-1)) % m (requires modular inverse)

Modular Exponentiation: Calculate a^b % m efficiently in O(log b)
```

### 1.2.2 Combinatorics

#### Permutations and Combinations
```
Permutation (order matters): P(n, r) = n! / (n-r)!
Combination (order doesn't matter): C(n, r) = n! / (r! × (n-r)!)

Pascal's Triangle Property:
C(n, r) = C(n-1, r-1) + C(n-1, r)
```

#### Important Formulas
| Concept | Formula | Use Case |
|---------|---------|----------|
| Factorial | n! = n × (n-1)! | Counting arrangements |
| Catalan Numbers | C_n = C(2n, n) / (n+1) | Binary trees, parentheses |
| Fibonacci | F(n) = F(n-1) + F(n-2) | Counting paths, DP |
| Stars and Bars | C(n+r-1, r-1) | Distributing items |

### 1.2.3 Logarithms & Powers

```
Essential Properties:
- log_b(xy) = log_b(x) + log_b(y)
- log_b(x/y) = log_b(x) - log_b(y)
- log_b(x^n) = n × log_b(x)
- log_b(x) = log_a(x) / log_a(b)  (Change of base)

Powers of 2 (memorize these!):
2^0 = 1, 2^1 = 2, 2^2 = 4, 2^3 = 8, 2^4 = 16
2^5 = 32, 2^6 = 64, 2^7 = 128, 2^8 = 256
2^10 = 1024 ≈ 10^3, 2^20 ≈ 10^6, 2^30 ≈ 10^9
```

### 1.2.4 Probability Basics

```
Fundamental Concepts:
- Probability = Favorable outcomes / Total outcomes
- P(A or B) = P(A) + P(B) - P(A and B)
- P(A and B) = P(A) × P(B) if independent
- Expected Value = Σ (value × probability)
```

---

## 1.3 Complexity Analysis (Big O Notation)

### Understanding Time Complexity

#### What is Big O?
Big O notation describes the **upper bound** of an algorithm's growth rate. It tells us how the runtime/space grows as input size increases.

#### Common Time Complexities (Fastest to Slowest)

| Notation | Name | Example | n=100 ops |
|----------|------|---------|-----------|
| O(1) | Constant | Array access | 1 |
| O(log n) | Logarithmic | Binary search | 7 |
| O(n) | Linear | Array traversal | 100 |
| O(n log n) | Linearithmic | Merge sort | 664 |
| O(n²) | Quadratic | Bubble sort | 10,000 |
| O(n³) | Cubic | 3 nested loops | 1,000,000 |
| O(2^n) | Exponential | Subsets generation | 10^30 |
| O(n!) | Factorial | Permutations | 10^157 |

#### Complexity Analysis Rules

```
1. DROP CONSTANTS:
   O(2n) → O(n)
   O(100n + 50) → O(n)

2. DROP LOWER ORDER TERMS:
   O(n² + n) → O(n²)
   O(n³ + n²+ n) → O(n³)

3. MULTIPLICATION FOR NESTED OPERATIONS:
   for i in range(n):        # O(n)
       for j in range(m):    # O(m)
           print(i, j)       # × O(1)
   # Total: O(n × m)

4. ADDITION FOR SEQUENTIAL OPERATIONS:
   for i in range(n): pass   # O(n)
   for j in range(m): pass   # O(m)
   # Total: O(n + m)
```

### Space Complexity

```
Measures additional memory used by the algorithm

Examples:
- Variables: O(1)
- Array of size n: O(n)
- 2D array n×m: O(n×m)
- Recursion depth d: O(d) for call stack
- HashMap with n keys: O(n)
```

### Constraint Analysis (Crucial for Interviews!)

```
Use constraints to determine acceptable complexity:

n ≤ 10        → O(n!), O(2^n) acceptable
n ≤ 20        → O(2^n), O(n! × log n) possible
n ≤ 100       → O(n³) acceptable
n ≤ 1,000     → O(n²) acceptable
n ≤ 10,000    → O(n²) borderline, prefer O(n log n)
n ≤ 100,000   → O(n log n) or O(n) needed
n ≤ 1,000,000 → O(n) or O(n log n) required
n ≤ 10^8      → O(n) maximum, prefer O(log n) or O(1)
```

---

## 1.4 Recursion Fundamentals

### What is Recursion?

A function that calls itself to solve smaller instances of the same problem.

```
Two Essential Parts:
1. BASE CASE: Condition to stop recursion (prevents infinite loop)
2. RECURSIVE CASE: Break problem into smaller subproblems
```

### Anatomy of a Recursive Function

```python
def recursive_function(input):
    # BASE CASE - when to stop
    if base_condition:
        return base_value
    
    # RECURSIVE CASE - make progress toward base case
    result = recursive_function(smaller_input)
    
    # COMBINE - use result to build answer
    return combined_result
```

### Classic Recursion Problems (Must Master)

#### 1. Factorial
```python
def factorial(n):
    if n <= 1:           # Base case
        return 1
    return n * factorial(n - 1)  # Recursive case

# factorial(5) = 5 × 4 × 3 × 2 × 1 = 120
# Call stack: factorial(5) → factorial(4) → factorial(3) → factorial(2) → factorial(1)
```

#### 2. Fibonacci
```python
def fibonacci(n):
    if n <= 1:           # Base case
        return n
    return fibonacci(n-1) + fibonacci(n-2)  # Recursive case

# Time: O(2^n) - Exponential! (can be optimized with memoization)
```

#### 3. Sum of Array
```python
def array_sum(arr, n):
    if n == 0:           # Base case
        return 0
    return arr[n-1] + array_sum(arr, n-1)
```

#### 4. Power Function
```python
def power(x, n):
    if n == 0:           # Base case
        return 1
    if n % 2 == 0:       # Even exponent
        half = power(x, n // 2)
        return half * half
    else:                # Odd exponent
        return x * power(x, n - 1)

# Time: O(log n) - Much better than O(n)!
```

### Recursion Patterns

#### Pattern 1: Decrease and Conquer
```
Reduce problem size by constant factor each step
Examples: Factorial, Linear search, Array sum
```

#### Pattern 2: Divide and Conquer
```
Split problem into multiple subproblems, solve each, combine results
Examples: Merge sort, Quick sort, Binary search
```

#### Pattern 3: Multiple Recursion
```
Make multiple recursive calls at each step
Examples: Fibonacci, Tree traversals, Combinations
```

### Recursion vs Iteration Trade-offs

| Aspect | Recursion | Iteration |
|--------|-----------|-----------|
| Code readability | Often cleaner | Can be verbose |
| Space | O(depth) stack | Usually O(1) |
| Performance | Overhead from calls | Generally faster |
| Use when | Problem is naturally recursive | Performance critical |

### Tail Recursion Optimization

```python
# NOT tail recursive (computation after recursive call)
def factorial(n):
    if n <= 1: return 1
    return n * factorial(n - 1)  # Multiplication happens after call

# TAIL RECURSIVE (recursive call is last operation)
def factorial_tail(n, accumulator=1):
    if n <= 1: return accumulator
    return factorial_tail(n - 1, n * accumulator)  # Nothing after call
```

---

## 1.5 Practice Problems for Phase 1

### Beginner Level (Complete All)

| # | Problem | Concept | Platform |
|---|---------|---------|----------|
| 1 | Two Sum | Arrays, HashMap basics | LeetCode #1 |
| 2 | Palindrome Number | Math, string manipulation | LeetCode #9 |
| 3 | Roman to Integer | String parsing | LeetCode #13 |
| 4 | Valid Parentheses | Stack basics | LeetCode #20 |
| 5 | Merge Two Sorted Lists | Linked list basics | LeetCode #21 |
| 6 | Remove Duplicates from Sorted Array | Two pointers | LeetCode #26 |
| 7 | Search Insert Position | Binary search basics | LeetCode #35 |
| 8 | Maximum Subarray | Kadane's algorithm intro | LeetCode #53 |
| 9 | Climbing Stairs | Basic recursion/DP | LeetCode #70 |
| 10 | Sqrt(x) | Binary search application | LeetCode #69 |

### Recursion Practice

| # | Problem | Concept |
|---|---------|---------|
| 1 | Reverse a string using recursion | Basic recursion |
| 2 | Check if array is sorted | Decrease and conquer |
| 3 | Print 1 to N without loop | Head recursion |
| 4 | Print N to 1 without loop | Tail recursion |
| 5 | Sum of digits | Number manipulation |
| 6 | Power of three/four | Multiple bases |
| 7 | Fibonacci with memoization | Intro to DP |
| 8 | Count ways to reach nth stair | Counting problems |

### Math Practice

| # | Problem | Platform |
|---|---------|----------|
| 1 | Count Primes | LeetCode #204 |
| 2 | Power of Two | LeetCode #231 |
| 3 | Ugly Number | LeetCode #263 |
| 4 | Happy Number | LeetCode #202 |
| 5 | Excel Sheet Column Number | LeetCode #171 |
| 6 | Factorial Trailing Zeroes | LeetCode #172 |

---

## Phase 1 Checklist

- [ ] Chose programming language and practiced syntax
- [ ] Comfortable with loops, conditions, functions
- [ ] Understand OOP basics (classes, inheritance)
- [ ] Know prime checking and Sieve algorithm
- [ ] Can calculate GCD/LCM efficiently
- [ ] Understand modular arithmetic
- [ ] Know permutation and combination formulas
- [ ] Can analyze time complexity of code
- [ ] Can analyze space complexity of code
- [ ] Can estimate required complexity from constraints
- [ ] Understand recursion base and recursive cases
- [ ] Solved at least 10 easy recursion problems
- [ ] Completed all 10 beginner level problems
- [ ] Can trace through recursive calls mentally

---

**Estimated Time:** 2-3 weeks with 2-3 hours daily practice

**Next:** [Phase 2: Core Data Structures →](#phase-2-core-data-structures)
# Phase 2: Core Data Structures

> **Duration:** 4-6 weeks | **Goal:** Master every fundamental data structure

---

## 2.1 Arrays

### What is an Array?
A contiguous block of memory storing elements of the same type, accessed by index.

### Array Operations & Complexities

| Operation | Time Complexity | Notes |
|-----------|-----------------|-------|
| Access by index | O(1) | Direct memory access |
| Search (unsorted) | O(n) | Linear scan required |
| Search (sorted) | O(log n) | Binary search |
| Insert at end | O(1) amortized | May need resize |
| Insert at index | O(n) | Shift elements right |
| Delete at end | O(1) | Simple removal |
| Delete at index | O(n) | Shift elements left |

### Key Array Patterns

#### Pattern 1: Two Pointers
```
Use two pointers moving towards each other or in same direction

Applications:
- Pair sum problems
- Reversing arrays
- Removing duplicates
- Merging sorted arrays
- Partitioning (Dutch National Flag)

Example: Two Sum (Sorted Array)
left = 0, right = n-1
while left < right:
    sum = arr[left] + arr[right]
    if sum == target: return [left, right]
    elif sum < target: left++
    else: right--
```

#### Pattern 2: Sliding Window
```
Maintain a window that slides over the array

Types:
1. Fixed size window (easy)
2. Variable size window (medium-hard)

Template (Variable Window):
left = 0
for right in range(n):
    # Add arr[right] to window
    while window_condition_invalid():
        # Remove arr[left] from window
        left++
    # Update answer
```

#### Pattern 3: Prefix Sum
```
Precompute cumulative sums for O(1) range queries

prefix[i] = sum of arr[0...i-1]
sum(i, j) = prefix[j+1] - prefix[i]

2D Prefix Sum:
prefix[i][j] = sum of submatrix from (0,0) to (i-1,j-1)
```

#### Pattern 4: Kadane's Algorithm
```
Find maximum subarray sum in O(n)

max_ending_here = max_so_far = arr[0]
for i in range(1, n):
    max_ending_here = max(arr[i], max_ending_here + arr[i])
    max_so_far = max(max_so_far, max_ending_here)
```

### Must-Solve Array Problems

| # | Problem | Pattern | Difficulty |
|---|---------|---------|------------|
| 1 | Two Sum | HashMap | Easy |
| 2 | Best Time to Buy/Sell Stock | Single pass | Easy |
| 3 | Contains Duplicate | HashSet | Easy |
| 4 | Product of Array Except Self | Prefix/Suffix | Medium |
| 5 | Maximum Subarray | Kadane's | Medium |
| 6 | Maximum Product Subarray | DP variant | Medium |
| 7 | 3Sum | Two pointers | Medium |
| 8 | Container With Most Water | Two pointers | Medium |
| 9 | Merge Intervals | Sorting | Medium |
| 10 | Subarray Sum Equals K | Prefix sum + HashMap | Medium |
| 11 | Rotate Array | Reversal | Medium |
| 12 | First Missing Positive | Cyclic sort | Hard |
| 13 | Trapping Rain Water | Two pointers/Stack | Hard |
| 14 | Median of Two Sorted Arrays | Binary search | Hard |

---

## 2.2 Strings

### String Fundamentals

```
Strings = Arrays of characters with special operations

Key Properties:
- Immutable in most languages (Java, Python)
- Comparison is O(min(len(s1), len(s2)))
- Concatenation: O(n) for immutable strings

String Builder Usage:
When doing many concatenations, use StringBuilder (Java) 
or list join (Python) for O(n) instead of O(n²)
```

### String Patterns

#### Pattern 1: Character Frequency Map
```python
from collections import Counter
freq = Counter(s)  # O(n) to build, O(1) to query

# Check anagram
def is_anagram(s1, s2):
    return Counter(s1) == Counter(s2)
```

#### Pattern 2: Two Pointers (for palindromes)
```python
def is_palindrome(s):
    left, right = 0, len(s) - 1
    while left < right:
        if s[left] != s[right]:
            return False
        left += 1
        right -= 1
    return True
```

#### Pattern 3: Sliding Window
```
Find substrings with specific properties
- Longest substring without repeating chars
- Minimum window substring
- Anagram substrings
```

#### Pattern 4: String Matching
```
KMP Algorithm: O(n + m) pattern matching
Rabin-Karp: O(n + m) average with rolling hash
Z-Algorithm: O(n + m) pattern matching
```

### Must-Solve String Problems

| # | Problem | Pattern | Difficulty |
|---|---------|---------|------------|
| 1 | Valid Anagram | Frequency count | Easy |
| 2 | Valid Palindrome | Two pointers | Easy |
| 3 | Longest Common Prefix | Vertical/Horizontal | Easy |
| 4 | Longest Substring Without Repeating | Sliding window | Medium |
| 5 | Longest Palindromic Substring | Expand from center/DP | Medium |
| 6 | Group Anagrams | Hash sorting | Medium |
| 7 | Minimum Window Substring | Sliding window | Hard |
| 8 | Palindromic Substrings | DP/Expand | Medium |
| 9 | Encode and Decode Strings | Design | Medium |
| 10 | Edit Distance | DP | Medium |

---

## 2.3 Linked Lists

### What is a Linked List?
Sequential collection where each element (node) contains data and reference to next node.

### Types of Linked Lists

```
1. SINGLY LINKED LIST
   [data|next] → [data|next] → [data|null]
   - Each node points to next
   - Traverse forward only

2. DOUBLY LINKED LIST
   null ← [prev|data|next] ⟷ [prev|data|next] → null
   - Each node points to prev and next
   - Traverse both directions

3. CIRCULAR LINKED LIST
   [data|next] → [data|next] → [data|next] ⟲
   - Last node points to first
   - No null terminator
```

### Linked List Operations

| Operation | Singly LL | Doubly LL |
|-----------|-----------|-----------|
| Access by index | O(n) | O(n) |
| Insert at head | O(1) | O(1) |
| Insert at tail | O(n) or O(1)* | O(1) |
| Insert at middle | O(n) | O(n) |
| Delete at head | O(1) | O(1) |
| Delete at tail | O(n) | O(1) |
| Delete at middle | O(n) | O(n) |
| Search | O(n) | O(n) |

*O(1) if tail pointer maintained

### Key Linked List Patterns

#### Pattern 1: Two Pointers (Fast & Slow)
```python
# Detect cycle
def has_cycle(head):
    slow = fast = head
    while fast and fast.next:
        slow = slow.next
        fast = fast.next.next
        if slow == fast:
            return True
    return False

# Find middle
def find_middle(head):
    slow = fast = head
    while fast and fast.next:
        slow = slow.next
        fast = fast.next.next
    return slow
```

#### Pattern 2: Reversal
```python
def reverse_list(head):
    prev = None
    curr = head
    while curr:
        next_temp = curr.next
        curr.next = prev
        prev = curr
        curr = next_temp
    return prev
```

#### Pattern 3: Dummy Node
```python
# Use dummy when head might change
def remove_elements(head, val):
    dummy = ListNode(0)
    dummy.next = head
    curr = dummy
    while curr.next:
        if curr.next.val == val:
            curr.next = curr.next.next
        else:
            curr = curr.next
    return dummy.next
```

### Must-Solve Linked List Problems

| # | Problem | Pattern | Difficulty |
|---|---------|---------|------------|
| 1 | Reverse Linked List | Reversal | Easy |
| 2 | Merge Two Sorted Lists | Merge | Easy |
| 3 | Linked List Cycle | Fast/Slow | Easy |
| 4 | Middle of Linked List | Fast/Slow | Easy |
| 5 | Remove Nth Node From End | Two pointers | Medium |
| 6 | Add Two Numbers | Math | Medium |
| 7 | Reorder List | Find mid + Reverse + Merge | Medium |
| 8 | Linked List Cycle II | Floyd's | Medium |
| 9 | LRU Cache | HashMap + DLL | Medium |
| 10 | Merge k Sorted Lists | Heap/Divide-conquer | Hard |
| 11 | Reverse Nodes in k-Group | Reversal | Hard |

---

## 2.4 Stacks

### What is a Stack?
LIFO (Last In, First Out) data structure.

```
Operations:
- push(x): Add to top - O(1)
- pop(): Remove from top - O(1)
- peek/top(): View top - O(1)
- isEmpty(): Check empty - O(1)

Visualization:
    |  3  | ← top
    |  2  |
    |  1  |
    -------
```

### Stack Patterns

#### Pattern 1: Matching Parentheses
```python
def is_valid(s):
    stack = []
    mapping = {')': '(', '}': '{', ']': '['}
    for char in s:
        if char in mapping:
            if not stack or stack.pop() != mapping[char]:
                return False
        else:
            stack.append(char)
    return len(stack) == 0
```

#### Pattern 2: Monotonic Stack
```python
# Next Greater Element
def next_greater(arr):
    result = [-1] * len(arr)
    stack = []  # stores indices
    for i in range(len(arr)):
        while stack and arr[i] > arr[stack[-1]]:
            result[stack.pop()] = arr[i]
        stack.append(i)
    return result
```

#### Pattern 3: Expression Evaluation
```
Infix to Postfix conversion
Postfix evaluation
Calculator problems
```

### Must-Solve Stack Problems

| # | Problem | Pattern | Difficulty |
|---|---------|---------|------------|
| 1 | Valid Parentheses | Matching | Easy |
| 2 | Min Stack | Design | Medium |
| 3 | Daily Temperatures | Monotonic stack | Medium |
| 4 | Evaluate Reverse Polish Notation | Evaluation | Medium |
| 5 | Basic Calculator | Expression | Hard |
| 6 | Largest Rectangle in Histogram | Monotonic stack | Hard |
| 7 | Decode String | Nested structure | Medium |
| 8 | Asteroid Collision | Simulation | Medium |

---

## 2.5 Queues

### What is a Queue?
FIFO (First In, First Out) data structure.

```
Operations:
- enqueue(x): Add to rear - O(1)
- dequeue(): Remove from front - O(1)
- front(): View front - O(1)
- isEmpty(): Check empty - O(1)

Visualization:
front → [ 1 | 2 | 3 | 4 ] ← rear
```

### Queue Variants

#### Circular Queue
```
- Fixed size array with wrap-around
- front and rear pointers
- rear = (rear + 1) % capacity
- front = (front + 1) % capacity
```

#### Deque (Double-Ended Queue)
```
- Insert/delete at both ends
- Supports both stack and queue operations
- Used for sliding window problems
```

#### Priority Queue (Heap-based)
```
- Elements dequeued by priority, not insertion order
- See Heaps section for details
```

### Queue Patterns

#### Pattern 1: BFS (Breadth-First Search)
```python
from collections import deque

def bfs(start):
    queue = deque([start])
    visited = {start}
    while queue:
        node = queue.popleft()
        for neighbor in get_neighbors(node):
            if neighbor not in visited:
                visited.add(neighbor)
                queue.append(neighbor)
```

#### Pattern 2: Sliding Window Maximum (Monotonic Deque)
```python
from collections import deque

def max_sliding_window(nums, k):
    result = []
    dq = deque()  # stores indices
    for i, num in enumerate(nums):
        # Remove indices outside window
        while dq and dq[0] < i - k + 1:
            dq.popleft()
        # Remove smaller elements
        while dq and nums[dq[-1]] < num:
            dq.pop()
        dq.append(i)
        if i >= k - 1:
            result.append(nums[dq[0]])
    return result
```

### Must-Solve Queue Problems

| # | Problem | Pattern | Difficulty |
|---|---------|---------|------------|
| 1 | Implement Queue using Stacks | Design | Easy |
| 2 | Number of Islands | BFS | Medium |
| 3 | Rotting Oranges | Multi-source BFS | Medium |
| 4 | Walls and Gates | BFS | Medium |
| 5 | Sliding Window Maximum | Monotonic deque | Hard |
| 6 | Design Circular Queue | Design | Medium |

---

## 2.6 Hash Tables (HashMap/Dictionary)

### What is a Hash Table?
Data structure that maps keys to values using a hash function.

```
Key Concepts:
- Hash Function: Converts key to index
- Collision Resolution: Handle same index for different keys
  - Chaining: Linked list at each bucket
  - Open Addressing: Probe for next empty slot
- Load Factor: n/capacity, typically resize at 0.75
```

### Hash Table Operations

| Operation | Average | Worst |
|-----------|---------|-------|
| Insert | O(1) | O(n) |
| Delete | O(1) | O(n) |
| Search | O(1) | O(n) |

### Hash Table Patterns

#### Pattern 1: Frequency Counter
```python
def top_k_frequent(nums, k):
    count = Counter(nums)
    return [x for x, _ in count.most_common(k)]
```

#### Pattern 2: Two Sum Pattern
```python
def two_sum(nums, target):
    seen = {}
    for i, num in enumerate(nums):
        complement = target - num
        if complement in seen:
            return [seen[complement], i]
        seen[num] = i
```

#### Pattern 3: Grouping
```python
def group_anagrams(strs):
    groups = defaultdict(list)
    for s in strs:
        key = tuple(sorted(s))
        groups[key].append(s)
    return list(groups.values())
```

### HashSet vs HashMap

| Feature | HashSet | HashMap |
|---------|---------|---------|
| Stores | Keys only | Key-value pairs |
| Use case | Uniqueness, membership | Associations, counting |
| Example | Contains duplicate | Two sum |

### Must-Solve Hash Table Problems

| # | Problem | Pattern | Difficulty |
|---|---------|---------|------------|
| 1 | Two Sum | Complement lookup | Easy |
| 2 | Contains Duplicate | Set membership | Easy |
| 3 | Valid Anagram | Frequency count | Easy |
| 4 | Group Anagrams | Grouping | Medium |
| 5 | Top K Frequent Elements | Counting | Medium |
| 6 | Longest Consecutive Sequence | Set operations | Medium |
| 7 | Subarray Sum Equals K | Prefix sum + map | Medium |
| 8 | LRU Cache | OrderedDict/DLL | Medium |

---

## 2.7 Trees

### Tree Terminology

```
        1       ← Root
       / \
      2   3     ← Internal nodes
     / \   \
    4   5   6   ← Leaf nodes

- Root: Top node with no parent
- Parent: Node with children
- Child: Node with parent
- Leaf: Node with no children
- Height: Longest path from root to leaf
- Depth: Distance from root to node
- Subtree: Tree formed by node and descendants
```

### Binary Tree

```
Each node has at most 2 children (left and right)

Types:
1. Full Binary Tree: Every node has 0 or 2 children
2. Complete Binary Tree: All levels filled except last, filled left to right
3. Perfect Binary Tree: All internal nodes have 2 children, all leaves same level
4. Balanced Binary Tree: Height difference of subtrees ≤ 1
```

### Tree Traversals

```python
# Pre-order (Root-Left-Right): Used for copying tree
def preorder(root):
    if not root: return
    print(root.val)
    preorder(root.left)
    preorder(root.right)

# In-order (Left-Root-Right): BST gives sorted order
def inorder(root):
    if not root: return
    inorder(root.left)
    print(root.val)
    inorder(root.right)

# Post-order (Left-Right-Root): Used for deleting tree
def postorder(root):
    if not root: return
    postorder(root.left)
    postorder(root.right)
    print(root.val)

# Level-order (BFS)
from collections import deque
def levelorder(root):
    if not root: return
    queue = deque([root])
    while queue:
        node = queue.popleft()
        print(node.val)
        if node.left: queue.append(node.left)
        if node.right: queue.append(node.right)
```

### Binary Search Tree (BST)

```
Properties:
- Left subtree contains only nodes < root
- Right subtree contains only nodes > root
- Both subtrees are also BSTs

Operations:
| Operation | Average | Worst (unbalanced) |
|-----------|---------|-------------------|
| Search | O(log n) | O(n) |
| Insert | O(log n) | O(n) |
| Delete | O(log n) | O(n) |
```

### Self-Balancing Trees (Know concepts)

```
AVL Tree:
- Height difference of subtrees ≤ 1
- Rotations to maintain balance

Red-Black Tree:
- Every node is red or black
- Root is black
- Red nodes can't have red children
- Same black nodes on all paths
```

### Must-Solve Tree Problems

| # | Problem | Pattern | Difficulty |
|---|---------|---------|------------|
| 1 | Maximum Depth of Binary Tree | DFS | Easy |
| 2 | Invert Binary Tree | DFS | Easy |
| 3 | Same Tree | DFS | Easy |
| 4 | Symmetric Tree | DFS | Easy |
| 5 | Binary Tree Level Order | BFS | Medium |
| 6 | Validate BST | Inorder/Bounds | Medium |
| 7 | Lowest Common Ancestor (BST) | BST property | Medium |
| 8 | Binary Tree Right Side View | BFS | Medium |
| 9 | Construct Binary Tree from Preorder/Inorder | Divide & Conquer | Medium |
| 10 | Kth Smallest Element in BST | Inorder | Medium |
| 11 | Serialize and Deserialize Binary Tree | BFS/DFS | Hard |
| 12 | Binary Tree Maximum Path Sum | DFS | Hard |

---

## 2.8 Heaps (Priority Queues)

### What is a Heap?
Complete binary tree satisfying heap property.

```
Max Heap: Parent ≥ Children
Min Heap: Parent ≤ Children

Array Representation (0-indexed):
- Parent of i: (i-1) // 2
- Left child of i: 2*i + 1
- Right child of i: 2*i + 2

Example Min Heap:
        1
       / \
      3   2
     / \
    5   4
Array: [1, 3, 2, 5, 4]
```

### Heap Operations

| Operation | Time Complexity |
|-----------|-----------------|
| Insert (heappush) | O(log n) |
| Remove min/max (heappop) | O(log n) |
| Get min/max (peek) | O(1) |
| Heapify array | O(n) |
| Build heap | O(n) |

### Heap Implementation

```python
import heapq

# Min heap (default in Python)
heap = []
heapq.heappush(heap, 5)
heapq.heappush(heap, 3)
heapq.heappush(heap, 8)
smallest = heapq.heappop(heap)  # Returns 3

# Max heap (negate values)
max_heap = []
heapq.heappush(max_heap, -5)
heapq.heappush(max_heap, -3)
largest = -heapq.heappop(max_heap)  # Returns 5

# Heapify existing list
arr = [5, 3, 8, 1, 2]
heapq.heapify(arr)  # O(n)
```

### Heap Patterns

#### Pattern 1: Top K Elements
```python
def find_k_largest(nums, k):
    return heapq.nlargest(k, nums)

# Or with min heap of size k:
def find_k_largest_v2(nums, k):
    heap = nums[:k]
    heapq.heapify(heap)
    for num in nums[k:]:
        if num > heap[0]:
            heapq.heapreplace(heap, num)
    return heap
```

#### Pattern 2: Merge K Sorted Lists
```python
def merge_k_lists(lists):
    heap = []
    for i, lst in enumerate(lists):
        if lst:
            heapq.heappush(heap, (lst[0], i, 0))
    
    result = []
    while heap:
        val, list_idx, elem_idx = heapq.heappop(heap)
        result.append(val)
        if elem_idx + 1 < len(lists[list_idx]):
            next_val = lists[list_idx][elem_idx + 1]
            heapq.heappush(heap, (next_val, list_idx, elem_idx + 1))
    return result
```

### Must-Solve Heap Problems

| # | Problem | Pattern | Difficulty |
|---|---------|---------|------------|
| 1 | Kth Largest Element | Min heap of size k | Medium |
| 2 | Top K Frequent Elements | Heap + HashMap | Medium |
| 3 | Find Median from Data Stream | Two heaps | Hard |
| 4 | Merge k Sorted Lists | Min heap | Hard |
| 5 | Task Scheduler | Max heap + Greedy | Medium |
| 6 | K Closest Points to Origin | Max heap of size k | Medium |

---

## 2.9 Graphs

### Graph Terminology

```
- Vertex (Node): Point in graph
- Edge: Connection between vertices
- Directed: Edges have direction (A → B)
- Undirected: Edges are bidirectional (A — B)
- Weighted: Edges have values
- Cycle: Path that starts and ends at same vertex
- Connected: Path exists between all vertex pairs
- DAG: Directed Acyclic Graph
```

### Graph Representations

#### Adjacency Matrix
```
Space: O(V²)
Edge lookup: O(1)
Iterate neighbors: O(V)

    0 1 2 3
0 [ 0 1 0 1 ]
1 [ 1 0 1 0 ]
2 [ 0 1 0 1 ]
3 [ 1 0 1 0 ]
```

#### Adjacency List
```python
# Space: O(V + E)
# Edge lookup: O(degree)
# Iterate neighbors: O(degree)

graph = {
    0: [1, 3],
    1: [0, 2],
    2: [1, 3],
    3: [0, 2]
}
```

### Graph Traversals

#### DFS (Depth-First Search)
```python
def dfs(graph, start, visited=None):
    if visited is None:
        visited = set()
    visited.add(start)
    for neighbor in graph[start]:
        if neighbor not in visited:
            dfs(graph, neighbor, visited)
    return visited

# Iterative DFS
def dfs_iterative(graph, start):
    visited = set()
    stack = [start]
    while stack:
        node = stack.pop()
        if node not in visited:
            visited.add(node)
            stack.extend(graph[node])
```

#### BFS (Breadth-First Search)
```python
from collections import deque

def bfs(graph, start):
    visited = {start}
    queue = deque([start])
    while queue:
        node = queue.popleft()
        for neighbor in graph[node]:
            if neighbor not in visited:
                visited.add(neighbor)
                queue.append(neighbor)
    return visited
```

### Key Graph Algorithms

| Algorithm | Use Case | Time |
|-----------|----------|------|
| DFS | Cycle detection, topological sort, connected components | O(V+E) |
| BFS | Shortest path (unweighted), level order | O(V+E) |
| Dijkstra | Shortest path (weighted, non-negative) | O((V+E)logV) |
| Bellman-Ford | Shortest path (with negative weights) | O(VE) |
| Floyd-Warshall | All pairs shortest path | O(V³) |
| Topological Sort | Task scheduling (DAG) | O(V+E) |
| Union-Find | Cycle detection, connected components | O(α(n)) |
| Kruskal/Prim | Minimum Spanning Tree | O(E log V) |

### Must-Solve Graph Problems

| # | Problem | Algorithm | Difficulty |
|---|---------|-----------|------------|
| 1 | Number of Islands | DFS/BFS | Medium |
| 2 | Clone Graph | DFS/BFS | Medium |
| 3 | Pacific Atlantic Water Flow | DFS/BFS | Medium |
| 4 | Course Schedule | Topological Sort | Medium |
| 5 | Course Schedule II | Topological Sort | Medium |
| 6 | Number of Connected Components | Union-Find/DFS | Medium |
| 7 | Graph Valid Tree | Union-Find | Medium |
| 8 | Word Ladder | BFS | Hard |
| 9 | Alien Dictionary | Topological Sort | Hard |
| 10 | Network Delay Time | Dijkstra | Medium |

---

## 2.10 Tries (Prefix Trees)

### What is a Trie?
Tree-like data structure for efficient string storage and retrieval.

```
Storing: ["app", "apple", "application", "apt"]

        root
         |
         a
         |
         p
        / \
       p   t (apt)
       |
       l (app)
       |
       e (apple)
       |
       ...
```

### Trie Implementation
```python
class TrieNode:
    def __init__(self):
        self.children = {}
        self.is_end = False

class Trie:
    def __init__(self):
        self.root = TrieNode()
    
    def insert(self, word):  # O(m)
        node = self.root
        for char in word:
            if char not in node.children:
                node.children[char] = TrieNode()
            node = node.children[char]
        node.is_end = True
    
    def search(self, word):  # O(m)
        node = self.root
        for char in word:
            if char not in node.children:
                return False
            node = node.children[char]
        return node.is_end
    
    def starts_with(self, prefix):  # O(m)
        node = self.root
        for char in prefix:
            if char not in node.children:
                return False
            node = node.children[char]
        return True
```

### Must-Solve Trie Problems

| # | Problem | Difficulty |
|---|---------|------------|
| 1 | Implement Trie | Medium |
| 2 | Design Add and Search Words | Medium |
| 3 | Word Search II | Hard |

---

## Phase 2 Checklist

- [ ] Arrays: Two pointers, sliding window, prefix sum
- [ ] Strings: Anagrams, palindromes, pattern matching
- [ ] Linked Lists: Reversal, cycle detection, merge
- [ ] Stacks: Matching, monotonic stack, expression evaluation
- [ ] Queues: BFS, sliding window maximum
- [ ] Hash Tables: Frequency counting, grouping
- [ ] Trees: Traversals, BST operations, LCA
- [ ] Heaps: Top K, merge K lists, streaming median
- [ ] Graphs: DFS, BFS, topological sort, shortest path
- [ ] Tries: Basic operations, prefix matching

**Estimated Time:** 4-6 weeks with 3-4 hours daily practice

---

**Next:** [Phase 3: Algorithm Paradigms →](#phase-3-algorithm-paradigms)
# Phase 3: Algorithm Paradigms

> **Duration:** 6-8 weeks | **Goal:** Master all major algorithmic techniques

---

## 3.1 Binary Search

### The Core Idea
Eliminate half the search space each iteration. **Requires sorted or monotonic property.**

### Binary Search Templates

#### Template 1: Standard (Find exact match)
```python
def binary_search(arr, target):
    left, right = 0, len(arr) - 1
    while left <= right:
        mid = left + (right - left) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1  # Not found
```

#### Template 2: Lower Bound (First >= target)
```python
def lower_bound(arr, target):
    left, right = 0, len(arr)
    while left < right:
        mid = left + (right - left) // 2
        if arr[mid] < target:
            left = mid + 1
        else:
            right = mid
    return left  # First position >= target
```

#### Template 3: Upper Bound (First > target)
```python
def upper_bound(arr, target):
    left, right = 0, len(arr)
    while left < right:
        mid = left + (right - left) // 2
        if arr[mid] <= target:
            left = mid + 1
        else:
            right = mid
    return left  # First position > target
```

#### Template 4: Binary Search on Answer
```python
def binary_search_answer(lo, hi, is_valid):
    """Find minimum valid answer"""
    while lo < hi:
        mid = lo + (hi - lo) // 2
        if is_valid(mid):
            hi = mid  # Try smaller
        else:
            lo = mid + 1  # Need larger
    return lo
```

### Binary Search Patterns

| Pattern | Description | Example |
|---------|-------------|---------|
| Find element | Standard binary search | Search in sorted array |
| Find boundary | First/last occurrence | Find first bad version |
| Search answer | Binary search on answer space | Koko eating bananas |
| Rotated array | Modified with rotation | Search in rotated array |
| 2D matrix | Treat as 1D or two searches | Search in 2D matrix |

### When to Use Binary Search
1. Array is sorted or has monotonic property
2. Answer has a range and you can verify validity
3. "Minimum that satisfies..." or "Maximum that satisfies..."
4. Problem can be transformed to yes/no question

### Must-Solve Binary Search Problems

| # | Problem | Pattern | Difficulty |
|---|---------|---------|------------|
| 1 | Binary Search | Standard | Easy |
| 2 | First Bad Version | Lower bound | Easy |
| 3 | Search Insert Position | Lower bound | Easy |
| 4 | Search in Rotated Sorted Array | Modified | Medium |
| 5 | Find Minimum in Rotated Sorted Array | Boundary | Medium |
| 6 | Find Peak Element | Boundary | Medium |
| 7 | Search a 2D Matrix | 2D to 1D | Medium |
| 8 | Koko Eating Bananas | Answer search | Medium |
| 9 | Capacity To Ship Packages | Answer search | Medium |
| 10 | Median of Two Sorted Arrays | Partition | Hard |

---

## 3.2 Two Pointers

### Types of Two Pointer Techniques

#### Type 1: Opposite Direction (Converging)
```python
def two_sum_sorted(arr, target):
    left, right = 0, len(arr) - 1
    while left < right:
        curr_sum = arr[left] + arr[right]
        if curr_sum == target:
            return [left, right]
        elif curr_sum < target:
            left += 1
        else:
            right -= 1
    return []
```

#### Type 2: Same Direction (Fast & Slow)
```python
def remove_duplicates(arr):
    if not arr:
        return 0
    slow = 0
    for fast in range(1, len(arr)):
        if arr[fast] != arr[slow]:
            slow += 1
            arr[slow] = arr[fast]
    return slow + 1
```

#### Type 3: Fast & Slow (Cycle Detection)
```python
def has_cycle(head):
    slow = fast = head
    while fast and fast.next:
        slow = slow.next
        fast = fast.next.next
        if slow == fast:
            return True
    return False
```

### Two Pointers Patterns

| Pattern | Use case | Examples |
|---------|----------|----------|
| Opposite ends | Sorted pairs | Two sum, 3Sum |
| Slow & fast | In-place modification | Remove duplicates |
| Cycle detection | Linked list cycles | Floyd's algorithm |
| Partition | Arrange elements | Dutch flag, Quick select |

### Must-Solve Two Pointer Problems

| # | Problem | Pattern | Difficulty |
|---|---------|---------|------------|
| 1 | Two Sum II | Converging | Medium |
| 2 | 3Sum | Sort + converging | Medium |
| 3 | Container With Most Water | Converging | Medium |
| 4 | Remove Duplicates | Fast/Slow | Easy |
| 5 | Move Zeroes | Fast/Slow | Easy |
| 6 | Linked List Cycle II | Floyd's | Medium |
| 7 | Trapping Rain Water | Converging | Hard |
| 8 | Sort Colors | Dutch flag | Medium |
| 9 | 4Sum | Nested converging | Medium |

---

## 3.3 Sliding Window

### Fixed Size Window
```python
def max_sum_k(arr, k):
    """Maximum sum of subarray of size k"""
    window_sum = sum(arr[:k])
    max_sum = window_sum
    
    for i in range(k, len(arr)):
        window_sum += arr[i] - arr[i - k]  # Slide window
        max_sum = max(max_sum, window_sum)
    
    return max_sum
```

### Variable Size Window Template
```python
def sliding_window_variable(arr, condition):
    """Find min/max window satisfying condition"""
    left = 0
    result = 0  # or float('inf') for minimum
    # window_state = ...  # Track window state
    
    for right in range(len(arr)):
        # 1. ADD element at right to window
        # window_state.add(arr[right])
        
        # 2. SHRINK window while invalid
        while not is_valid(window_state):
            # Remove element at left
            # window_state.remove(arr[left])
            left += 1
        
        # 3. UPDATE result
        result = max(result, right - left + 1)
    
    return result
```

### Example: Longest Substring Without Repeating Characters
```python
def length_of_longest_substring(s):
    seen = {}
    left = 0
    max_length = 0
    
    for right, char in enumerate(s):
        if char in seen and seen[char] >= left:
            left = seen[char] + 1
        seen[char] = right
        max_length = max(max_length, right - left + 1)
    
    return max_length
```

### Sliding Window Patterns

| Pattern | Description | Example |
|---------|-------------|---------|
| Fixed size | Window size constant | Max sum of k elements |
| Dynamic size | Find min/max window | Longest substring |
| Counter-based | Track frequencies | Minimum window substring |
| At most K | Constraint on window | Subarrays with K distinct |

### Must-Solve Sliding Window Problems

| # | Problem | Type | Difficulty |
|---|---------|------|------------|
| 1 | Maximum Average Subarray I | Fixed | Easy |
| 2 | Longest Substring Without Repeating | Variable | Medium |
| 3 | Minimum Window Substring | Variable + Counter | Hard |
| 4 | Permutation in String | Fixed + Counter | Medium |
| 5 | Find All Anagrams | Fixed + Counter | Medium |
| 6 | Longest Repeating Character Replacement | Variable | Medium |
| 7 | Subarrays with K Different Integers | At most K | Hard |
| 8 | Max Consecutive Ones III | Variable | Medium |

---

## 3.4 Backtracking

### The Core Idea
Build solution incrementally, abandoning paths that can't lead to valid solutions.

### Backtracking Template
```python
def backtrack(state, choices):
    # Base case: found a valid solution
    if is_solution(state):
        result.append(state.copy())
        return
    
    for choice in choices:
        # Pruning: skip invalid choices early
        if not is_valid(choice, state):
            continue
        
        # Make choice
        state.append(choice)
        
        # Explore further
        backtrack(state, get_next_choices(choice))
        
        # Undo choice (backtrack)
        state.pop()
```

### Classic Backtracking Problems

#### Subsets (All combinations)
```python
def subsets(nums):
    result = []
    
    def backtrack(start, path):
        result.append(path[:])  # Add current subset
        for i in range(start, len(nums)):
            path.append(nums[i])
            backtrack(i + 1, path)
            path.pop()
    
    backtrack(0, [])
    return result
```

#### Permutations (All arrangements)
```python
def permutations(nums):
    result = []
    
    def backtrack(path, used):
        if len(path) == len(nums):
            result.append(path[:])
            return
        
        for i in range(len(nums)):
            if used[i]:
                continue
            used[i] = True
            path.append(nums[i])
            backtrack(path, used)
            path.pop()
            used[i] = False
    
    backtrack([], [False] * len(nums))
    return result
```

#### Combinations (K elements from N)
```python
def combinations(n, k):
    result = []
    
    def backtrack(start, path):
        if len(path) == k:
            result.append(path[:])
            return
        
        # Pruning: need k-len(path) more elements
        for i in range(start, n - (k - len(path)) + 2):
            path.append(i)
            backtrack(i + 1, path)
            path.pop()
    
    backtrack(1, [])
    return result
```

### Backtracking Patterns

| Pattern | Description | Example |
|---------|-------------|---------|
| Generate all | List all possible solutions | Subsets, Permutations |
| Find one | Stop at first solution | Sudoku, N-Queens |
| Count | Count valid solutions | N-Queens II |
| Constraint satisfaction | Meet all constraints | Sudoku |

### Must-Solve Backtracking Problems

| # | Problem | Pattern | Difficulty |
|---|---------|---------|------------|
| 1 | Subsets | Generate all | Medium |
| 2 | Subsets II (with duplicates) | Generate + Skip dups | Medium |
| 3 | Permutations | Generate all | Medium |
| 4 | Permutations II (with duplicates) | Generate + Skip dups | Medium |
| 5 | Combinations | Generate all | Medium |
| 6 | Combination Sum | Unlimited choices | Medium |
| 7 | Combination Sum II | Limited choices | Medium |
| 8 | Letter Combinations of Phone | Generate all | Medium |
| 9 | Palindrome Partitioning | String partition | Medium |
| 10 | N-Queens | Constraint satisfaction | Hard |
| 11 | Sudoku Solver | Constraint satisfaction | Hard |
| 12 | Word Search | Grid path | Medium |

---

## 3.5 Dynamic Programming (DP)

### The Core Idea
Solve complex problems by breaking into overlapping subproblems, storing results to avoid recomputation.

### When to Use DP
1. Optimal substructure: Optimal solution contains optimal solutions to subproblems
2. Overlapping subproblems: Same subproblems solved multiple times
3. Key phrases: "minimum/maximum", "count ways", "is it possible"

### DP Approaches

#### Top-Down (Memoization)
```python
def fib_memo(n, memo={}):
    if n in memo:
        return memo[n]
    if n <= 1:
        return n
    memo[n] = fib_memo(n-1, memo) + fib_memo(n-2, memo)
    return memo[n]
```

#### Bottom-Up (Tabulation)
```python
def fib_tab(n):
    if n <= 1:
        return n
    dp = [0] * (n + 1)
    dp[1] = 1
    for i in range(2, n + 1):
        dp[i] = dp[i-1] + dp[i-2]
    return dp[n]
```

#### Space Optimized
```python
def fib_optimized(n):
    if n <= 1:
        return n
    prev2, prev1 = 0, 1
    for _ in range(2, n + 1):
        curr = prev1 + prev2
        prev2, prev1 = prev1, curr
    return prev1
```

### DP Patterns

#### Pattern 1: 1D DP (Linear Sequence)
```
State: dp[i] = answer for subproblem ending at/considering index i
Transition: dp[i] = f(dp[i-1], dp[i-2], ...)

Examples: Climbing Stairs, House Robber, Longest Increasing Subsequence
```

**Template: House Robber**
```python
def rob(nums):
    if len(nums) <= 2:
        return max(nums) if nums else 0
    
    dp = [0] * len(nums)
    dp[0] = nums[0]
    dp[1] = max(nums[0], nums[1])
    
    for i in range(2, len(nums)):
        dp[i] = max(dp[i-1], dp[i-2] + nums[i])
    
    return dp[-1]
```

#### Pattern 2: 2D DP (Two Sequences / Grid)
```
State: dp[i][j] = answer considering s1[0:i] and s2[0:j] OR grid position (i,j)
Transition: dp[i][j] = f(dp[i-1][j], dp[i][j-1], dp[i-1][j-1])

Examples: Edit Distance, Longest Common Subsequence, Unique Paths
```

**Template: Longest Common Subsequence**
```python
def longestCommonSubsequence(text1, text2):
    m, n = len(text1), len(text2)
    dp = [[0] * (n + 1) for _ in range(m + 1)]
    
    for i in range(1, m + 1):
        for j in range(1, n + 1):
            if text1[i-1] == text2[j-1]:
                dp[i][j] = dp[i-1][j-1] + 1
            else:
                dp[i][j] = max(dp[i-1][j], dp[i][j-1])
    
    return dp[m][n]
```

#### Pattern 3: 0/1 Knapsack
```
Given items with weight and value, maximize value within capacity

State: dp[i][w] = max value using items[0:i] with capacity w
Transition: 
- Skip item: dp[i][w] = dp[i-1][w]
- Take item: dp[i][w] = dp[i-1][w-weight[i]] + value[i]
- dp[i][w] = max(skip, take)
```

**Template: 0/1 Knapsack**
```python
def knapsack(weights, values, capacity):
    n = len(weights)
    dp = [[0] * (capacity + 1) for _ in range(n + 1)]
    
    for i in range(1, n + 1):
        for w in range(capacity + 1):
            dp[i][w] = dp[i-1][w]  # Don't take
            if weights[i-1] <= w:
                dp[i][w] = max(dp[i][w], 
                              dp[i-1][w-weights[i-1]] + values[i-1])
    
    return dp[n][capacity]
```

#### Pattern 4: Unbounded Knapsack
```
Items can be used unlimited times

Transition: dp[w] = max(dp[w], dp[w-weight[i]] + value[i])
Examples: Coin Change, Rod Cutting, Complete Knapsack
```

**Template: Coin Change**
```python
def coinChange(coins, amount):
    dp = [float('inf')] * (amount + 1)
    dp[0] = 0
    
    for coin in coins:
        for x in range(coin, amount + 1):
            dp[x] = min(dp[x], dp[x - coin] + 1)
    
    return dp[amount] if dp[amount] != float('inf') else -1
```

#### Pattern 5: String DP
```
State: dp[i][j] = property of substring s[i:j]
Transition: Depends on problem

Examples: Palindrome Partitioning, Longest Palindromic Substring
```

#### Pattern 6: Interval DP
```
State: dp[i][j] = optimal answer for range [i, j]
Transition: Try all split points k in [i, j]

Examples: Matrix Chain Multiplication, Burst Balloons
```

### DP Problem-Solving Framework

```
1. IDENTIFY: Is this a DP problem? (Optimization/Counting with subproblems)

2. DEFINE STATE: What does dp[i] or dp[i][j] represent?
   - What information uniquely identifies a subproblem?
   - What parameters change as we solve?

3. RECURRENCE: How to compute dp[i] from smaller subproblems?
   - What are the choices at each step?
   - How do subproblems combine?

4. BASE CASE: What are the trivial cases?
   - dp[0] = ?, dp[1] = ?

5. ORDER: In what order to fill the table?
   - Must solve subproblems before main problem

6. ANSWER: Where is the final answer?
   - dp[n]? dp[n][m]? max(dp[i])?
```

### Must-Solve DP Problems

#### 1D DP (Start here)
| # | Problem | Pattern | Difficulty |
|---|---------|---------|------------|
| 1 | Climbing Stairs | Fibonacci-like | Easy |
| 2 | House Robber | Linear decision | Medium |
| 3 | House Robber II | Circular array | Medium |
| 4 | Decode Ways | Counting | Medium |
| 5 | Longest Increasing Subsequence | LIS | Medium |
| 6 | Maximum Product Subarray | Kadane variant | Medium |
| 7 | Word Break | String DP | Medium |

#### 2D DP
| # | Problem | Pattern | Difficulty |
|---|---------|---------|------------|
| 8 | Unique Paths | Grid | Medium |
| 9 | Unique Paths II | Grid with obstacles | Medium |
| 10 | Minimum Path Sum | Grid | Medium |
| 11 | Longest Common Subsequence | Two strings | Medium |
| 12 | Edit Distance | Two strings | Medium |
| 13 | Target Sum | 0/1 Knapsack | Medium |

#### Knapsack Variants
| # | Problem | Pattern | Difficulty |
|---|---------|---------|------------|
| 14 | Coin Change | Unbounded | Medium |
| 15 | Coin Change 2 | Counting | Medium |
| 16 | Partition Equal Subset Sum | 0/1 Knapsack | Medium |
| 17 | Perfect Squares | Unbounded | Medium |

#### Advanced
| # | Problem | Pattern | Difficulty |
|---|---------|---------|------------|
| 18 | Longest Palindromic Subsequence | Interval | Medium |
| 19 | Interleaving String | Two strings | Medium |
| 20 | Regular Expression Matching | Two strings | Hard |
| 21 | Burst Balloons | Interval | Hard |

---

## 3.6 Greedy Algorithms

### The Core Idea
Make locally optimal choice at each step, hoping for global optimum.

### When Greedy Works
- Optimal substructure
- Greedy choice property (local optimum leads to global optimum)
- Can prove correctness (exchange argument, induction)

### Greedy Patterns

#### Pattern 1: Activity Selection / Interval Scheduling
```python
def max_meetings(intervals):
    """Maximum non-overlapping intervals"""
    intervals.sort(key=lambda x: x[1])  # Sort by end time
    count = 0
    end = float('-inf')
    
    for start, finish in intervals:
        if start >= end:
            count += 1
            end = finish
    
    return count
```

#### Pattern 2: Huffman-Style (Merge smallest)
```python
import heapq

def min_cost_connect_ropes(ropes):
    heapq.heapify(ropes)
    total_cost = 0
    
    while len(ropes) > 1:
        first = heapq.heappop(ropes)
        second = heapq.heappop(ropes)
        cost = first + second
        total_cost += cost
        heapq.heappush(ropes, cost)
    
    return total_cost
```

#### Pattern 3: Jump Game Style
```python
def can_jump(nums):
    max_reach = 0
    for i, jump in enumerate(nums):
        if i > max_reach:
            return False
        max_reach = max(max_reach, i + jump)
    return True
```

### Must-Solve Greedy Problems

| # | Problem | Pattern | Difficulty |
|---|---------|---------|------------|
| 1 | Jump Game | Farthest reach | Medium |
| 2 | Jump Game II | Min jumps | Medium |
| 3 | Non-overlapping Intervals | Interval scheduling | Medium |
| 4 | Merge Intervals | Interval merging | Medium |
| 5 | Meeting Rooms II | Min resources | Medium |
| 6 | Task Scheduler | Greedy + Heap | Medium |
| 7 | Gas Station | Circular greedy | Medium |
| 8 | Candy | Two-pass greedy | Hard |
| 9 | Best Time to Buy and Sell Stock II | Local maxima | Medium |

---

## 3.7 Divide and Conquer

### The Core Idea
1. **Divide**: Break problem into smaller subproblems
2. **Conquer**: Solve subproblems recursively
3. **Combine**: Merge solutions to get final answer

### Classic Divide and Conquer Algorithms

#### Merge Sort
```python
def merge_sort(arr):
    if len(arr) <= 1:
        return arr
    
    mid = len(arr) // 2
    left = merge_sort(arr[:mid])
    right = merge_sort(arr[mid:])
    
    return merge(left, right)

def merge(left, right):
    result = []
    i = j = 0
    while i < len(left) and j < len(right):
        if left[i] <= right[j]:
            result.append(left[i])
            i += 1
        else:
            result.append(right[j])
            j += 1
    result.extend(left[i:])
    result.extend(right[j:])
    return result

# Time: O(n log n), Space: O(n)
```

#### Quick Sort
```python
def quick_sort(arr, low, high):
    if low < high:
        pivot_idx = partition(arr, low, high)
        quick_sort(arr, low, pivot_idx - 1)
        quick_sort(arr, pivot_idx + 1, high)

def partition(arr, low, high):
    pivot = arr[high]
    i = low - 1
    for j in range(low, high):
        if arr[j] < pivot:
            i += 1
            arr[i], arr[j] = arr[j], arr[i]
    arr[i + 1], arr[high] = arr[high], arr[i + 1]
    return i + 1

# Time: O(n log n) average, O(n²) worst
# Space: O(log n)
```

### Must-Solve Divide and Conquer Problems

| # | Problem | Pattern | Difficulty |
|---|---------|---------|------------|
| 1 | Merge Sort | Classic | Medium |
| 2 | Quick Sort | Classic | Medium |
| 3 | Maximum Subarray | D&C approach | Medium |
| 4 | Search in Rotated Array | Modified binary | Medium |
| 5 | Construct Binary Tree | From traversals | Medium |
| 6 | Count Inversions | Merge sort variant | Hard |

---

## Phase 3 Checklist

- [ ] Binary Search: All 4 templates, can identify when to use
- [ ] Two Pointers: Converging, fast/slow, partition
- [ ] Sliding Window: Fixed and variable size patterns
- [ ] Backtracking: Subsets, permutations, constraint satisfaction
- [ ] Dynamic Programming: 1D, 2D, knapsack patterns
- [ ] Greedy: Interval scheduling, activity selection
- [ ] Divide and Conquer: Merge sort, quick sort

**Estimated Time:** 6-8 weeks with 4 hours daily practice

---

**Next:** [Phase 4: Advanced Topics →](#phase-4-advanced-topics)
# Phase 4: Advanced Topics

> **Duration:** 4-6 weeks | **Goal:** Master advanced patterns for competitive programming and hard interviews

---

## 4.1 Union-Find (Disjoint Set Union)

### What is Union-Find?
Data structure to track elements partitioned into disjoint sets, supporting:
- **Find**: Which set contains element X?
- **Union**: Merge two sets

### Implementation with Optimizations

```python
class UnionFind:
    def __init__(self, n):
        self.parent = list(range(n))
        self.rank = [0] * n
        self.count = n  # Number of components
    
    def find(self, x):
        """Path compression: Make all nodes point directly to root"""
        if self.parent[x] != x:
            self.parent[x] = self.find(self.parent[x])
        return self.parent[x]
    
    def union(self, x, y):
        """Union by rank: Attach smaller tree under larger tree"""
        root_x, root_y = self.find(x), self.find(y)
        if root_x == root_y:
            return False  # Already in same set
        
        if self.rank[root_x] < self.rank[root_y]:
            root_x, root_y = root_y, root_x
        self.parent[root_y] = root_x
        if self.rank[root_x] == self.rank[root_y]:
            self.rank[root_x] += 1
        
        self.count -= 1
        return True
    
    def connected(self, x, y):
        return self.find(x) == self.find(y)
```

### Time Complexity
With path compression + union by rank: **O(α(n))** per operation (nearly O(1))

### Applications
- Connected components in graph
- Cycle detection in undirected graph
- Kruskal's MST algorithm
- Dynamic connectivity
- Accounts merge

### Must-Solve Union-Find Problems

| # | Problem | Difficulty |
|---|---------|------------|
| 1 | Number of Connected Components | Medium |
| 2 | Graph Valid Tree | Medium |
| 3 | Redundant Connection | Medium |
| 4 | Accounts Merge | Medium |
| 5 | Longest Consecutive Sequence | Medium |
| 6 | Number of Islands II | Hard |
| 7 | Smallest String With Swaps | Medium |

---

## 4.2 Advanced Tree Structures

### Segment Tree

**Purpose**: Range queries (sum, min, max) and point/range updates in O(log n)

```python
class SegmentTree:
    def __init__(self, arr):
        self.n = len(arr)
        self.tree = [0] * (4 * self.n)
        self.build(arr, 0, 0, self.n - 1)
    
    def build(self, arr, node, start, end):
        if start == end:
            self.tree[node] = arr[start]
        else:
            mid = (start + end) // 2
            self.build(arr, 2*node+1, start, mid)
            self.build(arr, 2*node+2, mid+1, end)
            self.tree[node] = self.tree[2*node+1] + self.tree[2*node+2]
    
    def update(self, idx, val, node=0, start=0, end=None):
        if end is None: end = self.n - 1
        if start == end:
            self.tree[node] = val
        else:
            mid = (start + end) // 2
            if idx <= mid:
                self.update(idx, val, 2*node+1, start, mid)
            else:
                self.update(idx, val, 2*node+2, mid+1, end)
            self.tree[node] = self.tree[2*node+1] + self.tree[2*node+2]
    
    def query(self, l, r, node=0, start=0, end=None):
        if end is None: end = self.n - 1
        if r < start or l > end:
            return 0
        if l <= start and end <= r:
            return self.tree[node]
        mid = (start + end) // 2
        return (self.query(l, r, 2*node+1, start, mid) + 
                self.query(l, r, 2*node+2, mid+1, end))
```

### Binary Indexed Tree (Fenwick Tree)

**Purpose**: Prefix sums with updates in O(log n), simpler than segment tree

```python
class FenwickTree:
    def __init__(self, n):
        self.n = n
        self.tree = [0] * (n + 1)
    
    def update(self, i, delta):
        """Add delta to index i"""
        i += 1  # 1-indexed
        while i <= self.n:
            self.tree[i] += delta
            i += i & (-i)  # Add lowest set bit
    
    def prefix_sum(self, i):
        """Sum of elements [0, i]"""
        i += 1  # 1-indexed
        total = 0
        while i > 0:
            total += self.tree[i]
            i -= i & (-i)  # Remove lowest set bit
        return total
    
    def range_sum(self, l, r):
        """Sum of elements [l, r]"""
        return self.prefix_sum(r) - (self.prefix_sum(l-1) if l > 0 else 0)
```

---

## 4.3 Bit Manipulation

### Essential Bit Operations

```python
# Basics
x & y    # AND
x | y    # OR
x ^ y    # XOR
~x       # NOT
x << n   # Left shift (multiply by 2^n)
x >> n   # Right shift (divide by 2^n)

# Common Tricks
x & 1            # Check if odd
x & (x - 1)      # Remove lowest set bit
x & (-x)         # Isolate lowest set bit
x | (x + 1)      # Set lowest unset bit
x ^ (1 << i)     # Toggle bit i
x | (1 << i)     # Set bit i
x & ~(1 << i)    # Clear bit i
(x >> i) & 1     # Get bit i
```

### Important Bit Manipulation Patterns

#### Count Set Bits (Brian Kernighan)
```python
def count_bits(n):
    count = 0
    while n:
        n &= (n - 1)  # Remove lowest set bit
        count += 1
    return count
```

#### Power of Two
```python
def is_power_of_two(n):
    return n > 0 and (n & (n - 1)) == 0
```

#### Single Number (XOR)
```python
def single_number(nums):
    result = 0
    for num in nums:
        result ^= num
    return result
```

#### Subsets Using Bitmask
```python
def subsets_bitmask(nums):
    n = len(nums)
    result = []
    for mask in range(1 << n):
        subset = [nums[i] for i in range(n) if mask & (1 << i)]
        result.append(subset)
    return result
```

### Must-Solve Bit Manipulation Problems

| # | Problem | Difficulty |
|---|---------|------------|
| 1 | Single Number | Easy |
| 2 | Number of 1 Bits | Easy |
| 3 | Counting Bits | Easy |
| 4 | Reverse Bits | Easy |
| 5 | Missing Number | Easy |
| 6 | Sum of Two Integers | Medium |
| 7 | Single Number II | Medium |
| 8 | Single Number III | Medium |

---

## 4.4 Advanced Graph Algorithms

### Topological Sort (Kahn's Algorithm)
```python
from collections import deque, defaultdict

def topological_sort(num_nodes, edges):
    graph = defaultdict(list)
    in_degree = [0] * num_nodes
    
    for u, v in edges:
        graph[u].append(v)
        in_degree[v] += 1
    
    queue = deque([i for i in range(num_nodes) if in_degree[i] == 0])
    order = []
    
    while queue:
        node = queue.popleft()
        order.append(node)
        for neighbor in graph[node]:
            in_degree[neighbor] -= 1
            if in_degree[neighbor] == 0:
                queue.append(neighbor)
    
    return order if len(order) == num_nodes else []  # Empty if cycle exists
```

### Dijkstra's Algorithm
```python
import heapq
from collections import defaultdict

def dijkstra(graph, start):
    distances = {node: float('inf') for node in graph}
    distances[start] = 0
    pq = [(0, start)]
    
    while pq:
        curr_dist, node = heapq.heappop(pq)
        if curr_dist > distances[node]:
            continue
        
        for neighbor, weight in graph[node]:
            distance = curr_dist + weight
            if distance < distances[neighbor]:
                distances[neighbor] = distance
                heapq.heappush(pq, (distance, neighbor))
    
    return distances
```

### Bellman-Ford (Negative weights)
```python
def bellman_ford(n, edges, start):
    dist = [float('inf')] * n
    dist[start] = 0
    
    for _ in range(n - 1):
        for u, v, w in edges:
            if dist[u] != float('inf') and dist[u] + w < dist[v]:
                dist[v] = dist[u] + w
    
    # Check for negative cycle
    for u, v, w in edges:
        if dist[u] != float('inf') and dist[u] + w < dist[v]:
            return None  # Negative cycle exists
    
    return dist
```

### Floyd-Warshall (All pairs shortest path)
```python
def floyd_warshall(graph, n):
    dist = [[float('inf')] * n for _ in range(n)]
    
    for i in range(n):
        dist[i][i] = 0
    
    for u, v, w in graph:
        dist[u][v] = w
    
    for k in range(n):
        for i in range(n):
            for j in range(n):
                if dist[i][k] + dist[k][j] < dist[i][j]:
                    dist[i][j] = dist[i][k] + dist[k][j]
    
    return dist
```

### Minimum Spanning Tree (Kruskal's)
```python
def kruskal_mst(n, edges):
    edges.sort(key=lambda x: x[2])  # Sort by weight
    uf = UnionFind(n)
    mst = []
    
    for u, v, weight in edges:
        if uf.union(u, v):
            mst.append((u, v, weight))
            if len(mst) == n - 1:
                break
    
    return mst
```

### Must-Solve Advanced Graph Problems

| # | Problem | Algorithm | Difficulty |
|---|---------|-----------|------------|
| 1 | Course Schedule | Topological Sort | Medium |
| 2 | Course Schedule II | Topological Sort | Medium |
| 3 | Network Delay Time | Dijkstra | Medium |
| 4 | Cheapest Flights K Stops | Modified Dijkstra | Medium |
| 5 | Find the City | Floyd-Warshall | Medium |
| 6 | Min Cost to Connect All Points | Kruskal/Prim | Medium |
| 7 | Swim in Rising Water | Binary Search + BFS | Hard |
| 8 | Reconstruct Itinerary | Eulerian Path | Hard |

---

## 4.5 String Algorithms

### KMP (Knuth-Morris-Pratt) Pattern Matching
```python
def kmp_search(text, pattern):
    def build_lps(pattern):
        lps = [0] * len(pattern)
        length = 0
        i = 1
        while i < len(pattern):
            if pattern[i] == pattern[length]:
                length += 1
                lps[i] = length
                i += 1
            elif length:
                length = lps[length - 1]
            else:
                lps[i] = 0
                i += 1
        return lps
    
    lps = build_lps(pattern)
    i = j = 0
    matches = []
    
    while i < len(text):
        if text[i] == pattern[j]:
            i += 1
            j += 1
            if j == len(pattern):
                matches.append(i - j)
                j = lps[j - 1]
        elif j:
            j = lps[j - 1]
        else:
            i += 1
    
    return matches
```

### Rabin-Karp (Rolling Hash)
```python
def rabin_karp(text, pattern):
    d = 256  # Number of characters
    q = 101  # Prime number
    m, n = len(pattern), len(text)
    
    p_hash = t_hash = 0
    h = pow(d, m-1, q)
    
    # Calculate initial hashes
    for i in range(m):
        p_hash = (d * p_hash + ord(pattern[i])) % q
        t_hash = (d * t_hash + ord(text[i])) % q
    
    matches = []
    for i in range(n - m + 1):
        if p_hash == t_hash:
            if text[i:i+m] == pattern:
                matches.append(i)
        
        if i < n - m:
            t_hash = (d * (t_hash - ord(text[i]) * h) + ord(text[i+m])) % q
            if t_hash < 0:
                t_hash += q
    
    return matches
```

---

## Phase 4 Checklist

- [ ] Union-Find: Implementation with optimizations
- [ ] Segment Tree: Range queries and updates
- [ ] Fenwick Tree: Prefix sums
- [ ] Bit Manipulation: All common tricks
- [ ] Topological Sort: Both DFS and Kahn's
- [ ] Dijkstra: Shortest path in weighted graph
- [ ] MST: Kruskal's/Prim's algorithm
- [ ] KMP: Pattern matching

**Estimated Time:** 4-6 weeks with 4 hours daily practice

---

# Phase 5: Practice Strategy & Problem Lists

> **Goal:** Structured practice approach to solidify all concepts

---

## 5.1 Practice Philosophy

### The Golden Rules
1. **Understand before memorizing**: Know WHY patterns work
2. **Active recall > Passive reading**: Struggle before looking at solutions
3. **Spaced repetition**: Revisit problems after 1 day, 1 week, 1 month
4. **Quality > Quantity**: Deep understanding of 200 problems > surface level of 500
5. **Time yourself**: Practice under interview conditions

### Time Allocation Per Problem

| Difficulty | Time Limit | Review Solution |
|------------|------------|-----------------|
| Easy | 15-20 min | After 15 min stuck |
| Medium | 30-40 min | After 25 min stuck |
| Hard | 45-60 min | After 40 min stuck |

---

## 5.2 The 200 Essential Problems Roadmap

### Week 1-2: Arrays & Hashing (20 problems)

| # | Problem | Topics |
|---|---------|--------|
| 1 | Two Sum | HashMap |
| 2 | Contains Duplicate | HashSet |
| 3 | Valid Anagram | Frequency |
| 4 | Group Anagrams | HashMap |
| 5 | Top K Frequent Elements | Heap/Bucket |
| 6 | Product of Array Except Self | Prefix |
| 7 | Longest Consecutive Sequence | HashSet |
| 8 | Valid Sudoku | HashSet |
| 9 | Encode and Decode Strings | Design |
| 10 | Subarray Sum Equals K | Prefix + HashMap |
| 11 | Maximum Subarray | Kadane's |
| 12 | Maximum Product Subarray | DP |
| 13 | 3Sum | Two Pointers |
| 14 | Container With Most Water | Two Pointers |
| 15 | Trapping Rain Water | Two Pointers |
| 16 | Move Zeroes | Two Pointers |
| 17 | Sort Colors | Dutch Flag |
| 18 | Merge Intervals | Sorting |
| 19 | Insert Interval | Sorting |
| 20 | First Missing Positive | Cyclic Sort |

### Week 3-4: Two Pointers & Sliding Window (15 problems)

| # | Problem | Topics |
|---|---------|--------|
| 1 | Valid Palindrome | Two Pointers |
| 2 | Two Sum II (Sorted) | Two Pointers |
| 3 | 3Sum | Two Pointers |
| 4 | Container With Most Water | Two Pointers |
| 5 | Best Time to Buy/Sell Stock | Sliding Window |
| 6 | Longest Substring Without Repeating | Sliding Window |
| 7 | Longest Repeating Character Replacement | Sliding Window |
| 8 | Permutation in String | Sliding Window |
| 9 | Minimum Window Substring | Sliding Window |
| 10 | Sliding Window Maximum | Deque |
| 11 | Remove Duplicates from Sorted Array | Two Pointers |
| 12 | Remove Element | Two Pointers |
| 13 | Next Permutation | Two Pointers |
| 14 | Find All Anagrams | Sliding Window |
| 15 | Fruit Into Baskets | Sliding Window |

### Week 5-6: Stack & Queue (15 problems)

| # | Problem | Topics |
|---|---------|--------|
| 1 | Valid Parentheses | Stack |
| 2 | Min Stack | Design |
| 3 | Evaluate Reverse Polish Notation | Stack |
| 4 | Generate Parentheses | Backtracking |
| 5 | Daily Temperatures | Monotonic Stack |
| 6 | Car Fleet | Monotonic Stack |
| 7 | Largest Rectangle in Histogram | Monotonic Stack |
| 8 | Decode String | Stack |
| 9 | Asteroid Collision | Stack |
| 10 | Basic Calculator | Stack |
| 11 | Basic Calculator II | Stack |
| 12 | Implement Queue using Stacks | Design |
| 13 | Implement Stack using Queues | Design |
| 14 | Next Greater Element I | Monotonic Stack |
| 15 | Remove K Digits | Monotonic Stack |

### Week 7-8: Binary Search (15 problems)

| # | Problem | Topics |
|---|---------|--------|
| 1 | Binary Search | Standard |
| 2 | Search a 2D Matrix | Standard |
| 3 | Search in Rotated Sorted Array | Modified |
| 4 | Find Minimum in Rotated Sorted Array | Boundary |
| 5 | Find Peak Element | Boundary |
| 6 | Search in Rotated Sorted Array II | Modified |
| 7 | Find First and Last Position | Lower/Upper Bound |
| 8 | Time Based Key-Value Store | Design |
| 9 | Koko Eating Bananas | Answer Search |
| 10 | Capacity To Ship Packages | Answer Search |
| 11 | Split Array Largest Sum | Answer Search |
| 12 | Median of Two Sorted Arrays | Partition |
| 13 | Find K Closest Elements | Binary Search |
| 14 | Single Element in Sorted Array | Modified |
| 15 | Random Pick with Weight | Prefix + BS |

### Week 9-10: Linked Lists (15 problems)

| # | Problem | Topics |
|---|---------|--------|
| 1 | Reverse Linked List | Reversal |
| 2 | Merge Two Sorted Lists | Merge |
| 3 | Reorder List | Fast/Slow + Reversal |
| 4 | Remove Nth Node From End | Two Pointers |
| 5 | Copy List with Random Pointer | HashMap |
| 6 | Add Two Numbers | Math |
| 7 | Linked List Cycle | Fast/Slow |
| 8 | Linked List Cycle II | Floyd's |
| 9 | Find the Duplicate Number | Floyd's |
| 10 | LRU Cache | HashMap + DLL |
| 11 | LFU Cache | HashMap + DLL |
| 12 | Merge k Sorted Lists | Heap |
| 13 | Reverse Nodes in k-Group | Reversal |
| 14 | Swap Nodes in Pairs | Recursion |
| 15 | Palindrome Linked List | Fast/Slow |

### Week 11-13: Trees (25 problems)

| # | Problem | Topics |
|---|---------|--------|
| 1 | Invert Binary Tree | DFS |
| 2 | Maximum Depth of Binary Tree | DFS |
| 3 | Same Tree | DFS |
| 4 | Subtree of Another Tree | DFS |
| 5 | Lowest Common Ancestor of BST | BST |
| 6 | Binary Tree Level Order Traversal | BFS |
| 7 | Binary Tree Right Side View | BFS |
| 8 | Count Good Nodes in Binary Tree | DFS |
| 9 | Validate Binary Search Tree | DFS |
| 10 | Kth Smallest Element in BST | Inorder |
| 11 | Construct Binary Tree from Traversals | Recursion |
| 12 | Binary Tree Maximum Path Sum | DFS |
| 13 | Serialize and Deserialize Binary Tree | BFS/DFS |
| 14 | Diameter of Binary Tree | DFS |
| 15 | Balanced Binary Tree | DFS |
| 16 | Path Sum | DFS |
| 17 | Path Sum II | Backtracking |
| 18 | Path Sum III | Prefix Sum |
| 19 | Binary Search Tree Iterator | Stack |
| 20 | Populating Next Right Pointers | BFS |
| 21 | Flatten Binary Tree to Linked List | DFS |
| 22 | Sum Root to Leaf Numbers | DFS |
| 23 | Binary Tree Zigzag Level Order | BFS |
| 24 | Lowest Common Ancestor | DFS |
| 25 | Delete Node in BST | BST |

### Week 14-16: Graphs (25 problems)

| # | Problem | Topics |
|---|---------|--------|
| 1 | Number of Islands | DFS/BFS |
| 2 | Clone Graph | DFS/BFS |
| 3 | Max Area of Island | DFS |
| 4 | Pacific Atlantic Water Flow | DFS |
| 5 | Surrounded Regions | DFS/BFS |
| 6 | Rotting Oranges | Multi-source BFS |
| 7 | Walls and Gates | Multi-source BFS |
| 8 | Course Schedule | Topological Sort |
| 9 | Course Schedule II | Topological Sort |
| 10 | Redundant Connection | Union-Find |
| 11 | Number of Connected Components | Union-Find/DFS |
| 12 | Graph Valid Tree | Union-Find |
| 13 | Word Ladder | BFS |
| 14 | Alien Dictionary | Topological Sort |
| 15 | Network Delay Time | Dijkstra |
| 16 | Cheapest Flights K Stops | Modified BFS |
| 17 | Min Cost to Connect All Points | MST |
| 18 | Swim in Rising Water | Binary Search + BFS |
| 19 | Reconstruct Itinerary | Eulerian Path |
| 20 | Is Graph Bipartite | BFS/DFS |
| 21 | Shortest Path in Binary Matrix | BFS |
| 22 | Word Search | Backtracking |
| 23 | Word Search II | Trie + Backtracking |
| 24 | Open the Lock | BFS |
| 25 | Accounts Merge | Union-Find |

### Week 17-18: Heap & Priority Queue (12 problems)

| # | Problem | Topics |
|---|---------|--------|
| 1 | Kth Largest Element | Quick Select/Heap |
| 2 | Last Stone Weight | Max Heap |
| 3 | K Closest Points to Origin | Min Heap |
| 4 | Kth Largest Element in Stream | Min Heap |
| 5 | Task Scheduler | Max Heap + Greedy |
| 6 | Find Median from Data Stream | Two Heaps |
| 7 | Merge k Sorted Lists | Min Heap |
| 8 | Top K Frequent Elements | Bucket/Heap |
| 9 | Sort Characters By Frequency | Heap |
| 10 | Reorganize String | Max Heap |
| 11 | Ugly Number II | Min Heap |
| 12 | Smallest Range Covering K Lists | Min Heap |

### Week 19-21: Dynamic Programming (30 problems)

| # | Problem | Topics |
|---|---------|--------|
| 1 | Climbing Stairs | 1D DP |
| 2 | Min Cost Climbing Stairs | 1D DP |
| 3 | House Robber | 1D DP |
| 4 | House Robber II | Circular 1D DP |
| 5 | Longest Palindromic Substring | 2D DP |
| 6 | Palindromic Substrings | 2D DP |
| 7 | Decode Ways | 1D DP |
| 8 | Coin Change | Unbounded Knapsack |
| 9 | Coin Change II | Counting |
| 10 | Maximum Product Subarray | 1D DP |
| 11 | Word Break | 1D DP |
| 12 | Longest Increasing Subsequence | 1D DP/BS |
| 13 | Partition Equal Subset Sum | 0/1 Knapsack |
| 14 | Target Sum | 0/1 Knapsack |
| 15 | Unique Paths | 2D DP |
| 16 | Unique Paths II | 2D DP |
| 17 | Longest Common Subsequence | 2D DP |
| 18 | Edit Distance | 2D DP |
| 19 | Interleaving String | 2D DP |
| 20 | Distinct Subsequences | 2D DP |
| 21 | Best Time to Buy/Sell Stock (all) | State DP |
| 22 | Maximal Square | 2D DP |
| 23 | Jump Game | Greedy/DP |
| 24 | Jump Game II | Greedy/DP |
| 25 | Perfect Squares | Unbounded Knapsack |
| 26 | Regular Expression Matching | 2D DP |
| 27 | Wildcard Matching | 2D DP |
| 28 | Burst Balloons | Interval DP |
| 29 | Longest Valid Parentheses | 1D DP |
| 30 | Russian Doll Envelopes | LIS |

### Week 22-23: Backtracking (15 problems)

| # | Problem | Topics |
|---|---------|--------|
| 1 | Subsets | Generate |
| 2 | Subsets II | Generate + Skip |
| 3 | Permutations | Generate |
| 4 | Permutations II | Generate + Skip |
| 5 | Combination Sum | Unlimited |
| 6 | Combination Sum II | Limited |
| 7 | Combination Sum III | Constrained |
| 8 | Letter Combinations of Phone | Generate |
| 9 | Palindrome Partitioning | Partition |
| 10 | N-Queens | Constraint |
| 11 | N-Queens II | Counting |
| 12 | Sudoku Solver | Constraint |
| 13 | Word Search | Grid |
| 14 | Restore IP Addresses | Partition |
| 15 | Generate Parentheses | Valid Generate |

### Week 24: Greedy & Intervals (13 problems)

| # | Problem | Topics |
|---|---------|--------|
| 1 | Maximum Subarray | Kadane's |
| 2 | Jump Game | Greedy |
| 3 | Jump Game II | Greedy |
| 4 | Gas Station | Circular Greedy |
| 5 | Hand of Straights | HashMap + Sort |
| 6 | Merge Triplets | Greedy |
| 7 | Partition Labels | Greedy |
| 8 | Valid Parenthesis String | Greedy |
| 9 | Merge Intervals | Sort |
| 10 | Insert Interval | Sort |
| 11 | Non-overlapping Intervals | Interval Schedule |
| 12 | Meeting Rooms | Sorting |
| 13 | Meeting Rooms II | Min Heap |

---

## 5.3 Weekly Study Plan Template

```
MONDAY-WEDNESDAY: Learn new topic
- Read theory and patterns
- Study 2-3 example problems
- Solve 3-4 problems independently

THURSDAY-FRIDAY: Practice problems
- Solve 5-6 problems from that topic
- Mix easy and medium difficulty

SATURDAY: Review and hard problems
- Revisit problems you struggled with
- Attempt 1-2 hard problems

SUNDAY: Rest or light review
- Skim through week's concepts
- Organize notes
```

---

## 5.4 Interview Preparation Timeline

### 1 Month Before Interview
- Complete all Blind 75 problems
- Practice time management
- Review all patterns

### 2 Weeks Before Interview
- Focus on weak topics
- Do 3-4 mock interviews
- Practice explaining solutions

### 1 Week Before Interview
- Light practice (2-3 problems/day)
- Review common mistakes
- Mental preparation

### Day Before
- Light review only
- Rest well
- Prepare logistics

---

## 5.5 Resources

### Platforms
- **LeetCode**: Primary practice platform
- **NeetCode**: Curated lists and videos
- **AlgoExpert**: Structured learning
- **HackerRank**: Additional practice

### Books
- "Introduction to Algorithms" (CLRS)
- "Cracking the Coding Interview"
- "Elements of Programming Interviews"

### YouTube Channels
- NeetCode
- Abdul Bari
- William Fiset
- Back To Back SWE

---

## Phase 5 Checklist

- [ ] Created study schedule
- [ ] Completed 200 essential problems
- [ ] Reviewed all patterns
- [ ] Did mock interviews
- [ ] Identified and addressed weak areas
- [ ] Can explain solutions clearly

---

# 🎯 Final Summary

| Phase | Focus | Duration |
|-------|-------|----------|
| 1 | Foundation | 2-3 weeks |
| 2 | Data Structures | 4-6 weeks |
| 3 | Algorithm Paradigms | 6-8 weeks |
| 4 | Advanced Topics | 4-6 weeks |
| 5 | Practice & Review | Ongoing |

**Total Timeline: 4-6 months** with consistent 3-4 hours daily practice

---

> **Remember**: Mastery comes from understanding, not memorization. Focus on WHY solutions work, not just WHAT the solution is. Good luck on your DSA journey! 🚀
