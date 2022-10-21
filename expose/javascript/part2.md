1. It would print `3`, which is the length of `prices` because the for loop declared variable `i` using '`var`' (so line 12 is within the scope and can access the value of `i`) and when `i == prices.length`, the for loop was exited and the value stored in `i` was `prices.length == 3`.
2. It would print `150`. The value stored in `discountedPrices` is the value it last stored during the last iteration in the for loop, which is `prices[2]*(1-0.5)`, and the result is `300*0.5 == 150`.
3. It would print `150` - the value last stored during the last iteration of the for loop, which is `(discounted price * 100) / 100`, and the result is `(150 * 100) /100 == 150`.
4. The function returns an array of discounted prices calculated from `prices` and `discount`, `discountedPrices[i] == 0.5 * prices[i]`.
5. There will be an error because the `let` declares `i` in the scope of the for loop, but line 12 is outside of the scope and can't access `i`.
6. Likewise, `discountedPrice` is declared with the scope inside the for loop, but line 13 is outside of the scope so it can't access `discountedPrice`. So there will be an error.
7. Because the `finalPrice` variable is declared in the same scope as line 14, line 14 can access the value of `finalPrice` and it'll output the last iteration in the for loop, which is same as question 2 - `150`. 
