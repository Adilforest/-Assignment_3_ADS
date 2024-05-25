# Assignment_3_ADS

## Execution

This program performs the following operations:

1. **Hash Table Operations**:
    - Inserts 10,000 random strings into the hash table.
    - Prints the sizes of the buckets in the hash table.
    - Displays:
        - The number of used buckets.
        - The average size per non-empty bucket.
        - The number of buckets with sizes above the average.
        - The maximum size of any bucket.
        - The number of unique keys.
        - The elapsed time for these operations.

2. **Binary Search Tree (BST) Operations**:
    - Inserts 10 random number keys with indexes into the BST.
    - Displays a list of key-value pairs using in-order traversal.
    - Prints the final size of the tree and the elapsed time for these operations.

## Main

The `Main` class includes a main method which calls the following methods:

- `testMyHashTable()`
- `testBST()`

## testMyHashTable

In this method:

- The `MyTestingClass` calculates custom hashes for strings and inserts 10,000 random strings into the hash table.
- The size of each bucket is printed to the console.
- The elapsed time for these operations is measured and displayed.

## testBST

In this method:

- The size field and its getter are implemented to display the size of the tree.
- A list of key-value pairs, composed using in-order traversal and the iterator method, is displayed.
- The `KeyValuePair` inner class allows access to both the key and the value during iteration.

## HashTable

The hash table is implemented using the separate chaining method for collision resolution. This approach provides an amortized time complexity of \(O(1)\), with a worst-case time complexity of \(O(N)\).

### Methods

- **Constructor**:
    - `public MyHashTable()`: Default constructor with a preset number of buckets.
    - `public MyHashTable(int M)`: Constructor that allows setting a custom number of buckets.

- **put(K key, V value)**:
    - Inserts the key-value pair into the hash table.
    - Resizes the table to a prime number at least twice its current size if the load factor exceeds 0.7.

- **get(K key)**:
    - Retrieves the value associated with the specified key.

- **remove(K key)**:
    - Removes the key-value pair from the hash table.

- **contains(K key)**:
    - Checks if the key exists in the hash table.

- **getKey(V value)**:
    - Retrieves the key associated with the specified value.

- **getBucketSizes()**:
    - Returns an `ArrayList<Integer>` containing the sizes of all buckets in the table.

## BinarySearchTree

A binary search tree (BST) where each node contains a key and a value. Each node ensures that:
- The left subtree contains keys less than the node's key.
- The right subtree contains keys greater than the node's key.

### Methods

- **put(K key, V value)**:
    - Inserts a node with the specified key and value into the tree.

- **get(K key)**:
    - Retrieves the value associated with the specified key.

- **delete(K key)**:
    - Deletes the node with the specified key.

- **iterator()**:
    - Returns an iterator over a list of key-value pairs, composed using in-order traversal.

- **size()**:
    - Returns the size of the tree.

### KeyValuePair

A class to represent a key-value pair.

- **Constructor**:
    - `KeyValuePair(K key, V value)`: Initializes a new key-value pair.

- **getKey()**:
    - Returns the key of the pair.

- **getValue()**:
    - Returns the value of the pair.
