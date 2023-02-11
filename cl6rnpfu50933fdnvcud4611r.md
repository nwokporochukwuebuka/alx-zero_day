# Recursion In JavaScript

## What is Recursion?

Recursion is the process of something calling itself. A recursive function is a function that calls itself in order to execute a function. The syntax of a recursive function is:

![javascript-recursion.webp](https://cdn.hashnode.com/res/hashnode/image/upload/v1660374339997/9VuqGawF9.webp align="left")

From the diagram above, we can see that the `recurse()` function is called inside itself.

## How a Recursive Function Works

Recursive functions run infinitely and hence need a condition to break out. This condition is usually an if statement. The recursive function runs if the condition is not met, but immediately after that condition is met, the recursive function returns a value and stops running.

## Differences Between Recursion and Iteration

Many developers confuse recursion with iteration. While they perform similar operations (i.e., they are used to repeat processes), they are somewhat different in their syntax.

Recursion uses function calls to make the statements run repeatedly in the body of the function, while iteration uses the for, while, and do while loops to execute statements repeatedly.

Most problems that can be solved using the iteration method can also be solved using recursion.

### Example 1:

In this example, we want to count down from a given number to zero.

**Using iteration, we have**

```bash
function countDown(n){
  for (let i = n; i > 0; i--){
    console.log(i);
  }
  console.log("Hurray");
}

// running our function
countDown(5);
```

**Output:**

```bash
5
4
3
2
1
Hurray
```

**Using recursion, we have:**

```bash
function countDownRecursive(n){
  // first we create our breakout condition 
  if (n < 1){
    return console.log("Hurray");
  }
  console.log(n);
  countDownRecursive(n-1);
}

// running our function
countDownRecursive(5);
```

**Output:**

```bash
5
4
3
2
1
Hurray
```

#### Explanation:

**Iterative function** In the iteration method used, we can see that once the input number has been passed, and the function is run, the variable i is logged out and then decreased until it gets to one and prints "Hurray".

**Recursive Function** In the recursive method, this is what happens

```bash
countDown(5) prints 5 and calls countDown(4)
countDown(4) prints 4 and calls countDown(3)
countDown(3) prints 5 and calls countDown(2)
countDown(2) prints 5 and calls countDown(1)
countDown(1) prints 1 and calls countDown(0) which is less than 0, and hence returns "Hurray".
```

### Example 2:

In this example we want to add number within a certain range, from that number up to one. **Using iteration, we have:**

```bash
function sumRange(n){
  let total = 0;
  for(let i = n; i > 0; i--){
    total += i;
  }
  return total;
}

console.log(sumRange(5));
```

**Output:**

```bash
15
```

**Using recursion, we have:**

```bash
function sumRangeRecursive(n, total = 0){
  if(n <= 0){
    return total;
  }
  return sumRangeRecursive(n-1, total + n);
}

console.log(sumRangeRecursive(5));
```

**Output:**

```bash
15
```

#### Explanation:

**Iterative Function** When the function was ran, first the total variable is initialized and for a range from the given input to one is added and i is decreased until i is less than zero and the total result is returned

**Recursive Function** Two parameters are needed, the starting point of the range and the total parameter set to zero. This is what happens when the function is ran,

```bash
sumRangeRecursive(5, total = 0) calls sumRangeRecursive(4, total = 0 + 5)
sumRangeRecursive(4, total = 5) calls sumRangeRecursive(3, total = 4 + 5)
sumRangeRecursive(3, total = 9) calls sumRangeRecursive(2, total = 9 + 3)
sumRangeRecursive(2, total = 12) calls sumRangeRecursive(1, total = 12 + 2)
sumRangeRecursive(1, total = 14) calls sumRangeRecursive(0, total = 14 + 1)
returns 15
```

Thank you all for reading.

You can follow me on the following platforms:

Twitter 🐦: @[@nwokporo_ebuka](@nwokporo_ebuka)

LinkedIn ⚡: @[@chukwuebuka_nwokporo](@chukwuebuka_nwokporo)

GitHub 🚀: @[@ebukvick](@ebukvick)

Hashnode 📗: @[Nwokporo Chukwuebuka](@codeDaddy)