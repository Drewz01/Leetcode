PALINDROME NUMBER

Thought Process
Understand what a palindrome means:

 A number is a palindrome if it reads the same forward and backward (e.g., 121 → 121, but -121 → 121-, so not a palindrome).


Rule out obvious non-palindromes:


Any negative number is automatically not a palindrome.


Any number that ends with 0 but isn’t 0 itself (e.g., 10) can’t be a palindrome because it would start with 0 when reversed.


Avoid converting to a string (follow-up requirement):

 Instead of comparing characters in a string, try to solve it mathematically.


Reverse only half of the number:


If you reverse the whole number, you risk integer overflow.


Instead, repeatedly take the last digit (x % 10) and build a reversed half.


Stop when the reversed half becomes greater than or equal to the remaining part (x).


Compare the two halves:


If the number has an even number of digits, then x == reversedHalf.


If the number has an odd number of digits, the middle digit doesn’t matter, so compare x == reversedHalf / 10.


