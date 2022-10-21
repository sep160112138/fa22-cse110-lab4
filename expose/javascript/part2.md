1. It would print `3`, which is the length of `prices` because the for loop declared variable `i` using '`var`' (so line 12 is within the scope and can access the value of `i`) and when `i == prices.length`, the for loop was exited and the value stored in `i` was `prices.length == 3`.
2. It would print `150`. The value stored in `discountedPrices` is the value it last stored during the last iteration in the for loop, which is `prices[2]*(1-0.5)`, and the result is `300*0.5 == 150`.
3. It would print `150` - the value last stored during the last iteration of the for loop, which is `(discounted price * 100) / 100`, and the result is `(150 * 100) /100 == 150`.
4. The function returns an array of discounted prices calculated from `prices` and `discount`, `discountedPrices[i] == 0.5 * prices[i]`.
5. There will be an error because the `let` declares `i` in the scope of the for loop, but line 12 is outside of the scope and can't access `i`.
6. Likewise, `discountedPrice` is declared with the scope inside the for loop, but line 13 is outside of the scope so it can't access `discountedPrice`. So there will be an error.
7. Because the `finalPrice` variable is declared in the same scope as line 14, line 14 can access the value of `finalPrice` and it'll output the last iteration in the for loop, which is same as question 2 - `150`. 
8. The function will, again, return an array same as the one in question 4 because `discountedPrices` was declared in the scope of the function.
9. Variable `i` in this question is declared the same way as question 5, so similarly, line 11 produces an error for the same reason it's out of scope and not in the for loop.
10. The variable `length` is declared as a constant and was only assigned once and never reassigned. So there's no error with that variable and line 12 prints the length of `prices` which is 3.
11. Throughout the entire function, `discounted` was never reassigned, but instead modified internally by pushing values into it. Because there's no reassignment, there's no error, and the function returns the same values as it did in questions 4 and 8.
12. 
> a. `student.name`<br>
  b. `student['Grad Year']`<br>
  c. `student.greeting()`<br>
  d. `student['Favorite Teacher'].name`<br>
  e. `student.courseLoad[0]`<br>
13.
> a. Output is `'32'` since integer 2 maps to its string representation<br>
  b. Output is `1` since the minus sign is a mathematical expression and the string `'3'` is automatically converted into a number `3`.<br>
  c. Output is `3` since plus sign number `3` and plus sign makes the `null` automatically convert to `0`<br>
  d. Output is `'3null'` since `'3'` suggests an automatic conversion of `null` into `"null"`, and the strings are appended.<br>
  e. Output is `4` since number `3` and plus sign automatically converted `true` to `1`.<br>
  f. Output is `0` since the plus sign automatically converts `false` to `0` and `null` to `0`.<br>
  g. Output is `'3undefined'` since `'3'` is a string so it converts `undefined` to `'undefined`' and appends it.<br>
  h. Output is `NaN` since the minus sign is a mathematical expression and string `'3'` is converted into number `3`. And in math 3-undefined is undefined so the output is undefined as a number, so `NaN`.<br>
14.
> a. `True`, `'2'` gets converted to number `2` and `2 > 1` is true.<br>
  b. `False`, both are strings and are compared a character at a time. The first character of `'12'` is `'1'` and it's less than `'2'` lexicographically.<br>
  c. `True`, `'2'` gets converted to number `2` and `2 == 2` is true.<br>
  d. `False`, `===` disallows type conversion so `'2'` is a different type than `2`.<br>
  e. `False`, `true` is converted to `1` and `1 == 2` is false.<br>
  f. `True`, since `2` isn't empty nor `0`, then `Boolean(2)` is true, and `true === true` is true.<br>
15. They both check if both sides of the operator are equal, but `==` allows type conversion and `===` doesn't.
16. See part2-question16.js file
17. The result would be an array `[2,4,6]`. `modifyArray` creates a new array and pushes all elements of `[1,2,3]` into it using a for loop. In the process of that, each element is processed in callback(), which is inputted as doSomething(), which multiplies the inputted number by 2. So each number pushed into `newArr` is double the number of the original array.
18. See part2-question18.js file
19. The output is `1 4 3 2`. Because `1` and `4` are outputted immediately since there's no timeout and are outputted in order. But for `3`, although the delay is set to 0, there's a approximately 4 ms delay due to the browser minimum delay. `2` has a longer delay so it's outputted last.
