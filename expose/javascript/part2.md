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
