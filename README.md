[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/FgMJElkj)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.

## Question 1
1) Asymtotic analysis considers contant factors as negligable, but depending on the input size it can make a considerable actual performance and memory consumption. For example if we only want to use small inputs, and one algorithm with alot of constant facotors has complexity of (logn) and another has (n^2), asymtotic analysis would lead us to beleive the (logn) would be better, but it might actually run slower than the (n^2) algorithm with the constant factors. 

2) Asymtotic analaysis doesn't consider the machine specifications, things such as processor speed, cache size, or even just the complier used can effect the speed and effiecency of an algorithm. Almost no machine run the exact same as another, and these differences can make one algorithm more favorable than another.

3) Asymptotic analysis analyzes the inherent complexity of an algorithm itself. The actual performance can be heavily influenced by the programmer's implementation choices, coding style, and chosen data structures. A well-implemented algorithm with a higher asymptotic complexity might outperform a poorly implemented one with a lower complexity.

## Question 2: 
The asymtotic complexity of a binary search is O(log(n)), thus if $\frac{5}{3} log(1000) = 5$, I would say the run time for n = 10000 would be around $\frac{5}{3} log(10000) \approx 6.666$


## Question 3
1) This could be a hardware problem, where certain aspects of the the machine's hardware made it process the input slower. This can happen when the input is larger than the cache so part of the input gets stored in a  memory with slower access, or if the other processes running on the machine are competing for memory and CPU resources. 

2) It could be that the search algorithm has is working on an unbalanced tree, causing a linear search to occur instead of a binary search. This could cause the tree traversal to work in linear time (n) instead of logarithmically (logn), significantly reducing the effiency of the search function. 

3) It could be an issue with the algorithm implementation where it appears to work efficiently on small inputs but becomes less efficient with larger ones. For example, if the implementation uses nested loops for comparisons, it can significantly increase the number of operations as the input size grows. This could happen if the loops iterate through the entire tree for each comparison instead of using the binary search tree's structure for finding elements. Similarly, if the recursive search function makes a copy of the entire tree on each recursive call instead of just the relevant subtree, it can waste memory and slow down the search for larger trees by retraversing paths it already been on.