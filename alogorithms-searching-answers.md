####Exercises

>1. What is a real-life scenario that uses linear search?
`A: A real world example of a linear search is looking through your phone for a name. If looking for someone with last name W, you'd go to W, then look at each name until you find the name with the correct last name.`

>2. What is a real-life scenario that uses binary search?
`A: A real life example of a binary search would be walking down between two isles in a library. You have to find which isle is less than or greater than the number you are looking for, then once you find that the number is on left or right, you would turn towards those shelves, then you would have to divide that side to find the isle number, etc.`

>3. Given the alphabetically sorted collection in this checkpoint, how many iterations would it take to find the value G using linear search?
`A: It would take seven iterations to find the value G per the example in this checkpoint.`

>4. Given the alphabetically sorted collection in this checkpoint, how many iterations would it take to find the value G using binary search?
`A: The binary search would iterate three times per the example in this checkpoint.`

>5. Given an unsorted collection of a million items, which algorithm would you choose between linear search and binary search? Explain your reasoning.
`A: Linear search would be the best algorithm for this problem, because binary searches cannot sort unsorted collections.`

>6. Given a sorted collection of a million items, which algorithm would you choose between linear search and binary search? Explain your reasoning.
`A: For a sorted collection, the binary search would be the best solution because it can divide and conquer, cutting the processing time in half.`

####Programming Assignments

>1. You and a friend have set a wager to see who can find the word "Albatross" in the dictionary the fastest. Write a program to allow you to win the bet.
function dictionarySearch(collection, word){
  var first = collection[0];
  var last = collection.length -1;
  ```
  while (first <= last) {
    var mid = (first + last) / 2;
    if(collection[mid] > word) { first = mid -1;
  }
  else if (collection[mid] < word){
    first = mid + 1;
  }
  else {
    return mid;
  }
  }
  return "Sorry, that word was not found.";
}
```
>2. You work at a pet store, and a child has asked you to net the only white-spotted goldfish from the fish tank. Write a program that will help you net the right fish.
```
function findFish(collection, targetFish){
  for(var i = 0; i < collection.length; i++){
    if (collection[i] === targetFish){
      return "You've found the fish!";
    }
  }
  return "That fish isn't in this tank.";
}
```
