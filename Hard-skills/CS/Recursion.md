# Recursion
  **A recursive function** is a function that calls itself. That sounds pretty crazy - why would we do this? Often, recursion is an alternative to iteration and in many cases it can actually be more elegant, resulting in less code that is more readable. However, it's essential to have what's called a base case in all recursive functions, as well as an understanding of the call stack.

  * Always have a base case
    A base case is a terminating case that ends the recursive calls.
    Without a base case, your recursive function will keep calling itself until you run out of memory (you should get a *RangeError* with the message `Maximum call stack size exceeded`).

  Will be added another copy of function to the stack each time. This process will continue until we reach the base case, after which these functions will start popping off of the stack.   

  `function productOfArray(arr) {`
    `if (arr.length) {`
        `const last = arr.pop();`
        `return last + productOfArray(arr);`
    `}`
    `return 0;`
  `}`