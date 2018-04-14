#### Exercises

>1. What is the main difference between a stack and a queue?
`A: The main difference between a stack and a queue is the order of priority. LIFO as compared to FIFO. For instance, in LIFO the same end is used to insert and delete elements. Whereas in FIFO, only one end is used for insertion (rear) and another is used for the deletion of elements (front end).`

>2. What are the similarities between stacks and queues?
`A: Data Structures are similar in that they both have in/out priorities for completion.`

>3. Imagine you are an engineer tasked with implementing the UNDO and REDO options in a word processor such as Microsoft Word. Which data structure would you use for each option and why?
`A: UNDO: LIFO: LIFO would be used to place the last change back onto the top of the stack.`
`A: REDO: FIFO: FIFO Would be used to add a change back into the queue of completed changes.`

####Programming Questions

>1. Given a string, reverse it using a stack. For example, the string "Bloc!" should be converted to "!cloB".
`A: For this function, I would:
1) Create an empty string.
2) One by one push all characters of string to stack.
3) One by one push all characters from stack and put them back to string.`
```
function reverseString(string){
  var newString = [];
  for(var i =0; i <= string.length; i++) {
    newString.push(string.charAt(string.length - i));
  }
  return newString.join('');
}

console.log(reverseString("Bloc!"));
```

>2. Implement the delete functionality of a stack using one queue. Make a FIFO data structure mirror the functionality of a LIFO data structure.
`A: CLASS stack with item constructor
FUNCTION
INPUT queue array
INPUT deleteItem method THEN FOR iteration through items in queue
END FOR
THEN push queue items index
POP queue
RETURN queue
END FUNCTION
LET stack equal to new Stack with empty constructor.
CALL stack on deleteItem method and input empty array
END CLASS`
```
class Stack {
  constructor(item){
  this.queue = ["1", "2", "3"];
}
deleteItem(item){
  for(var i = 0; i > this.queue.length; i++){
    this.queue.push(item[i]);
}
this.queue.pop();
return this.queue;
}
}
let stack = new Stack();

stack.deleteItem([]);
```

>3. Fill in the methods for the following Queue class so that it will work as expected.

`A:
CLASS QUEUE
 FUNCTION enqueue(element)
 THEN push items(element)
 END FUNCTION

 FUNCTION dequeue
THEN shift items()
 END FUNCTION
END CLASS
`
