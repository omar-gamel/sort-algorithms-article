# Categories of sorting algorithms

Sorting algorithms are categorized into: <br>
<br>
1. <b>Internal sorting algorithms:</b> These are sorting algorithms applied to a small amount of data. Only the main memory is used. Examples would be bubble sort, insertion sort, and quicksort.

2. <b>External sorting algorithms:</b> These are sorting algorithms that can be applied to massive amounts of data. As a result, external storage devices such as hard drives, and flash disks are used. An example would be merge sort.

# Efficiency of sorting algorithms

Some sorting algorithms are more efficient than others. The effectiveness of a sorting algorithm is usually defined by the following performance measures:<br>
<br>

- <b>Time complexity:</b> This is the amount of time required by the computer to perform the sorting based on an algorithm.

- <b>Memory complexity:</b> It is the amount of computer memory required by the computer to perform the sorting based on an algorithm.

Based on the factors above, an algorithm has four performance cases:

1. <b>Worst case time complexity:</b> It is a function defined as a result of a maximum number of steps taken on any instance of size n. It is usually expressed in Big O notation.

2. <b>Average case time complexity:</b> It is a function defined as a result of the average number of steps taken on any instance of size n. It is usually expressed in Big theta notation.

3. <b>Best case time complexity:</b> It is a function defined as a result of the minimum number of steps taken on any instance of size n. It is usually expressed in Big omega notation.

4. <b>Space complexity:</b> It is a function defined as a result of additional memory space needed to carry out the algorithm. It is usually expressed in Big O notation.

# Strategies applied during sorting

- <b>Recursion:</b> Recursion is a programming method where you define a function in terms of itself. The function generally calls itself with slightly modified parameters (in order to converge).

- <b>Divide and conquer:</b> The algorithm accomplishes its task by dividing the problem into smaller subproblems and solving them to come up with the overall solution.

# Sorting algorithms
For each sorting algorithm discussed below, there is a step-by-step explanation of how the algorithm works, image representation, and implementation of the algorithm using JavaScript.

# Bubble sort
Bubble sort follows the recursion technique.<br>
<br>
<b>Step-by-step guide:</b>

- Start by comparing the first two elements in an array.

- Swap them if required.

- Continue till the end of the array. At this point, you have made a series of inner passes and completed an outer pass.

- Repeat the process until the entire array is sorted.

<b> JavaScript implementation </b>

<p>

```javascript

function bubbleSort(arr){

    //Outer pass
    for(let i = 0; i < arr.length; i++){

        //Inner pass
        for(let j = 0; j < arr.length - i - 1; j++){

            //Value comparison using ascending order

            if(arr[j + 1] < arr[j]){

                //Swapping
                [arr[j + 1],arr[j]] = [arr[j],arr[j + 1]]
            }
        }
    };
    return arr;
};

console.log(bubbleSort([5,3,8,4,6]));
```
</p>

Output:

<p>

```javascript

[ 3, 4, 5, 6, 8 ]

```
</p>

Bubble sort has the following performance cases:

- Worst-case time complexity: Big O (n^2).

- Average-case time complexity: Big theta (n^2).

- Best-case time complexity: Big omega (n).

- Space complexity: Big O (1).

# Insertion sort
