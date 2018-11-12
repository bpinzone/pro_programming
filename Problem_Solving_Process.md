## Programming Problem Solving Process
This is a collection of processes, ideas, and useful information to go through for each stage of solving programming problems.
It's a mix of my own reflections and experiential insights, as well as advice from others at the end.
Some parts are specific to C++.
(benpinzone.io/psp Redirects to this raw document)
---
### Know and use the STL (Containers, Algorithms, Utils.)
Data Structures
* Class, Array, Vector, Linked List
* Deque, Stack, Queue, Priority Queue / Heap
* Sets
	* Ordered (default) or unordered
	* Single (default) or multi
	* Mind the STL functions: Intersection, differences, etc. (Apply to sorted vectors.)
* Maps
	* Ordered (default) or unordered
	* Single (default) or multi
* Union - Find (Unifying Disjoint Sets)
* Pair - Auto sorts by first, then seconds.
* Graphs
* Composition - Use one inside another.
* Combination - Use multiple alongside each other.
Algorithm Families
* Direct
* Brute Force
* Greedy
* Divide and Conquer
	* Recursion
	* Dynamic Programming - Overlapping sub-problems.
		* Must be able to form optimal solutions from optimal sub-solutions.
* Backtracking - Constraint Satisfaction
* Branch and Bound - Optimization
---
### Number One Priority: Understand the Question
* Am I actually understanding the question?
* State the objective clearly.
* Seek answers to clarifying questions until you do.
* Know when you simply do not understand the **problem statement**.
* Understand any existing test cases.
### Stuck?
* Narrow down the output space! If I don't know the answer, can I at least put bounds on it?
    * May lead to more insight.
* Which populated data structure(s) do I wish I had?
    * If you had this structure, the problem would be trivial.
* What CAN I do? What will the result of those can-do actions be?
* What first step am I forced to take?
* Be clever - see section.
* If you have a partial solution- Think about what you want it to do fundamentally, and state what it presently does clearly.
### Always
* Do it yourself!
    * Identify YOUR operations extremely specifically.
        * In most cases, if you can't do it, you can't program a computer to do it.
    * Pretend you have a perfect memory as a human.