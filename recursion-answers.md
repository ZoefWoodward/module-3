#### Exercises

>1. Define and compare recursion and iteration.
`A: Recursion is more like a function that will call itself. Like a mirror calling to a mirror until it reaches its destination. Whereas an iteration, will loop through each item, repeating the desired process.`

>2. Name five algorithms that are commonly implemented with recursion.
```
1. The Binary Tree
2. Merge Sort
3. Quick Sort
4. Factorial
5. Fibonacci Sequence
```

>3. When should you use recursion, and when should you avoid recursion?
`A: A good time to use recursion would be when it is too complex to use iterative code. Recursive functions are used for it's simplicity. For instance, to recurse on a solved problem: do nothing, you're done.`

>4. Compare the recursive and iterative solutions to the three algorithms from the checkpoint (Factorial, Maximum, and Fibonacci). What is similar and what is different?
`A: They are similar in that all three compare to another number to get their result, and they are all different in their methods of getting the result.`

>5. Given a multi-dimensional collection (such as an array) where the number of dimensions is unknown, write a recursive algorithm to count the number of items in the entire collection.
```
var addNumber = function(array, count) {


  if (count < array.length) {
    return array[count] + addNumber(array, count + 1);
  } else {
    return 0;
  }

};

  var sum = 0;
  var count = 0;


sum = sum + addNumber([1, 2, 3, 5, 6, 7], count);

sum;
```

>6. A palindrome is a word or phrase whose spelling is the same either direction (e.g., racecar). Write a recursive algorithm to determine if a given word or phrase is a palindrome.
```
var isPalindrome = function(string){
  var stringLength = string.length;
  if (stringLength === 0 || stringLength === 1) {
    return true;
  }
  if (string[0] === string[stringLength -1]) {
    return isPalindrome(string.slice(1, stringLength -1) );
  }
  return false;
};

isPalindrome("racecar");
```

>7. Laura and Xander are going door-to-door around their block looking for their lost cat. Write a recursive algorithm showing one way they can visit every house on their block exactly once.
```
var visitNumber = function(x, y) {
  if (x > 0) {
    return;
  }
  if (y === undefined) {
    y = 0;
  } else if (y > 9) {
    return visitNumber(x + 1);
  }
  console.log(x, y);
  visitNumber(x, y + 1);
};
visitNumber(0);
```
