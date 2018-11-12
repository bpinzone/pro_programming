## Programming Problem Solving Process>
  
This is a collection of processes, ideas, and useful information to go through for each stage of solving programming problems.
It's a mix of my own reflections and experiential insights, as well as advice from others at the end.
Some parts are specific to C++.
(benpinzone.io/psp Redirects here)
---
### Know and use the STL (Containers, Algorithms, Utils.)
  
**Data Structures**
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
  
**Algorithm Families**
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
---
### Stuck?
* Narrow down the output space! If I don't know the answer, can I at least put bounds on it?
    * May lead to more insight.
* Which populated data structure(s) do I wish I had?
    * If you had this structure, the problem would be trivial.
* What CAN I do? What will the result of those can-do actions be?
* What first step am I forced to take?
* Be clever - see section.
* If you have a partial solution- Think about what you want it to do fundamentally, and state what it presently does clearly.
---
### Always
* Do it yourself!
    * Identify YOUR operations extremely specifically.
        * In most cases, if you can't do it, you can't program a computer to do it.
    * Pretend you have a perfect memory as a human.
---
### Misc
* If you're asked about the existence of a solution or the value of some property (count the number of swaps necessary, etc), keep in mind you probably won't need to write the entire algorithm that would actually determine that result. Just some theoretical analysis. Use counting techniques, set theory, etc.
* Once you have the main idea and you are confident in the algorithm, DO NOT forget to work out all minute details.
    * BE the computer. Be the compiler. Forget what the code is supposed to do. See what it does.
* Just try something.
* Try inverting the problem statement of 'what I want to do':
    * 'I want to take out the least expensive edges' ->
    * 'I want to put in the most expensive edges'
* You always have access to a stack through recursion.
* Narrow down the output space.
* Do not make graph problems too complicated.
* When the solution involves complicated conditions for collections of ordered elements regarding indices, positions, etc, start building the solution requirements (boolean expressions) with those indices as being variables.
* Think carefully about final return values.
---
### Don't be Blind
* If visualization would greatly help, and you don't have it, you're BLIND!
* Am I missing anything obvious?
* Do not get hung up on one aspect of the problem.
* Take a step back and look at details that you weren't focusing on before- access modifiers, etc.
* What language subtleties might I correct?
    * Access modifiers, inline statics, etc.
* Many pointers? DRAW IT. ie linked list problems.
---
### Bridging the Gap
* What do I have?
* What do I know?
* What are my tools?

* What additional information would be helpful?
* What additional basic information could I compute easily?
    * Try counting things, running all your data through any functions provided.

* What can I theoretically know?
* What can I do with the resources I have?
* What (data) can I generate? How can I use that?
    * What if I ran everything? (All provided data through all provided functions.)

* What first step am I forced to take?

* What do I wish I had?
    * If you had this structure, the problem would be trivial.

* What final result/product/populated data structure do I want in the end?
    * Work backwards! (ie, if I had x, the problem would be solved. How do I generate x?)
---
### Regarding Data Structures
* Decide what sort of functionality you need.
    * What do you want/need to do? and quickly?
    * What is done a lot?
    * What operation is most important?
* Think
    * What structure should I use?
    * Run through each, not limiting yourself to one.
    * If you're having trouble deciding, consider using a combination or composition.
---
### Being Clever
* Visualize the Data! In any way that you can!
* Observe basic sample cases. What if I did this?
* What is really going on here, fundamentally?
    * If you are given some entity/function, ask- What IS this, fundamentally?
        * Is there a superfluous transformation going on?
            * Something may just be a saturating counter, decoder, or mux.
* The data that I am working with- What else can it represent in terms of this specific problem? What else can I do with it?
    * ie characters are integers. Use fingerprints.
    * ie values can be pointers into vector.
* Try something weird.
---
### Regarding Input Cases
* Small enumeration is not bad.
    * If pre-conditions vary, enumerating 4-6 cases may be necessary.
* What cases are special? When will my current code not work?
* Which cases are easy? How can I make others more like those? Can I find a rule here?
---
### Reduction
* What other problems does this seem similar to?
* Run through algorithm families.
* Particularly cycle detection with limited knowledge.
---
### Existence of Solution Problems:
* Making your algorithm more efficient:
    * Ask the following for two cases: What will my algorithm do? What are the time bounds for that case? When can I stop?
        * If there is a solution.
        * If there isn't a solution.
---
### Complexity
* Can I get my solution to a lower complexity?
* If you don't think you can do better, prove it!
* Hard recurrence relation? Draw a 2D call grid. Shape may emerge.
    * ie Triangle over call graph of x,y inputs -> O(n^2)
* Average out the worst case.
* BUD - Bottleneck, Unnecessary work, Duplicated work.
---
### In General for Interviews
* Talk through your thought process.
* Ensure your basic approach is understood.
* Write moderately detailed pseudo code first.
---
### Various Types of Questions
* String questions
    * Substring Stuff- use DP
        * Or even collection subset questions - DP
    * Hard Linear Best Conceived Runtime- use a state machine!
    * General
        * Characters are integer encodings. Use this to your advantage. (Finding an extra character in a string, etc.)
        * Find a good way to manage indices/iterators for hard linear BCR.
---
### Excellent STL
* is_permutation
* equal
* transform
* unique
* is_partitioned, partition, partition_point
* for_each
* find_if
* replace_if
* And all other variants of regex: .*[copy]?[if]?
---
### New / To Consolidate
Identify 3-5 Critical Pieces
* Actively identify any bad assumptions you may have made unintentionally.
Other New
* Do not trip over your own complexity.
    * Try not to have a data structure serve more than one purpose if there are no benefits.
    * Make sure stopping conditions on loops are as specific as they should be.
    * If a design starts getting out of hand, make it more modular, and state PRECISELY what an entity of code should accomplish.
    * Don't make a loop have two purposes. One loop, one job.
New From Operating Systems.
* General
    * Have an incomplete initial idea? Just go for it and start reasoning about it.
    * State what you want/need clearly. (And in technical terms!!! Be specific with yourself.)
    * Again - Just try something.
    * Again - Small enumeration is not bad.
    * Ask yourself the right questions.
    * Having trouble implementing a detail of a design? A problem clearly stated is half solved.
        * ie Some entity doesn't have access to the instance of class x THAT INVOKED ME... (So give that entity a pointer!)
    * Clarity of Design
        * Do NOT instantiate superfluous objects.
        * Think like Connamacher.
        * When you need clarity, think only of fundamental definitions of:
            * your tools
            * the fundamental desired outcome of what you are building.
    * Understanding the question
        * Read every single word carefully.
        * Do not make un-warranted assumptions. PAY ATTENTION TO PLURALITY (s).
        * Know your responsibilities. (maintaining structures, etc.)
        * When you think you're done, re-read the question and go through like a checklist.
        * Am I making any incorrect assumptions?
    * Make no assumptions about objects that users give you as input. Especially in set theory.
        * Ask - For what user input will this not work. Now also, YOU - try to break it as if you're malicious.
        * ex: Do not assume give mutex pointer sets are disjoint.
    * ACTIVELY try to come up with assumptions you may have unintentionally made.
    * ACTIVELY ask yourself - What do I want, in technical terms?
* Specific
    * Pointers solve everything. -P Chen. Muxes solve everything. - M Brehob.
    * Better safe than sorry with locks and guards. Just don't cause deadlock.
    * 'What is the problem with concept x' -> 'What problems might occur if we use concept x?'
    * Review P2 Design.
    * Highly Specific
        * Check if queues are empty.
        * Locks and CVs
            * You never know how the world has changed when you give up and re-acquire a lock.
            * When you return from wait, you have the lock.
        * Deadlock - when NO ONE can make progress.
            * State the condition such that not a single entity can make progress. How many entities are there?
        * Review get,set,make context.
            * set: set processor context to that pointed to by arg (ucontext_t*).
            * get: get processor context and store it into that pointed to by arg (ucontext_t*).
            * make: make processor context out of: (func, num_args, args...) and store it into that pointed to by arg (ucontext_t*).
            * Use dynamic bools.
---
### Other People's Processes
* Get P Chen's. TODO.
* Paoleti
    * Greedy
    * Divide and conquer
    * Dynamic program
    * Backtracking or Branch + Bound
* Random Dude
    * "What's the question?" In my case, I can trace 80% of the instances where I mis-answered to my getting the question wrong and not realizing that I had gotten the question wrong.
        * FYI, in the other 20% of instances, I simply did not get the question.
    * "What information do I have to work with"?
    * "What information do I need to answer the question and that I don't have?"
    * "If I don't have the info I need, what assumptions can I safely make?"
    * "How do I go about checking my assumptions and verifying the integrity of the facts that I am working with?"
