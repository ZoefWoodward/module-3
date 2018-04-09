####Exercises

> Why do programmers use pseudocode?
A: It's a logical way to break down algorithms into small pieces.

> If you run pseudocode on your computer what would happen?
A: It wouldn't run unless you write it in a programming language.

#### Programming Assignment

>Write the following algorithms in pseudocode:

> Create a function that takes two numbers and prints out the greater number.

A:
```
FUNCTION
INPUT first number
INPUT second number
IF first number is less than second number
PRINT second number
END IF
ELSE PRINT 'Not greatest number'.
END ELSE
END FUNCTION
```

> Create a function that prints out the numbers from 1 to 100.

A:
```
FUNCTION
FOR SET counter to 0.
IF counter is less than or equal to 100.
ADD counter number iteration.
ENDFOR
PRINT counter.
ENDIF
END FUNCTION

```

> Create a function that searches for a specific entry in a phonebook.

A:
```
SET phonebook to array of entries: john, 555-555-5555, 123 south street.
FUNCTION
  SET iteration to 0.
  FOR an entry that is less than phonebook.length.
  INPUT iteration
  ENDFOR
    IF phonebook array is strictly equal to entry
      PRINT "Found entry" + " " + "entry" + " " + "at index" + " " + iteration
      RETURN true
    ENDIF
  ELSE
  RETURN FALSE
END FUNCTION

SET entry to findEntry name
IF not entry
PRINT "Entry does not exist!"
ENDIF
```

> Using the pseudocode you wrote for the previous question, implement it in any computer language of your choice.

A:
```var phonebook = ['john', '555-555-555', '123 south street'];

function findEntry(entry) {
  for (var i=0; i < phonebook.length; i++) {
    if (phonebook[i] === entry) {
      console.log("Found entry" + " " + entry + " " + "at index" + " " + i);
      return true;
    }
  }
  return false;
}

var entry = findEntry('john');
if(!entry) {
  console.log('Entry does not exist!');
}
```
