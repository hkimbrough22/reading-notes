# Code 401 - Reading Notes

<!-- All references used were from Code 401 reading
assignment 30 -->

[comment]: <> (https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)

[comment]: <> (https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)

[comment]: <> (https://www.youtube.com/watch?v=MfhjkfocRR0)

[comment]: <> (https://en.wikipedia.org/wiki/Hash_table)

## Hash Tables
### Common Terminology
- Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.
- Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.
- Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.


Useful for holding unique values.

### Basic Idea
- The basic idea of a hashtable is the ability to store the key into this data structure, and quickly retrieve the value. This is done through what we call a hash. A hash is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.

- Since we are able to hash our key and determine the exact location where our value is stored, we can do a lookup in an O(1) time complexity.


### General Functionality
- Hash maps do this to store values:
  1. accept a key
  2. calculate the hash of the key
  3. use modulus to convert the hash into an array index
  4. store the key with the value by appending both to the end of a linked list
  
  
- Hash maps do this to read value:
  1. accept a key
  2. calculate the hash of the key
  3. use modulus to convert the hash into an array index
  4. use the array index to access the short LinkedList representing a bucket
  5. search through the bucket looking for a node with a key/value pair that matches the key you were given


### Useful Methods
#### Add()
- When adding a new key/value pair to a hashtable:

1. send the key to the GetHash method.
2. Once you determine the index of where it should be placed, go to that index
3. Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
4. If something does exist, add the new key/value pair to the data structure within that bucket.

#### Find()
- The Find takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm to iterate through the bucket and see if the key exists and return the value.

#### Contains()
- The Contains method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to have the contains call the GetHash and check the hashtable if the key exists in the table given the index returned.

#### GetHash()
- The GetHash will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.


[BACK TO HOME](../README.md)