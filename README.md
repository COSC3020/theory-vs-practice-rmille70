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

Question 1
1) Asymtotic analysis considers contant factors as negligable, but depending on the input size it can make a considerable actual performance and memory consumption.
2) Asymtotic analaysis doesn't consider the specific hardware specifications of the machine the program in running on, which is usually different machine to machine.
3) Asymtotic analaysis focuses on the big picture, so even though for larger datasets the asymtotic complexity of one program may be better than another, if we only want to use smaller inputs sizes the asymtotic complexity can be misleading. 

Question 2

The asymtotic complexity of a binary search is O(log(n)), thus if $\frac{5}{3} log(1000) = 5$, I would say the run time for n = 10000 would be around $\frac{5}{3} log(10000) \approx 6.666$


Question 3

This could be a hardware problem, where certain aspects of the the machine's hardware made it process the list slower. It could also be that the search algorithm has to perform complex checks on node specific details, which could slow down the search if each node needs alot of details checked. It could also be an issue with the algorithm implementation where it appears to work efficiently on small inputs but when scaled to larger inputs it isn't as efficient. This can happen because of issues with loops, recursion, or how input are stored. 
