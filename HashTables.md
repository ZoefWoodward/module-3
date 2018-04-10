#### Exercises

>1. What is a hash table?
`A: A hash table is a collection of similar data.`

>2. What is hashing?
`A: A process that converts arbitrary data into a fixed-length code using the hashing function.`

>3. How does a hash table store data?
`A: It takes the key, converts it to a hash code using a hashing function, mods the hash code to get an array index, and then stores the value in the array index.`

>4. How are hash tables and objects different?
`A: Hash tables contain data with a variable number of consistently formatted values, each with an identifier; like employee information. And an object is will contain a static number of distinct values of different types.`

>5. Determine whether you would use a hash table or an object to store each of the following pieces of data:
>A list of pets and their unique names.
`A: Hash Table`

>The name, age, and the birthday of your best friend.
`A: Object`

>The name and location of every company in a given city.
`A: Hash Table`

>All of the books checked out from a library by a particular individual.
`A: Hash Table`

>The primary and secondary phone numbers for a contact.
`A: Object`

>6. Build a system that allows a sales associate to enter a customer's name, address, and phone number into the system and look up customers using their phone numbers. Store this information in a hash table.
```A: function lookupCustomer(phone number)
CREATE HashMapCustomerInfo
function handleCustomerInfo()
STORE each name, address, and phone number into HashMapCustomerInfo and associate with index (value)
CHECK whether HashMapCustomerInfo contains phone number from customer.
```

>7. Build a system that allows a store owner to track their store's inventory using a hash table for storage.
```A: function storeInventory(inventory)
CREATE HashMapStoreInventory
STORE inventory info into HashMapStoreInventory and associate with inventory (value)
CHECK storeInventory(value)
```

>8. Build a system that allows digital copies of newspapers to be entered and searched by publisher and publication date. Use hash tables to store the necessary data.
```A: function enterNewspaper(publisher, publication date)
CREATE HashMapNewspaper
CREATE digital copy with publisher and publication date
STORE enterNewspaper into HashMapEnterNewspaper and associate with digital copy (value)
function searchNewspaper(publisher, publication date)
CHECK HashMapNewspaper for digital copy(value)
```
