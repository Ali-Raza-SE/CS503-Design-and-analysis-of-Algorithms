# CS-503 — Design and Analysis of Algorithms

## Module 1: Introduction to Algorithms

This lecture is designed for **classroom teaching**. I’ll keep the language simple, but include the important **definitions, formulas, examples, algorithms, and technical concepts** students need before starting complexity analysis.

---

# 1. Introduction to Algorithms

## 1.1 What is an Algorithm?

An **algorithm** is a finite sequence of well-defined steps used to solve a problem or perform a task.

### Simple Definition

> **An algorithm is a step-by-step procedure for solving a problem.**

For example, suppose we want to find the largest number among three numbers:

**Input:** `10, 25, 15`

**Steps:**

1. Take the first number as the largest.
2. Compare it with the second number.
3. If the second number is larger, update the largest.
4. Compare the largest with the third number.
5. Display the largest number.

**Output:** `25`

So:

$$
\boxed{\text{Input} \rightarrow \text{Algorithm} \rightarrow \text{Output}}
$$

---

# 2. Algorithm vs Program

Students often confuse an **algorithm** with a **program**.

### Algorithm

An algorithm is the **logic or solution method**.

### Program

A program is the **implementation of an algorithm in a programming language**.

For example:

### Algorithm

```text
1. Read two numbers
2. Add them
3. Display the result
```

### Python Program

```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))

sum = a + b

print(sum)
```

The algorithm explains **what to do**.

The program tells the computer **how to implement it in a particular language**.

### Quick Comparison

| Algorithm                            | Program                            |
| ------------------------------------ | ---------------------------------- |
| Problem-solving procedure            | Implementation                     |
| Language independent                 | Language dependent                 |
| Written using steps/pseudocode       | Written using programming language |
| Focuses on logic                     | Focuses on execution               |
| Can be implemented in many languages | Written in a specific language     |

---

# 3. Why Do We Need Algorithms?

Almost every computational problem requires an algorithm.

Examples:

* Searching for a student in a database
* Sorting student marks
* Finding the shortest route
* Calculating salary
* Checking whether a number is prime
* Finding the largest element
* Compressing a file
* Searching Google
* Processing transactions
* Finding the shortest path in a network

The important point is:

> **A computer does not solve a problem by itself. We provide a systematic procedure—the algorithm.**

---

# 4. Characteristics of an Algorithm

A good algorithm generally has the following characteristics:

1. **Input**
2. **Output**
3. **Definiteness**
4. **Finiteness**
5. **Effectiveness**
6. **Correctness**
7. **Generality**

Let's understand each.

---

## 4.1 Input

An algorithm should accept **zero or more inputs**.

### Example

Algorithm for adding two numbers:

```text
Input: A, B
```

Here:

$$
A=10,\quad B=20
$$

are inputs.

### Definition

> **Input is the data provided to an algorithm before execution.**

---

# 4.2 Output

An algorithm should produce **at least one output/result**.

For addition:

```text
Input:
A = 10
B = 20

Output:
30
```

### Definition

> **Output is the result produced by an algorithm.**

---

# 4.3 Definiteness

Every step of an algorithm must be **clear and unambiguous**.

For example:

```text
Add A and B
```

is definite.

But:

```text
Do something useful
```

is not definite.

The computer should know exactly what each instruction means.

### Definition

> **Definiteness means every step of an algorithm must be precisely and unambiguously defined.**

---

# 4.4 Finiteness

An algorithm must eventually terminate.

It cannot continue forever.

For example:

```text
1. Read A
2. Read B
3. Calculate A + B
4. Display result
5. Stop
```

It terminates after a finite number of steps.

### Definition

> **Finiteness means an algorithm must terminate after a finite number of steps.**

---

# 4.5 Effectiveness

Every operation should be basic enough that it can actually be performed.

For example:

```text
1. Read A
2. Read B
3. Add A and B
4. Display result
```

Each operation is executable.

### Definition

> **Effectiveness means every step of an algorithm must be sufficiently basic and executable in a finite amount of time.**

---

# 4.6 Correctness

An algorithm must produce the **right answer** for valid inputs.

Suppose an algorithm is designed to calculate:

$$
A+B
$$

For:

$$
A=10,\ B=20
$$

the result must be:

$$
30
$$

If it produces `25`, the algorithm is incorrect.

---

# 4.7 Generality

An algorithm should solve a **general class of problems**, not just one specific example.

For example:

Bad algorithm:

```text
1. Take 10
2. Add 20
3. Print 30
```

This only solves one case.

Better algorithm:

```text
1. Read A
2. Read B
3. Sum = A + B
4. Print Sum
```

This works for:

```text
10 + 20
5 + 7
100 + 250
-5 + 10
```

---

# 5. Characteristics — Quick Table

| Characteristic    | Meaning                         |
| ----------------- | ------------------------------- |
| **Input**         | Data given to algorithm         |
| **Output**        | Result produced                 |
| **Definiteness**  | Every step is clear             |
| **Finiteness**    | Algorithm eventually terminates |
| **Effectiveness** | Steps are executable            |
| **Correctness**   | Produces the correct result     |
| **Generality**    | Works for a general problem     |

### Memory Trick

Remember:

> **I-D-F-E-C-G**

**I**nput
**D**efiniteness
**F**initeness
**E**ffectiveness
**C**orrectness
**G**enerality

---

# 6. Algorithmic Problem Solving

Algorithmic problem solving means using a **systematic computational approach** to solve a problem.

Instead of immediately writing code, we first understand the problem and design a solution.

---

## 6.1 Basic Problem-Solving Model

A simple model is:

$$
\boxed{\text{Problem} \rightarrow \text{Algorithm} \rightarrow \text{Program} \rightarrow \text{Output}}
$$

For example:

### Problem

Find the largest number in a list.

### Algorithm

Compare elements one by one and keep track of the largest.

### Program

Implement the algorithm using Python/Java/C++.

### Output

Largest number.

---

# 7. Steps of Algorithmic Problem Solving

A systematic approach can be:

### Step 1 — Understand the Problem

Ask:

* What is the problem?
* What information is given?
* What result is required?

---

### Step 2 — Identify Inputs

Determine what data is provided.

Example:

```text
A list of numbers
```

---

### Step 3 — Identify Outputs

Determine what the algorithm should produce.

Example:

```text
Largest number
```

---

### Step 4 — Determine Constraints

Understand restrictions on the input.

For example:

```text
1 ≤ n ≤ 1,000,000
```

This is important because the input size can affect algorithm selection.

---

### Step 5 — Develop a Solution

Think of possible approaches.

For example, to find an element:

* Linear Search
* Binary Search

---

### Step 6 — Write the Algorithm

Use:

* Natural language
* Pseudocode
* Flowchart

---

### Step 7 — Prove/Check Correctness

Make sure the algorithm produces the required answer.

---

### Step 8 — Analyze the Algorithm

Determine:

* Time required
* Memory required

This introduces the concepts of:

$$
\text{Time Complexity}
$$

and

$$
\text{Space Complexity}
$$

which we will study in detail in later modules.

---

### Step 9 — Implement

Convert the algorithm into a programming language.

---

### Step 10 — Test

Use different inputs, including:

* Normal cases
* Boundary cases
* Invalid cases
* Large inputs

---

# 8. Analyzing Algorithms

Algorithm analysis means evaluating how efficiently an algorithm solves a problem.

We mainly analyze two resources:

### 1. Time

How much computational work does the algorithm perform?

### 2. Space

How much memory does the algorithm require?

Therefore:

$$
\boxed{\text{Algorithm Analysis} =
\text{Time Analysis} + \text{Space Analysis}}
$$

---

# 9. Time Complexity

Time complexity describes how the running time of an algorithm **grows with input size**.

Let:

$$
n = \text{size of input}
$$

We represent running time as:

$$
T(n)
$$

For example, if an algorithm processes every element once:

$$
T(n)=cn
$$

where \(c\) represents the constant amount of work per element.

We normally simplify this as:

$$
\boxed{T(n)=O(n)}
$$

Don't worry about the detailed Big-O rules yet. They will be covered in the next modules.

---

# 10. Space Complexity

Space complexity describes how much memory an algorithm requires as the input size increases.

For example, if an algorithm creates an additional array of size \(n\):

$$
S(n)=O(n)
$$

If it only uses a few variables:

$$
S(n)=O(1)
$$

---

# 11. Designing Algorithms

Algorithm design means developing a systematic procedure to solve a problem efficiently.

There can be **multiple algorithms for the same problem**.

For example, suppose we need to search for a value in a sorted array.

We can use:

### Linear Search

Check elements one by one.

$$
O(n)
$$

### Binary Search

Repeatedly divide the search space into two halves.

$$
O(\log n)
$$

Both solve the same problem, but Binary Search is generally much more efficient for a sorted array.

This demonstrates an important idea:

> **Correctness alone is not enough; we also care about efficiency.**

---

# 12. Algorithm Design Process

A practical algorithm design process can be divided into the following stages:

```text
Problem Definition
       ↓
Input / Output Identification
       ↓
Constraints
       ↓
Possible Solutions
       ↓
Select Design Approach
       ↓
Write Algorithm / Pseudocode
       ↓
Prove Correctness
       ↓
Analyze Complexity
       ↓
Implement
       ↓
Test
       ↓
Improve
```

---

# 13. Step 1 — Problem Definition

Clearly define what needs to be solved.

### Example

> Given an array of integers, find the largest element.

Input:

$$
A=[10,25,7,40,18]
$$

Output:

$$
40
$$

---

# 14. Step 2 — Identify Input and Output

### Input

An array:

$$
A[0...n-1]
$$

### Output

Largest element:

$$
max
$$

---

# 15. Step 3 — Consider Constraints

Suppose:

$$
1 \le n \le 10^6
$$

Now we know that the algorithm may need to process up to one million elements.

This influences our design.

---

# 16. Step 4 — Develop Possible Solutions

For finding the largest element, one simple solution is:

1. Assume first element is largest.
2. Compare it with every remaining element.
3. Update largest whenever a bigger element is found.

---

# 17. Step 5 — Write Pseudocode

### Pseudocode

```text
Algorithm FindMax(A, n)

1. max ← A[0]

2. for i ← 1 to n - 1 do
3.     if A[i] > max then
4.         max ← A[i]
5.     end if
6. end for

7. return max
```

---

# 18. Step 6 — Prove Correctness

We need to establish that the algorithm actually returns the largest element.

Initially:

$$
max=A[0]
$$

After processing each element, `max` contains the largest element seen so far.

After all \(n\) elements are processed:

$$
max=\max(A[0],A[1],...,A[n-1])
$$

Therefore, the algorithm returns the largest element.

---

# 19. Step 7 — Analyze Complexity

The algorithm checks every element once.

Therefore:

$$
T(n)=c_1+c_2n
$$

Ignoring constants and lower-order terms:

$$
\boxed{T(n)=O(n)}
$$

It uses only one extra variable:

$$
\boxed{S(n)=O(1)}
$$

---

# 20. Correctness of Algorithms

Correctness is one of the most important concepts in algorithm design.

### Definition

> An algorithm is correct if it produces the required output for every valid input according to the problem specification.

There are two important aspects:

### Partial Correctness

If the algorithm terminates, the answer is correct.

### Termination

The algorithm eventually stops.

Together:

$$
\boxed{\text{Correctness} =
\text{Partial Correctness} + \text{Termination}}
$$

---

# 21. Example of an Incorrect Algorithm

Suppose the problem is:

> Find the maximum of two numbers.

Incorrect algorithm:

```text
Algorithm Maximum(A, B)

1. If A > B
2.     return A
```

What happens when:

$$
A=5,\ B=10
$$

The algorithm produces no answer.

Therefore, it is not correct for all valid inputs.

---

# 22. Proving Correctness

There are several techniques for proving algorithm correctness.

At this stage, the most important ideas are:

1. **Logical reasoning**
2. **Mathematical induction**
3. **Loop invariants**

We will later study mathematical induction and formal analysis in greater detail.

---

# 23. Loop Invariant

A **loop invariant** is a condition that remains true before and after each iteration of a loop.

It is commonly used to prove the correctness of iterative algorithms.

### Example: Finding Maximum

Consider:

```text
max ← A[0]

for i ← 1 to n-1
    if A[i] > max
        max ← A[i]
```

### Invariant

> Before each iteration, `max` contains the largest element among the elements already processed.

Initially:

$$
max=A[0]
$$

So the invariant is true.

After each iteration, if a larger value is found, `max` is updated.

At termination, all elements have been processed.

Therefore:

$$
max=\text{largest element}
$$

---

# 24. Simple Algorithm Example 1 — Add Two Numbers

### Problem

Add two numbers.

### Algorithm

```text
Algorithm Add(A, B)

1. Read A
2. Read B
3. Sum ← A + B
4. Return Sum
```

### Example

$$
A=10
$$

$$
B=20
$$

Therefore:

$$
Sum=10+20=30
$$

### Complexity

Only one addition is performed.

$$
\boxed{T(n)=O(1)}
$$

assuming fixed-size input values.

---

# 25. Simple Algorithm Example 2 — Check Even or Odd

### Problem

Determine whether a number is even or odd.

### Key Formula

A number \(n\) is even if:

$$
n\bmod 2=0
$$

Otherwise, it is odd.

### Algorithm

```text
Algorithm EvenOdd(n)

1. If n mod 2 = 0
2.     Print "Even"
3. Else
4.     Print "Odd"
```

### Example

$$
n=12
$$

$$
12\bmod2=0
$$

Therefore:

```text
12 is Even
```

---

# 26. Simple Algorithm Example 3 — Find Maximum of Two Numbers

### Algorithm

```text
Algorithm Maximum(A, B)

1. If A > B
2.     return A
3. Else
4.     return B
```

### Example

$$
A=25,\quad B=15
$$

Since:

$$
25>15
$$

Output:

$$
25
$$

---

# 27. Simple Algorithm Example 4 — Find Maximum in an Array

### Problem

Find the largest number in:

$$
[5,9,2,15,7]
$$

### Algorithm

```text
Algorithm FindMax(A, n)

1. max ← A[0]

2. for i ← 1 to n-1
3.     if A[i] > max
4.         max ← A[i]

5. return max
```

### Dry Run

| Step    | Current Element | max |
| ------- | --------------: | --: |
| Initial |               5 |   5 |
| 1       |               9 |   9 |
| 2       |               2 |   9 |
| 3       |              15 |  15 |
| 4       |               7 |  15 |

Final result:

$$
\boxed{15}
$$

---

# 28. Simple Algorithm Example 5 — Linear Search

### Problem

Find a target value in an array.

Array:

$$
A=[10,20,30,40,50]
$$

Target:

$$
40
$$

### Algorithm

```text
Algorithm LinearSearch(A, n, key)

1. for i ← 0 to n-1
2.     if A[i] = key
3.         return i
4. return -1
```

### Dry Run

Search for `40`:

```text
10 ≠ 40
20 ≠ 40
30 ≠ 40
40 = 40
```

Therefore:

$$
\boxed{\text{Index}=3}
$$

### Complexity

In the worst case, we may check all \(n\) elements:

$$
\boxed{O(n)}
$$

---

# 29. Simple Algorithm Example 6 — Calculate Factorial

The factorial of \(n\) is:

$$
\boxed{n!=n(n-1)(n-2)\cdots2(1)}
$$

For example:

$$
5!=5\times4\times3\times2\times1
$$

$$
5!=120
$$

### Iterative Algorithm

```text
Algorithm Factorial(n)

1. fact ← 1
2. for i ← 1 to n
3.     fact ← fact × i
4. return fact
```

### Example

For \(n=5\):

```text
fact = 1

i = 1 → fact = 1
i = 2 → fact = 2
i = 3 → fact = 6
i = 4 → fact = 24
i = 5 → fact = 120
```

Output:

$$
\boxed{120}
$$

---

# 30. Simple Algorithm Example 7 — Calculate Average

Suppose:

$$
A=[10,20,30,40]
$$

The average is:

$$
\boxed{\text{Average}=\frac{\text{Sum of elements}}{\text{Number of elements}}}
$$

Therefore:

$$
Average=\frac{10+20+30+40}{4}
$$

$$
Average=\frac{100}{4}=25
$$

### Algorithm

```text
Algorithm Average(A, n)

1. sum ← 0

2. for i ← 0 to n-1
3.     sum ← sum + A[i]

4. average ← sum / n

5. return average
```

The loop executes \(n\) times:

$$
\boxed{T(n)=O(n)}
$$

---

# 31. Simple Algorithm Example 8 — Check Prime Number

A number greater than 1 is **prime** if it has exactly two positive divisors:

$$
1
$$

and itself.

Examples:

$$
2,3,5,7,11,13
$$

are prime.

### Simple Algorithm

```text
Algorithm IsPrime(n)

1. If n < 2
2.     return False

3. for i ← 2 to n-1
4.     if n mod i = 0
5.         return False

6. return True
```

### Example

For:

$$
n=7
$$

Check:

$$
7\bmod2\neq0
$$

$$
7\bmod3\neq0
$$

$$
7\bmod4\neq0
$$

$$
7\bmod5\neq0
$$

$$
7\bmod6\neq0
$$

Therefore:

$$
\boxed{7\text{ is Prime}}
$$

---

# 32. Algorithm Design Techniques

When designing algorithms, different strategies can be used.

Some important techniques that students will study later include:

| Technique                 | Basic Idea                                 |
| ------------------------- | ------------------------------------------ |
| **Brute Force**           | Try possible solutions directly            |
| **Divide and Conquer**    | Divide problem into smaller subproblems    |
| **Greedy**                | Make the best local choice                 |
| **Dynamic Programming**   | Store solutions to overlapping subproblems |
| **Backtracking**          | Build solution and undo when necessary     |
| **Randomized Algorithms** | Use randomness in decision making          |

For CS-503, these techniques become increasingly important as the course progresses.

---

# 33. Correctness vs Efficiency

A very important concept:

> **An algorithm must first be correct, and then we try to make it efficient.**

Consider two algorithms:

### Algorithm A

Correct but:

$$
O(n^2)
$$

### Algorithm B

Correct and:

$$
O(n\log n)
$$

For large input sizes, Algorithm B is generally preferable.

So algorithm design considers:

$$
\boxed{\text{Correctness + Efficiency}}
$$

---

# 34. Algorithm Quality

A good algorithm should ideally have:

* Correctness
* Efficiency
* Simplicity
* Clarity
* Maintainability
* Generality
* Scalability

Among these, **correctness and efficiency** are particularly important in DAA.

---

# 35. Algorithm Representation

Algorithms can be represented in several ways.

### 1. Natural Language

```text
Take two numbers.
Add them.
Display the result.
```

### 2. Pseudocode

```text
Sum ← A + B
```

### 3. Flowchart

Graphical representation using symbols.

### 4. Programming Language

```python
sum = a + b
```

For DAA, **pseudocode** is especially useful because it focuses on algorithmic logic rather than language-specific syntax.

---

# 36. Important Mathematical Notation

Students should become familiar with:

### Input Size

$$
n
$$

### Running Time

$$
T(n)
$$

### Space

$$
S(n)
$$

### Summation

$$
\sum_{i=1}^{n} i
$$

For example:

$$
1+2+3+\cdots+n
$$

has the formula:

$$
\boxed{\sum_{i=1}^{n}i=\frac{n(n+1)}{2}}
$$

### Factorial

$$
\boxed{n!=n(n-1)(n-2)\cdots1}
$$

### Logarithm

$$
\boxed{\log_2 n}
$$

These mathematical concepts become very important when analyzing algorithm complexity.

---

# 37. Worked Example — Algorithm for Sum of First n Numbers

### Problem

Calculate:

$$
1+2+3+\cdots+n
$$

---

## Approach 1 — Loop

```text
Algorithm Sum(n)

1. sum ← 0
2. for i ← 1 to n
3.     sum ← sum + i
4. return sum
```

For:

$$
n=5
$$

we get:

$$
1+2+3+4+5=15
$$

The loop runs \(n\) times:

$$
T(n)=O(n)
$$

---

## Approach 2 — Mathematical Formula

We know:

$$
\boxed{Sum=\frac{n(n+1)}{2}}
$$

For:

$$
n=5
$$

$$
Sum=\frac{5(6)}{2}
$$

$$
Sum=15
$$

This approach performs a constant number of operations:

$$
\boxed{T(n)=O(1)}
$$

### Important Lesson

Both algorithms are correct, but the second approach is more efficient for very large \(n\).

This is exactly why we study **Design and Analysis of Algorithms**.

---

# 38. Algorithm Analysis Example

Suppose we have:

```text
for i = 1 to n
    print(i)
```

The statement executes:

$$
n
$$

times.

Therefore:

$$
T(n)=cn
$$

Ignoring the constant:

$$
\boxed{T(n)=O(n)}
$$

---

Now consider:

```text
for i = 1 to n
    for j = 1 to n
        print(i,j)
```

The outer loop executes \(n\) times.

For every outer iteration, the inner loop executes \(n\) times.

Therefore:

$$
n\times n=n^2
$$

So:

$$
\boxed{T(n)=O(n^2)}
$$

This will be studied formally in the **Asymptotic Analysis module**.

---

# 39. Algorithm vs Data Structure

Another important distinction:

### Algorithm

Defines the procedure for solving a problem.

### Data Structure

Defines how data is organized/stored.

Examples of data structures:

* Array
* Linked List
* Stack
* Queue
* Tree
* Graph
* Hash Table

An algorithm often uses one or more data structures.

For example:

> **Binary Search Algorithm + Sorted Array**

So:

$$
\boxed{\text{Efficient Algorithm} + \text{Suitable Data Structure}}
$$

can produce a highly efficient solution.

---

# 40. Real-World Example — Google Search

Suppose millions of web pages exist.

A search engine needs to find relevant pages quickly.

A simple approach of checking every page one by one would be extremely inefficient.

Therefore, search engines use sophisticated:

* Data structures
* Searching algorithms
* Ranking algorithms
* Graph algorithms
* Distributed algorithms

This demonstrates why algorithm efficiency matters in real-world systems.

---

# 41. Module 1 — Quick Revision Table

| Concept                | Simple Definition                                 |
| ---------------------- | ------------------------------------------------- |
| **Algorithm**          | Step-by-step solution to a problem                |
| **Input**              | Data given to algorithm                           |
| **Output**             | Result produced                                   |
| **Definiteness**       | Steps are clear and unambiguous                   |
| **Finiteness**         | Algorithm terminates                              |
| **Effectiveness**      | Steps are executable                              |
| **Correctness**        | Produces correct result                           |
| **Generality**         | Works for general inputs                          |
| **Time Complexity**    | Growth of computational time                      |
| **Space Complexity**   | Growth of memory requirement                      |
| **Pseudocode**         | Language-independent algorithm description        |
| **Algorithm Design**   | Developing a solution procedure                   |
| **Algorithm Analysis** | Evaluating efficiency                             |
| **Loop Invariant**     | Condition that remains true during loop execution |

---

# 42. Important Formulas for Module 1

### Sum of first \(n\) natural numbers

$$
\boxed{\sum_{i=1}^{n}i=\frac{n(n+1)}{2}}
$$

### Factorial

$$
\boxed{n!=n(n-1)(n-2)\cdots1}
$$

### Average

$$
\boxed{Average=\frac{\text{Sum}}{\text{Number of Elements}}}
$$

### Basic Time Representation

$$
\boxed{T(n)=\text{running time as a function of input size}}
$$

### Basic Space Representation

$$
\boxed{S(n)=\text{memory requirement as a function of input size}}
$$

### Correctness

$$
\boxed{\text{Correctness}=\text{Partial Correctness}+\text{Termination}}
$$

---

# 43. Exam-Oriented Questions

### Short Questions

1. Define an algorithm.
2. What is the difference between an algorithm and a program?
3. What is meant by definiteness?
4. Explain finiteness with an example.
5. What is algorithmic problem solving?
6. Define correctness of an algorithm.
7. What is time complexity?
8. What is space complexity?
9. What is pseudocode?
10. What is a loop invariant?

### Long Questions

1. Explain the characteristics of an algorithm with suitable examples.
2. Explain the complete algorithm design process.
3. Explain algorithmic problem solving with an example.
4. Explain algorithm analysis and distinguish between time and space complexity.
5. Explain correctness of algorithms and the role of loop invariants.
6. Design an algorithm to find the maximum element of an array and explain its correctness.
7. Design and analyze an algorithm for linear search.
8. Compare two different approaches for calculating the sum of the first \(n\) natural numbers.

---

# 44. Key Takeaways

Students should remember these **five core ideas** from Module 1:

### 1. Algorithm

> A finite sequence of clear steps used to solve a problem.

### 2. Good Algorithm

Should be:

$$
\boxed{\text{Clear + Finite + Effective + Correct + General}}
$$

### 3. Algorithmic Problem Solving

$$
\boxed{\text{Understand Problem → Design → Prove → Analyze → Implement → Test}}
$$

### 4. Algorithm Analysis

Mainly studies:

$$
\boxed{\text{Time Complexity + Space Complexity}}
$$

### 5. Algorithm Design

A solution should not only work; it should work **correctly and efficiently**.

---

## Module 1 → What Comes Next?

After students understand **what an algorithm is, how to design one, and why we analyze it**, the natural next step is **Module 2: Mathematical Foundations for Algorithm Analysis**, followed by **Asymptotic Analysis (Big-O, Ω, Θ, o, ω)**.

That foundation will allow students to mathematically answer the key DAA question:

> **“How efficient is this algorithm when the input becomes very large?”**
