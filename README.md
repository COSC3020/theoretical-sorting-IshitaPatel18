[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/9YUeXH71)
# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.

Since I have access to the black-box implementation of the sorting algorithm, 
to verify the runtime of $O(n)$, I would give the black-box an unsorted data 
set that consists of a relatively small number of elements and then compare it
to a larger set of elements to see if the runtime has increased linearly as $O(n)$ should. 
Repeating these tests would be the most accurate way to verify the claim because 
it is physical evidence that shows the runtime changes linearly as the input grows in size. 
Along with checking for linear results, I would take a data set and try every
permutation of the data set through the black-box. Not only should I see a sorted list
for every single permutation, but it should also be solved in roughly the same time. 
I would do this for multiple data sets of various sizes to see if the runtime
increases linearly as the size of the input data gets larger. My bet would be that
as the data sets get larger and larger, the runtime will not grow linearly, or there
will be permutations that can not be sorted resulting in unsorted lists.
Since this black-box implementation can sort arbitrary elements in $O(n)$ time
by comparing two elements at a time, slide 45 from the sorting powerpoint slides
disagrees with this statement as the slide says, "This is true for any comparison-based
sorting algorithm so the complexity of the sorting problem is $\Omega(n * log(n))$."
This is supported by the decison tree that occurs as two elements from the data set are compared.
As two elements are compared the tree branches into a yes or no situation at every comparison,
which would lead to a tree that contains n! number of leaves and a height of lg(n!).
The worst case of a decision tree is at least lg(n!) and by Stirling's approximation,
lg(n!) is equivalent to n * lg(n). If this researcher disagrees then the only way to 
disprove this would be for a thorough source code analysis, otherwise, $O(n)$ is not possible. 
Therefore, the Computer Science researcher that claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two elements at a time
would not be correct based on the n*log(n) time complexity for any comparison based sorting algorithm. 
