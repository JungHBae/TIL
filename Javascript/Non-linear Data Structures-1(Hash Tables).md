# Hash Tables and Javascript Objects 

## Hash Tables

 Hash tables are another type of non-linear data structure that can be used in Javascript to store and retrieve key-value pairs. 
 In Javascript a hash table is implemented in the form of an **Object** or **Map**.
 A hash table is a data structure that uses a hash function to map keys to indices in an array.

 In a hash table, the keys are hashed using a hash function, which generates a unique index in the array for each key. 
 The value associated with the key is then stored in the array at that index. 
 When a value is to be retrieved, the key is hashed again to obtain the corresponding index in the array, and the value stored at that index is returned.
 
 ```mermaid
 graph LR
 A[Hash Table] --> B[Hash Function]
 B --> C[Hash Value]
 C --> D{Collision?}
 D -- Yes --> E[Chaining]
 D -- No --> F[Store Value]
 E --> G[Linked List 1]
 E --> H[Linked List 2]
 F --> I[Array Index]
```

 Hash tables are very efficient for storing and retrieving key-value pairs, because the **lookup time is constant** on average, 
 regardless of the number of elements in the hash table. However, hash tables can also have collisions, where two keys are hashed to the same index in the array. 
 To handle collisions, hash tables use a technique called collision resolution.

 In JavaScript, hash tables can be implemented using objects or the built-in Map object, which uses a hash table internally to store key-value pairs. 
 The choice of implementation depends on the specific requirements of the application and the features needed, such as ordering or iteration.

## Objects

 *Object* play a similar role as Hash tables, in that they both use key-value pairs to store and access data. 
 However, they are not exactly the same. 

 In JavaScript, you can use an object literal to create a hash table-like structure, but it's important to note that objects differ from hash tables. 
 For example, *objects* in JavaScript can have *prototype chains*, which is a feature that allows objects to inherit properties from other objects. 
 In contrast, *hash tables* are typically implemented as simple key-value stores without any inheritance or other complex features. 
 Additionally, objects in JavaScript are not guaranteed to maintain the *order* of their properties,
 while hash tables are typically ordered based on the hash function used to map keys to indices.
 
