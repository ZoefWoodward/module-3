#### Exercises

>1. What is time complexity and what is its relation to algorithms?
`A: Time complexity is the measurement of how long it will take an algorithm (program) to execute. `

>2. What is runtime?
`A: Runtime is the physical time duration of an algorithm.`

>3. How is the runtime of an algorithm calculated?
`A: The runtime of an algorithm is often used synonymously with time complexity, but is calculated by adding up how many instructions the algorithm will execute as a function of the size of its input, then simplifying the expression to the largest term and dropping any constants. The x axis will represent the input size, and the y axis represents the runtime in a graph.`

>4. Name the six types of algorithm growth rates we saw in this checkpoint and list them in order of most efficient to least efficient. Now Google another algorithmic growth rate not covered and place it in the correct spot in your list.
`A: From most efficient to least efficient:
O(1) : Constant Growth Rate

O(log n) : Logarithmic Growth Rate

O(n) : Linear Growth Rate

O(n log n) : Log-Linear Growth Rate

O(n^2) : Quadratic Growth Rate

"O(nk) : Polynomial Growth Rate" (Added)

O(2^n) : Exponential Growth Rate
`
>5. Choose one of the algorithmic growth rates from the last question and make a comparison to a real-life situation.
`A: Bacteria Grown in a lab is an excellent example of the Exponential Growth Rate. Bacteria reproduce by binary fission (splitting in half), and the time between divisions is about an hour for many species. Each split Bacteria, will then go through another binary fission, and so on, exponentially.`

>6. Determine the time complexity of the following snippet of code. It is commonly known as a linear search.
FUNCTION linearSearch(array, target)
 FOR each number in the array
   IF number = target THEN
     RETURN true
   END IF
 END FOR
 RETURN false
END FUNCTION

`A: The time complexity of function linearSearch is O(n)`

>7.Determine the time complexity of the following snippet of code.
FUNCTION foo(array)
 FOR each number in the array
   FOR each number in the array
     print "Hello"
   END FOR
 END FOR
END FUNCTION

`A: The time complexity of the function foo is O(n^2)`

>8. Determine the time complexity of the following snippet of code. It is commonly known as the Fibonacci sequence.
FUNCTION fibonacci(number)
 IF number < 1 THEN
   ERROR
 ELSE IF number = 1 or 2 THEN
   RETURN 1
 ELSE
   CALL fibonacci WITH number - 2 RETURNING twoBack
   CALL fibonacci WITH number - 1 RETURNING oneBack
   RETURN twoBack + oneBack
 END IF
END FUNCTION

`A: The time complexity of function fibonacci is O(2^n)`

>9. Out of the code snippets you just saw, which is the most time efficient?
`A: The time complexity function linearSearch "O(n)" is the most efficient.`
