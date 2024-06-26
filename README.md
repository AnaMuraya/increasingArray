# increasingArray question
You are given an array of integers. On each move you are allowed to increase exactly one of its element by one. Find the minimal number of moves required to obtain a strictly increasing sequence from the input.

Example

For inputArray = [1, 1, 1], the output should be
solution(inputArray) = 3.


## solution explanation
The function takes an array as its parameter and returns the minimum number of moves needed to make all elements in the array strictly increasing.

It starts by initializing the moves variable to zero. It then loops through each element of the array, starting at index 1 (since we're comparing each element to the one before it).

For each element i, the function checks if it is less than or equal to the previous element i-1. If it is, then we need to move this element up so that it is strictly greater than the previous element. To do this, the function adds inputArray[i-1] - inputArray[i] + 1 to moves (this represents the number of moves needed to increase inputArray[i] to inputArray[i-1]+1). It then sets inputArray[i] to inputArray[i-1] + 1.

After the loop completes, the function returns the final value of moves.