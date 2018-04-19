#### Exercises
> 1. What are some pros and cons of using linked lists instead of arrays?
```
Pros: A pro of a linked list would be the extra space you have for each list as it is it's own list, instead of a giant array of items.
Cons: Because each list is linked to the next, it could take longer to reach the desired list, because you have to go through each list linearly.
```

> 2. Come up with a real world example of a linked list.
```
A: An example of a linked list would be a scavenger hunt. In order to proceed to the next clue and get to your destination, you need to get to each clue, in a linear way. Each clue leading you to the next, and the next, until the final item has been reached.
```

#### Programming Questions

>1. The Linked List push function should take a value, create a node, and add it to the end of a list. Below is a push function for a singly linked list. However, there is something wrong with it. Find the bug and fix the code.

```
LinkedList.prototype.push = function(element) {
     var node = new Node(element);
     currentNode = this.head;

     if (!currentNode){
       this.head = node;
     } else {
       currentNode.next = currentNode;
     }
     currentNode.next = node;
};
```

>2. Given an unsorted singly linked list, remove all duplicates from the linked list.
Example
Input: a -> c -> d -> d -> a
Output: a -> c -> d
```
function LinkedList() {
  this.head = null;
}

LinkedList.prototype.removeDuplicates = function(){
  if (!this.head || !this.head.next){
    console.log('No duplicates were found. Empty or a single element Linked List.');
    return;
  }

  var n1;
  var n2;
  var n3;
  var value;
  n2 = this.head;

  while(n2) {
    val = n2.data;
    n1 = n2;
    n3 = n1.next;

    while(n3){
      if (n3.data === value){
        n1.next = n3.next;
      } else {
        n1 = n3;
      }
      n3 = n3.next;
    }
    n2 = n2.next;
  }
};
```
>3.
```
LinkedList.prototype.reverse = function(){
  currentNode = this.head;
  nextNode = currentNode.next;

while(nextNode) {
  var temporary = nextNode.next;
  nextNode.next = currentNode;
  currentNode = nextNode;
  nextNode = temporary;
}

this.head.next = null;
this.head = currentNode;
};
```
