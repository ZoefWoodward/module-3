#### Exercises

>1. What is a hash table?
`A: A hash table is a collection of similar data.`

>2. What is hashing?
`A: A process that converts arbitrary data into a fixed-length code using the hashing function.`

>3. How does a hash table store data?
`A: It takes the key, converts it to a hash code using a hashing function, mods the hash code to get an array index, and then stores the value in the array index.`

>4. How are hash tables and objects different?
`A: Hash tables contain data with a variable number of consistently formatted values, each with an identifier; like employee information. And an object will contain a static number of distinct values of different types.`

>5. Determine whether you would use a hash table or an object to store each of the following pieces of data:
>A list of pets and their unique names.
`A: Object`

>The name, age, and the birthday of your best friend.
`A: Object`

>The name and location of every company in a given city.
`A: Hash Table`

>All of the books checked out from a library by a particular individual.
`A: Hash Table`

>The primary and secondary phone numbers for a contact.
`A: Hash Table`

>6. Build a system that allows a sales associate to enter a customer's name, address, and phone number into the system and look up customers using their phone numbers. Store this information in a hash table.
```var hash = (string, max) => {
  var hash = 0;
  for (var i =0; i <= string.length; i++){
    hash += string.charAt(i);
}
return hash % max;
};

let HashTable = function() {
  let storage = [];
  const storageLimit = 100;

  this.print = function() {
    console.log(storage);
  };

  this.add = function(phone, customerAddress){
    var index = hash(phone, storageLimit);
    if (storage[index] === undefined) {
      storage[index] = [ [phone, customerAddress]
      ];
    } else {
      var input = false;
      for (var i =0; i < storage[index].length; i++) {
        if (storage[index][i][0] === phone) {
          storage[index][i][1] = customerAddress;
          input = true;
      }
    }
    if (input === false){
      storage[index].push([phone, customerAddress]);
    }
  }
};

this.remove = function(phone) {
  var index = hash(phone, storageLimit);
  if (storage[index].length === 1 && storage[index][0][0] === phone) {
    delete storage[index];
  } else {
    for (var i = 0; i < storage[index].length; i++){
      if (storage[index][i][0] === phone) {
        delete storage[index][i];
      }
    }
  }
};

this.lookup = function(phone) {
  var index = hash(phone, storageLimit);
  if (storage[index] === undefined){
    return undefined;
  } else {
    for (var i =0; i < storage[index].length; i++){
      if (storage[index][i][0] === phone) {
        return storage[index][i][1];
      }
    }
  }
};
};

var customers = new HashTable();
customers.add("555-555-5555", "Zoe", "123 South Street");
customers.add("123-456-7890", "Jane Doe", "333 North Ave");
customers.add("707-707-7070", "John Doe", "321 Backwards Day Lane");
customers.lookup("555-555-5555");
```

>7. Build a system that allows a store owner to track their store's inventory using a hash table for storage.
```var hash = (string, max) => {
  var hash = 0;
  for(var i =0; i < string.length; i++){
    hash += string.charCodeAt(i);
  }
  return hash % max;
};

let HashTable = function() {
  let storage = [];
  const storageLimit = 100;

  this.print = function() {
    console.log(storage);
  };

  this.add = function(key, value) {
    var index = hash(key, storageLimit);
    if (storage[index] === undefined){
      storage[index] = [
        [key, value]
        ];
    } else {
      var input = false;
      for (var i = 0; i < storage[index].length; i++ ){
        if (storage[index][i][0] === key){
          storage[index][i][1] = value;
          input = true;
        }
      }
      if (input === false){
        storage[index].push([key, value]);
      }
    }
  };

  this.lookup = function(key) {
    var index = hash(key, storageLimit);
    if (storage[index] === undefined) {
      return undefined;
    } else {
      for (var i = 0; i < storage[index].length; i++) {
        if (storage[index][i][0] === key){
          return storage[index][i][1];
        }
      }
    }
  };
};

var inventory = new HashTable();
inventory.add("Avocados", "50");
inventory.add("Kombucha", "25");
inventory.add("Sushi Rolls", "20");
inventory.add("Almond Milk", "20");
inventory.lookup("Avocados");
```

>8. Build a system that allows digital copies of newspapers to be entered and searched by publisher and publication date. Use hash tables to store the necessary data.
```
var hash = (string, max) => {
  var hash = 0;
  for (var i = 0; i < string.length; i++){
    hash += string.charCodeAt(i);
  }
  return hash % max;
};

let HashTable = function(){
  let storage = [];
  const storageLimit = 25;


  this.add = function(key, value){
    var index = hash(key, storageLimit);
    if (storage[index] === undefined){
      storage[index] = [
        [key, value]
        ];
    } else {
      var input = false;
      for (var i = 0; i < storage[index].length; i++){
        if (storage[index][i][0] === key){
          storage[index][i][1] = value;
          input = true;
        }
      }
      if (input === false) {
        storage[index].push([key, value]);
      }
    }
  };

  this.lookup = function (key) {
    var index = hash(key, storageLimit);
    if (storage[index] === undefined){
      return undefined;
    } else {
      for (var i = 0; storage[index].length; i++){
        if (storage[index][i][0] === key){
          return storage[index][i][1];
        }
      }
    }
    };
    this.lookupDate = function(value) {
      var index = hash(value, storageLimit);
      if(storage[index] === undefined){
        return undefined;
      } else {
        for (var i = 0; storage[index].length; i++){
          if (storage[index][i][1] === value) {
            return storage[index][i][2];
          }
        }
      }
    };
};

var digitalCopies = [{
  publisher: "",
  publicationDate: "",
  article: ""
}];

var articleTable = new HashTable();
articleTable.add("Forbes", "2018");
articleTable.lookup("Forbes");
articleTable.lookupDate("2018");
```
