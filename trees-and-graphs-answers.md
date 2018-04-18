#### Exercises

>1. What is a binary tree and what makes it unique to other trees?

`A: A binary tree is a recursive data structure that takes one piece of root data, and branches into left and right for it's child data, and each child branches into two, so on and so forth. `

>2. What is a heuristic?
`A: A heuristic is a guess that an algorithm makes to solve a complex problem sooner by sacrificing accuracy.`

>3. What is another problem besides the shortest-path problem that requires the use of heuristics?
`A: An example of another problem that requires the use of heuristics is earthquake readiness. Seismologists will use data from seismic waves to come up with heuristic predictions on when the next earthquake will hit. An educated guess, in other words.`

>4. What is the difference between a depth-first search and a breadth-first search?
`A: The difference between a depth-first search and a breadth first search is how they go through the grandchildren's data. The depth first search will go through one side completely, then the other. And the breadth first search goes through each row before moving on to the next.`

>5. Explain in your own words what an undirected, a-cyclic, unweighted graph is.
`A: An undirected, a-cyclic, unweighted graph would be a graph in which each node is connected to each other like a two way street, does not form any loops, and has no weighted branches (cost).  `

>6. What kind of graph is a binary search tree?
`A: A binary tree is an undirected, a-cyclic graph. Binary trees can be weighted or unweighted, depending on the data.`


#### Programming Questions
>1. Given a Binary Search Tree and a value, write a function that checks to see whether the value exists within the tree.

```
-Starting at the root value, we will want to check each branch and return true if the data is in the tree.
-Testing the left branch first to see if the root value is less than the node on the left.
-If true, proceed down the left.
-If else, proceed checking down the right side of the tree until the value is found.

BinarySearchTree.prototype.isPresent = function(data) {
  let current = this.root;
  while (current) {
    if (data === current.data) {
      return true;
    }
    if (data < current.data){
      current = current.left;
    } else {
      current = current.right;
    }
  }
  return false;
}

```

>2. Given a Binary Search Tree and two nodes, n1 and n2, write a function that finds the distance between the two nodes.

```
-First we want to add the distance between n1 and the root, plus the distance between n2 and the root to find the shortest path between n1 and n2.

function findDistance(root, n1, n2){
  if (root === null || n1 === n2){
    return 0;
  }
  distance.left = findDistance(root.left, n1, n2);
  distance.right = findDistance(root.right, n1, n2);

  if (distance.left > 0 && distance.right > 0){
    return distance.left + distance.right;
  }
  if (distance.left > 0 && distance.right > 0){
    return distance.left;
  }
  if (distance.right > 0 && root === n1 || n2){
    return distance.right;
  }
  if (distance.left === 0 && distance.right === 0){
    if(root !== n1 || n2){
      return 0;
    }
    if (root == n1 || n2){
      return 1;
    }
    } else {
      return max(distance.left, distance.right) + 1;
    }
}
```
