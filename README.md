# NOPT042- Additional homework assignments

If you need extra points, you can solve the following additional assignments. Each is worth one point. The deadline is end of March; if you want me to grade your solution earlier, email me. There is only one GitHub Classroom repository for all of the assignments. 

There are no tests for the autograder. It is up to you to choose a representation of the instance. Prepare at least one simple satisfiable instance, one unsatisfiable instance, and one reasonably large instance (so that your model runs for at least a few seconds). Describe briefly how to run your model.

If you have any questions, or need help, let me know!

## 1. 3D packing

We have several small boxes (cuboids, i.e. 3D rectangles) given as a list of triples of positive integers (length, width, height). We want to pack them all in a box of the shape of a cube. What is the smallest possible length of the side of such cube?

Each of the small boxes can be placed on any of their sides. Boxes can be placed on top of each other, but:
* the base of the top box must lie completely on another box,
* a box can only be placed on top of a box that is at least as heavy, assuming uniform density.

## 2. Minimum common substring partition

We are given two strings. We want to partition the strings into substrings so that each string can be obtained from the other by rearranging its parts (if this is possible). The goal is to find a partition into the smallest number of parts.

For example, if `s1 = GAGACTA` and `s2 = AACTGAG`, then the optimal partition has size 3: `s1 = GAG|ACT|A`, `s2 = A|ACT|GAG` (the instance is taken from [this paper](https://arxiv.org/pdf/2110.05168.pdf)).

## 3. DNA double digest

Using enzyme A, a DNA sequence is cut at certain points into a number of fragments. Using enzyme B, it is cut at possibly (but not neccessarily!) different points and into a possibly different number of pieces. We know the lengths of the fragments when using enzyme A, enzyme B, and both the enzymes at once. Find a permutation of the fragments using enzyme A, and a permutation of the fragments using enzyme B, that fits with the fragments using both enzymes. 

See [this presentation](https://ksvi.mff.cuni.cz/~mraz/bioinf/Present/KubonMartisek16.pdf) for more details and the following sample instance:

```
A = {375, 282, 2205, 746, 2352, 9040}
B = {3518, 1887, 389, 5916, 2017, 1273}
AB = {375, 282, 2205, 656, 90, 1797, 389, 166, 5750, 2017, 1273}
```
for which a possible solution is `([3, 0, 1, 5, 2, 4], [1, 4, 3, 0, 2, 5])`.


## 4. Tower of Hanoi

Solve the Tower of Hanoi puzzle for an arbitrary number of pegs and discs. Use the `planner` module. This is Exercise 6.9/7 in [the book](http://picat-lang.org/picatbook2015/constraint_solving_and_planning_with_picat.pdf).
