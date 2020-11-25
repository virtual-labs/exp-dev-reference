#Bubble Sort
## Understanding the Bubble Sort Algorithm
### How can we sort an array?
In Bubble Sort, we take the simplest possible approach to sort an array.

   * We look through the array in an orderly fashion, comparing only adjacent elements at a time.
   * Whenever we see two elements which are out of order (refer to the picture below), we swap them so that the smaller element comes before the greater element.
   * We keep performing the above steps over the array again and again till we get the sorted form.


                     

###  When should we swap?
<center><img src="images/img.png"  width="600" height="310"> <br><b>Figure-6:</b></p> </center>

### Important Observations
Let's take note of a few important observations :

    If we start from the first index and keep comparing the ith and (i+1)th element (where i varies from 1st to the second last index), at the end of one iteration, we see that the greatest element in the entire array has reached the last position.
    This is because no matter where the greatest element was, it gets swapped repeatedly to reach it's correct position. Refer to the picture below!
    Similarly, if we do a second iteration, we will end up with the second greatest element in the second last position.

Step by Step Process for One Iter
<center><img src="images/img.png"  width="600" height="310"> <br><b>Figure-6:</b></p> </center>

## Demonstration of Bubble Sort
### Algorithm of Bubble Sort




Let's have a final look at the consolidated algorithm to sort an array of N elements:

   * STEP 1 : Compare the ith and (i+1)th element, where i=first index to i=second last index.
   * STEP 2 : Compare the pair of adjacent elements. If ith element is greater than the (i+1)th element, swap them.
   * STEP 3 : Run steps 1 and 2 a total of N-1 times to attain the final sorted array.

###Demonstration of Bubble Sort Algorithm
<video>
### Iteration by Iteration Visualization of Bubble Sort
<center><img src="images/img.png"  width="600" height="310"> <br><b>Figure-6:</b></p> </center>
## Bubble Demo
<demo>
## Step by Step Practice of Bubble Sort
<demo>
## Hands-on Exercise on Bubble Sort
### Exercise : Bubble Sort

## Optimized Bubble Sort
### Estimated Time 
15 minutes
### Demonstration of Optimized Bubble Sort Concept 
<video>
###Learning Objectives of this Module


In this module, we will :

   * Observe some characteristics of the algorithm
   * Understand how we can use them to optimise the algorithm
   * Practice the algorithm
   * Test your conceptual understanding with a short quiz
##Optimization Technique of Bubble Sort
### Optimization Technique


Now that we have seen and understood how Bubble Sort works, let's take note of a few observations :

   * As we pointed out before, after the Tth iteration, the Tth largest element is placed correctly (at the Tth index from the end).
   * Given this fact, we can say that if we're on the Tth iteration, the greatest (T-1) elements already occupy their correct places among the last (T-1) indices of the array.
   * Hence, we don't have to compare these elements again and again in subsequent iterations. Instead, in the Tth iteration, we can just compare the first (N-T+1) elements.
   * Since we are reducing the number of redundant comparisons, the running time of the algorithm will be lesser.

###When can we Stop?

   * In many cases, we notice that the array gets sorted much before the N iterations are completed.
   * To avoid redundant iterations, we can check whether or not our array is sorted, after each iteration. We can terminate our algorithm if the array is sorted.
   * How do we check if our array is sorted? Notice that if we run an iteration where no swaps are required, it means that all pairs of adjacent elements are correctly ordered, or in other words, the array is sorted.
   * Hence, whenever we encounter one full iteration without any swaps, we can safely declare the array as sorted.
   * Note that given an already sorted array, we will be able to terminate our algorithm in one iteration itself.

###Visualization of Optimized Bubble Sort
<image>
###When to Stop?
<image>

###Demonstration of Optimized Bubble Sort Technique with an Example
<video> 
## Demo of Optimized Bubble Sort
## Step by Step Practice of Optimized Bubble Sort
### Practice : Optimized Bubble Sort
## Hands-on Exercise on Optimized Bubble Sort



