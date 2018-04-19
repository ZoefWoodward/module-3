#### Exercises

>1. Using proper pseudo-code, describe the following algorithms:
>Making Tea

```
CASE
SET mug to this.mug;
SET water to this.water;
SET kettle to this.kettle;
SET honey to this.honey;
SET teabag to this.teabag;
ENDCASE

FUNCTION
FOR water in kettle, INCREMENT water until this.kettle equals 1 cup THEN
IF water in kettle is equal to 1 cup, SET kettle to on equals true, THEN
  WHILE true INCREMENT boiling temp UNTIL <= boiling temp of 200 degrees F.
  END WHILE
  END IF
  END FOR
  IF water in kettle is boiled add tea bag to mug.
  END IF
  IF mug is equal to water plus teabag, add 1 teaspoon of honey.
    IF water + teabag + honey + mug equals true, INCREMENT counter for 5 minutes.
    END WHILE
  END IF
  IF 5 minutes equals true, subtract teabag from mug.
  END IF
  END FUNCTION
```

>Washing Dishes
```
SET dishes to this.Dishes
SET soap to this.soap
SET water to this.water
SET sink to this.sink

CASE
Dishes in sink : Dirty RETURN true;
Dishes in sink : Clean RETURN null;
ENDCASE

FUNCTION
IF true, add soap to water in sink.
END IF
ELSE IF Dishes in the sink equals null,
PRINT "There are no dishes in the sink to clean"
END ELSE IF
ELSE IF dishes are clean equals true,
PRINT ("You've cleaned all of your dishes!")
END ELSE IF
END FUNCTION
```

>A Watering my plants.
```
FUNCTION
SET plants to array of plants
SET water to this.water
SET dryness to array of plants - 1 cup of water
return true if dryness is equal to array of plants

FOR each plant, loop through to check if dryness is equal to true.
IF true, loop through each plant in array and add +1 cup of water.
END IF
IF false
PRINT ("Your plants don't need water!")
END FOR
END FUNCTION
```

>2. As with the knot algorithm, there may be more than one way to solve the problem. It is essential to try to pick the best algorithm for a situation. Name three companies who created an algorithm that made them successful, e.g., Google's search algorithm. It doesn't need to be a tech example (such as a recipe or manufacturing a product). Google's algorithm produces more relevant results than other search engines; what about each of your cases make them stand out?
`A: Hopper app created an algorithm to track flight prices and predicts the cheapest time to buy your plane ticket. This stands out to me because the algorithm uses past data from airlines to get better prices for customers, which is something I haven't seen before them.`

>3. Hypothesize about what constitutes an efficient algorithm versus an inefficient algorithm.
`A: An efficient algorithm will have a sequence of logical steps, accomplish the goal set out, and finish quickly.
An inefficient algorithm will be out of order, not complete the goal, and take a very long time, possibly with bugs, and unnecessary or unclean code.`
