#### Exercises

> 1. A line of people at an amusement park ride.
 The line is composed of members, represented as strings.
 There is a front to the line, as well as a back.
 When someone enters the line, place them at the end.
 People may leave the line whenever they see fit, and those behind them take their place.
> Given the above real-world information, use an array data structure to code the following solution.
a) Use an array input: ["Vivian", "Ava", "Josh", "Patrick", "Mike"]
`var newPerson = (["Vivian", "Ava", "Josh", "Patrick", "Mike"])`

>b) Insert a new person, "Mary" at the end of the line. In other words, you should insert Mary after Mike.
`newPerson.push("Mary");`

>c) Find a person in line named "Josh." This function should return the position of 2 in the array, (recall that arrays are 0-based).
`var newPerson = (["Vivian", "Ava", "Josh", "Patrick", "Mike"]);

function findPerson(name){
for (var i=0; i <= newPerson.length; i++){
if (newPerson[i] === name) {
console.log("Found" + " " + name + " " + "at index" + " " + i);
return true;
}
}`

>d) Find a person in line named "Emily." What should your function return if it does not find the item in the array?
`return false;
}
var person = findPerson('Emily');
if (!person) console.log('Emily is not in line!');`

>e) What if Ava wants to allow a friend, "Melissa", to cut in line in front of her? How would you code this so Melissa appears before Ava?
`newPerson.splice(1, 0, "Melissa");`

>f) If Patrick wants to leave the line, how would you delete him from the array?
`newPerson.splice(4, 1);
newPerson;`


>2. Provide another real-world example that you can model using a data structure.
`A: A product waitlist may require a data structure where people will come and go from the list and emails are deployed as items become available for purchase.``

>3. How would your data structure allow developers to access and manipulate the data?
`A: They could access the names of people currently waiting for products to become available, and can manipulate the data by updating customers as products become available for those who have waited the longest.`
