# Finds the kth largest number among a set of N numbers
A C++ program that finds the kth largest number among a set of N numbers. It implements the solution using two different algorithms and measure the time elapsed during the execution of these
algorithms. As input, the program will take the type of algorithm to be applied (1 or 2), k (a number less than or equal to N). Then it will take N followed by
a list of N numbers. All these input values obtained from an input file. As output, it prints out the kth largest number and the total elapsed time for the completion
of the algorithm.
### The Design 
![image](https://user-images.githubusercontent.com/31419720/54096867-b6216580-43be-11e9-9d66-4b5ee5115068.png)
* Algorithm 1 (AlgorithmSortAll):
  * Store all the numbers in an array;
  * Sort the array in decreasing order, e.g., using insertion sort;
  * return the number at index k-1 in the array.
* Algorithm 2 (AlgorithmSortK):
  * Store only the first k numbers in an array;
  * Sort the array in decreasing order, e.g., using insertion sort;
  * Read the rest of the numbers one by one;
  * Ignore if it is smaller than the number at kth position in the array
  * Otherwise; insert it in its correct position in the array and shift the
remaining numbers (the number at the kth position will be thrown
out of the array)
  * Return the number at index k-1 in the array
#### Input
<br>The program basically takes N +3 numbers as input; first, the algorithm type, second, k,
third, N, and then a total of N numbers. The program will consume all the inputs from a
text file, which contains all the parameters and numbers, each separated by a new line.
For example, the contents of the data.txt file could be like the following:
* 1
* 3
* 5
* 234
* 321
* 324
* 23
* 43
</br>For this example input file, the algorithm type will be 1 (AlgorithmSortAll). The
program should find the 3rd largest element among a list of 5 numbers. These numbers
are 234, 321, 324, 23, and 43.</br>
### Test File Creator
(testInputGenerator.cpp) You can run this
program on the console/terminal with the following format:</br>
testInputGenerator.exe algorithm_type k N number_range > data.txt</br>
Hereby, you need to provide concrete values for the command parameters as
highlighted with bold fonts. For instance, if you run the program as follows, then you
will find the data.txt file in the same directory, which includes 1, 3, 5, in the first three
lines, followed by 5 numbers that are randomly selected between 0 and 400.</br>
testInputGenerator.exe 1 3 5 400 > data.txt
