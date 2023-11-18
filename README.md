# ROTATION-OF-ARRAYS

N is the length of the input array A.
if statement checks if the array is empty (N === 0) or if no rotation is needed (K === 0). If either condition is true, the original array is returned as no rotation is necessary.

const rotatedArray = [];This creates an empty array to store the elements after rotation.

The for loop iterates through each element of the original array.

The line const index = (i + K) % N; calculates the new index for the current element after rotation and operator (%) is used to ensure that the new index remains within the bounds of the array.
For example, if N is 5 (array length), and i + K is 7, then (i + K) % N will be 2, effectively wrapping around the array.

THAT IS :- i + K: The variable i represents the current index of the element in the original array. K is the number of positions to rotate the array to the right

rotatedArray[index] = A[i]; assigns the current element to its new position in the rotated array.


//#THE BINARY GAP EXPLANATION//
 The concepts of currentGap and maxGap to the examples:

currentGap:

currentGap represents the length of the current sequence of consecutive 0 bits encountered while iterating through the binary representation.
It gets incremented for each consecutive 0 encountered until a 1 is found in the binary representation.
maxGap:

maxGap represents the maximum length of binary gaps encountered so far while iterating through the binary representation.
It gets updated whenever a longer sequence of consecutive 0 bits is found.
Let's use the example of the binary representation 1000010001 (decimal number 529) to illustrate:

Starting with currentGap and maxGap both set to 0.

let currentGap = 0;
    let maxGap = 0;

Iterate through the binary representation:

Encounter 1, reset currentGap to 0.
Encounter 0, increment currentGap to 1.
Encounter more 0s, increment currentGap to 4.
Encounter 1, update maxGap to 4 (the longest sequence so far) and reset currentGap to 0.
Encounter more 0s, increment currentGap to 3.
... continue until the end.
In this example, the longest binary gap is of length 4, and maxGap will hold this value after the iteration is complete. currentGap keeps track of the current sequence length, and maxGap is updated whenever a longer sequence is found. After the iteration, maxGap holds the length of the longest binary gap.

#THE 529=10000010001 EXPLAINATION

Divide by 2:

Start with the decimal number 529.
Divide 529 by 2. The quotient is 264, and the remainder is 1.
The remainder (1) is the rightmost bit in our binary representation.
Divide the Quotient:

Now, divide the quotient (264) by 2. The new quotient is 132, and the remainder is 0.
Append the remainder (0) to the left of the previous remainder.
Repeat the Process:

Repeat the process by dividing the new quotient (132) by 2. The new quotient is 66, and the remainder is 0.
Append the remainder (0) to the left of the previous remainders.
More Divisions:

Continue the process with divisions: 66 ÷ 2 (quotient: 33, remainder: 0), 33 ÷ 2 (quotient: 16, remainder: 1), 16 ÷ 2 (quotient: 8, remainder: 0), 8 ÷ 2 (quotient: 4, remainder: 0), 4 ÷ 2 (quotient: 2, remainder: 0), 2 ÷ 2 (quotient: 1, remainder: 0), and 1 ÷ 2 (quotient: 0, remainder: 1).
Final Division:

The binary representation is obtained by reading the remainders from bottom to top: 1000010001.

example two

9 is 1001
Divide by 2:

Start with the decimal number 9.
Divide 9 by 2. The quotient is 4, and the remainder is 1.
The remainder (1) is the rightmost bit in our binary representation.
Divide the Quotient:

Now, divide the quotient (4) by 2. The new quotient is 2, and the remainder is 0.
Append the remainder (0) to the left of the previous remainder.
Repeat the Process:

Repeat the process by dividing the new quotient (2) by 2. The new quotient is 1, and the remainder is 0.
Append the remainder (0) to the left of the previous remainders.
Final Division:

Finally, divide the last quotient (1) by 2. The new quotient is 0, and the remainder is 1.
Append the remainder (1) to the left of the previous remainders.
Putting it all together, we get the binary representation 1001. The rightmost bit corresponds to the last remainder obtained in the division process, and the leftmost bit corresponds to the first remainder. Therefore, the binary representation of the decimal number 9 is 1001.

