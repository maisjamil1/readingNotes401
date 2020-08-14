## Big O :
describes the worst-case scenario, and can be used to describe the execution time required or the space used by an algorithm.

 

## O(1):
describes an algorithm that will always execute in the same time (or space) regardless of the size of the input data set.

 

## O(N):
describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set.

 

## Logarithms:

Binary search:is a technique used to search sorted data sets. It works by selecting the middle element of the data set, essentially the median, and compares it against a target value. If the values match it will return success. If the target value is higher than the value of the probe element it will take the upper half of the data set and perform the same operation against it. Likewise, if the target value is lower than the value of the probe element it will perform the operation against the lower half.

![img](https://www.geeksforgeeks.org/wp-content/uploads/Binary-Search.png)


This type of algorithm is described as O(log N).its extremely efficient when dealing with large data sets,Doubling the size of the input data set has little effect on its growth as after a single iteration of the algorithm the data set will be halved and therefore on a par with an input data set half the size.

