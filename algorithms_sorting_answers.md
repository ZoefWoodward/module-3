#### Exercises
>1. Write pseudocode for bubble sort.
```
function bubbleSort(collection)
  REPEAT
    SET swapped to false;
    FOR i = first index of collection to last index of collection -1
      IF collection[index] > collection[index + 1] THEN
      SET temporary to collection[index]
      SET collection[index] to collection[index + 1]
      SET collection[index + 1] to temporary
      SET swapped to true;
    END IF
  END FOR
UNTIL swapped is false

```
>2. Write pseudocode for quicksort.
```
FUNCTION quickSort(collection)
    SET left to 0
    SET right to collection - 1
    IF left < right THEN
        SET pivot to right
        SET partitionIndex to partition WITH collection, pivot, left, right
        CALL quickSort WITH collection, left, partitionIndex - 1;
        CALL quickSort WITH collection, partitionIndex + 1, right;
    ELSE
        RETURN collection
    END IF
END function

FUNCTION partition(collection, pivot, left, right)
    SET pivotValue to collection[pivot]
    SET partitionIndex to left
    FOR i = left to right of collection
        IF collection[i] < pivotValue THEN
        CALL swap WITH collection, i, partitionIndex
        END IF
    END FOR
    CALL swap WITH collection, right, partitionIndex
    RETURN partitionIndex
END function

FUNCTION swap(collection, i, j)
    SET temporary to collection[i]
    SET collection[i] to collection[j]
    SET collection[j] to temporary
END function

```
>3. We talked about time complexity in a previous checkpoint, and how to get an idea of the efficiency of an algorithm. After looking at the pseudocode for the above sorting methods, identify why merge sort and quick sort are much more efficient than the others. Walking through each algorithm with a few sample collections may help.
`A:  Quick sort and Merge sort have a time complexity of 0(n log n).
Quick sort is efficient because it uses less memory than other sorting methods and can handle larger inputs better than other options.
Merge sort is efficient because it has less comparisons than other sorting methods, which compare items one at a time.`

>4. All of the sorts addressed in this checkpoint are known as comparison sorts. Research bucket sort and explain how it works. What is the ideal input for bucket sort?
`A: Bucket sort works by starting with an unsorted array, setting up an array of empty buckets, scatter the elements into buckets according to their range, sort the elements within the buckets, and then gathering the sorted elements from all buckets into the original array.`
