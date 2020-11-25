#  Introduction to Bubble Sort
## Estimated Time
1 hour
## A Short Introduction to the Overall Experiment
[Demo](https://www.youtube.com/embed/1WHzXwp5l7g)

## Prerequisites of the Experiment
This experiment requires you to have basic knowledge about :
  * [The Notion of Sorting](https://en.wikipedia.org/wiki/Sorting_algorithm)
  * [Notion of Time and Space complexity](https://en.wikipedia.org/wiki/Time_complexity)

And above all, a curiosity to learn and explore!
## Overview of the Experiment

  * The aim of this experiment is to understand the Bubble Sort algorithm, its time and space complexity, and how it compares against other sorting algorithms.
  *  The experiment features a series of modules with video lectures, interactive demonstrations, simulations, hands-on practice exercises and quizzes for self analysis.

## Learning Objectives of the Experiment

In this experiment, we will be able to do the following:

   * Given an unsorted array of numbers, generate a sorted array of numbers by applying Bubble Sort.
   * Optimise the Bubble Sort algorithm to achieve better performance.
   * Demonstrate knowledge of time complexity of Bubble Sort by counting the number of operations involved in each iteration.
   * Compare Bubble Sort with other sorting algorithms and realise Bubble Sort as a stable comparison sorting algorithm.

## Experiment Modules and their Weightage
|Module |Weightage | Expectation
|Pre-Test|10%|Solve All Questions
|Bubble Sort|25%|Understand the Bubble Sort algorithm
|Optimized Bubble Sort 	|25%|Understand the optimization technique
|Analysis|25%|Understand the time and space complexity
|Post-test|15%|Solve All Questions

# Bubble Sort Algorithm
## Estimated Time
15 hours
## Demonstration of Bubble Sort Concept
[Demo](https://www.youtube.com/embed/ph-C6sUyzE4)
## Learning Objectives of this Module
In this module, we will :

  *  Gain the intuition for Bubble Sort
  *  Learn when and how to swap incorrectly ordered elements
  *  Learn about the primitive Bubble Sort algorithm
  *  Practice the algorithm
  *  Test your conceptual understanding with a short quiz



## Understanding the Bubble Sort Algorithm
### How can we sort an array?
In Bubble Sort, we take the simplest possible approach to sort an array.

   * We look through the array in an orderly fashion, comparing only adjacent elements at a time.
   * Whenever we see two elements which are out of order (refer to the picture below), we swap them so that the smaller element comes before the greater element.
   * We keep performing the above steps over the array again and again till we get the sorted form.

###  When should we swap?
<center><img src="images/swap.png"  width="600" height="310"> <br></p> </center>

### Important Observations
Let's take note of a few important observations :

   * If we start from the first index and keep comparing the ith and (i+1)th element (where i varies from 1st to the second last index), at the end of one iteration, we see that the greatest element in the entire array has reached the last position.
   * This is because no matter where the greatest element was, it gets swapped repeatedly to reach it's correct position. Refer to the picture below!
   * Similarly, if we do a second iteration, we will end up with the second greatest element in the second last position.

### Step by Step Process for One Iter
<center><img src="images/oneiteration.png"  width="600" height="310"> <br><b>Figure-2:oneiteration</b></p> </center>

## Demonstration of Bubble Sort
### Algorithm of Bubble Sort
Let's have a final look at the consolidated algorithm to sort an array of N elements:

   * STEP 1 : Compare the i^th and (i+1)^th element, where i=first index to i=second last index.
   * STEP 2 : Compare the pair of adjacent elements. If i^th element is greater than the (i+1)^th element, swap them.
   * STEP 3 : Run steps 1 and 2 a total of N-1 times to attain the final sorted array.

### Demonstration of Bubble Sort Algorithm
[Demo](https://www.youtube.com/embed/aFjElrUB0Qw)
### Iteration by Iteration Visualization of Bubble Sort
<center><img src="images/bubble.png"  width="600" height="310"> <br><b>Figure-6:</b></p> </center>
## Observations
From the above observations, we can conclude that after the T^th iteration, we will have the T^th largest element placed at its correct position. If we have N elements in a given array, we would therefore have to run N-1 iterations to place all the elements in their correct place and completely sort the array.

Notice that after N-1 iterations, N-1 elements will be in their correct positions, so the one element left will automatically have no choice but to already be in its correct position as well!

Look at the picture below and work out the result of each iteration. See if it matches the picture, and notice which elements keep getting placed correctly after each iteration! 

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
## Optimization Technique of Bubble Sort
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

### Visualization of Optimized Bubble Sort
<center><img src="images/optimise1.png"  width="600" height="310"> <br><b>Figure3:optimise1.png</b></p> </center>
1
### When to Stop?
<center><img src="images/optimise2.png"  width="600" height="310"> <br><b>Figure-4:optimise2.png</b></p> </center>
### Demonstration of Optimized Bubble Sort Technique with an Example
<video> 
## Demo of Optimized Bubble Sort
## Step by Step Practice of Optimized Bubble Sort
### Practice : Optimized Bubble Sort
## Hands-on Exercise on Optimized Bubble Sort
## Analysis of Bubble Sort
## Estimated Time
15 hours
### Analysis of Bubble Sort
<demo>
### Learning Objectives of this Module
 In this module, we will be learning about :

  *  Time and Space Complexity : We will learn about the running time of one iteration, and then extend it to N iterations to complete the sorting process.
  *  Stable Sort : We will learn about stability of sorting algorithms. Then we will see how Bubble Sort is a Stable Sort.
  *  Comparison with other algorithms : We will compare Bubble Sort with other sorting algorithms and see in which situations Bubble Sort is the optimal/not optimal approach to take.

## Time and Space Complexity of Bubble Sort
### Running Time of Bubble Sort
Lets assume that we are sorting N elements of a given array using SIMPLE Bubble Sort.

   * To complete one iteration, we traverse the array exactly once. Since we perform N-1 comparisons in an iteration, time complexity of completing one iteration is O(N).
   * In regular Bubble Sort, we run N-1 iterations, which is O(N), to sort our array. Hence overall time complexity becomes O(N*N). Note that even if array is fully sorted initially, regular Bubble Sort will take O(N^2) time to complete.

### Best and Worst Cases for Optimized Bubble Sort
For regular Bubble Sort, time complexity will be O(N^2) in all cases. For optimized Bubble Sort :

  *  In best case scenario, we will have an already sorted array. We will have to run one iteration (N-1 comparisons) to determine this. Time complexity will be O(N) in this case.
  *  In worst case (reverse sorted array) we will have to run N iterations to sort our array. Total comparisons performed will be (N-1)+(N-2)+(N-3)....+2+1. Hence overall time complexity becomes O(N^2).

Try out the demo below and look out for the number of comparisons performed for sorted, reverse sorted and randomly generated array using optimized Bubble Sort. Notice how the number of comparisons always remains between O(N) and O(N^2)!

### Time complexity of Optimized Bubble Sort
<<demo>>
### Space Complexity of Bubble Sort
While swapping two elements, we need some extra space to store temporary values. Other than that, the sorting can be done in-place. Hence space complexity is O(1) or constant space.

## Stability of Bubble Sort
### What is a Stable Sort Algorithm?
A sorting algorithm is said to be stable if two objects with equal keys appear in the same order in sorted output as they appeared in the input unsorted array. For example, look at the picture below. The unsorted array has two elements with value 23. Note the order of both these elements in the stable and unstable sorted arrays.
### Stable and Unstable Sort
<center><img src="images/stable.png"  width="600" height="310"> <br><b>Figure-4:optimise5:stable</b></p> </center>
### Is Bubble Sort Stable?
Yes, Bubble Sort is a stable sorting algorithm. We swap elements only when A is less than B. If A is equal to B, we do not swap them, hence relative order between equal elements will be maintained.
Look at the picture below and keep an eye out for the ordering of 23 and 23*. Note how the original order of these elements is retained throughout the sorting process. The relative positioning of 23 and 23* does not change in the sorted output.
### Stability of Bubble Sort
<center><img src="images/stablebubble.png"  width="600" height="310"> <br><b>Figure-6:stablebubble</b></p> </center>
## Comparison with other algorithms
### Graph : Time Complexities of Sorting Algorithms
<center><img src="images/comparison.png"  width="600" height="310"> <br><b>Figure-7:comparison</b></p> </center>
### Comparison with other sorting algorithms
<center><img src="images/comparison-table.png"  width="600" height="310"> <br><b>Figure-8:comparison-tabl</b></p> </center>
