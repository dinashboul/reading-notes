# Hashtables

1- **Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.**

2-**Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.**

3- **Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.**

## Why do we use them?

### Hold unique values

### Dictionary

### Library


### Note: Hashtables are a data structure that utilize key value pairs. This means every Node or Bucket has both a key, and a value.

#### A hash is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.

#### Arrays actually have fast access. If we know the index of the information we want we can access that information in O(1) time. The reason why searching for a piece of data in a collection is O(N) isn’t because the array is slow, it’s just that we have to look through all N things in the collection.

#### Hash maps take advantage of an array’s O(1) read access. Instead of adding elements to an array from beginning to end, a hash map uses a “hash function” to place each item at a precise index location, based off it’s key.

### Structure

#### Creating a Hash

**Here is a simplistic hashing algorithm:**

- Add or multiply all the ASCII values together.

- Multiply it by a prime number such as 599.

- Use modulo to get the remainder of the result, when divided by the total size of the array.

- Insert into the array at that index.

**NOTE: Production systems will have much more robust hashing algorithms that ensure even distribution of values across all buckets and avoid unnecessary collisions.**

### Collisions

**A collision occurs when more than one key hashes to the same index in an array. As mentioned earlier, a “perfect hash” will never have any collisions. To put this into perspective, the worst possible hash is one that hashes every single key to the same exact index of an array. The more keys you have hashed to a specific index, the more key/value pair combos you can potentially have.**

### Hash maps do this to store values:

- accept a key

- calculate the hash of the key

- use modulus to convert the hash into an array index

- store the key with the value by appending both to the end of a linked list

### Hash maps do this to read value:

- accept a key

- calculate the hash of the key

- use modulus to convert the hash into an array index

- use the array index to access the short LinkedList representing a bucket

- search through the bucket looking for a node with a key/value pair that matches the key

### Bucket Sizes

**Hash Maps can have any number of buckets. If a hash map has only a few buckets it will be densely full and have many collisions. If a hash map has more buckets it will be more sparsely populated, there will be less collisions, but there may be a lot of extra empty space.**

### Methods

_ set()

- get()

- has()

- keys()

- hash()
