# Exercise: Data Structures

# Sprint One: Object-Oriented Programming
---
In this assignment, we'll implement and test two basic data structures:

### 1. [Queue](http://en.wikipedia.org/wiki/Queue_(abstract_data_type))

A queue works like a line for an amusement park ride -- people enter at the end of the queue and leave from the front (*FIFO*: first in, first out).

<!-- ![queue image](../images/200px-Data_Queue.svg.png) -->

#### A queue would be great for....

Issuing instructions to your sandwich-making robot.

### 2. [Stack](http://en.wikipedia.org/wiki/Stack_(abstract_data_type))

A stack works like a stack of plates -- plates are added and removed from the the top of the stack (*LIFO*: last in, first out).

<!-- ![stack image](../images/200px-Data_stack.svg.png) -->

#### A stack would be great for...

Implementing your browser's back button.

## Bare Minimum Requirements

Implement both **stack** and **queue** data structures in each of the instantiation styles. The functional style is stubbed out in `src/functional/queue.js` and `src/functional/stack.js` to get you started.

* No arrays! Instead, use an object with numeric keys
- [ ] Pass all the tests. To run all the tests, first run `npm start` in your terminal from the sprint's root directory. You'll know if this step completed successfully when you see the following output in your terminal:

  ```
  Serving "/Users/.../your-sprint-folder" at http://127.0.0.1:xxxx
  ```

  Now, navigate to the `http://127.0.0.1:xxxx` link in your browser (don't forget to include the colon and extra numbers at the end), and open the `SpecRunner.html` file.

### Data Structure Specs

- [ ]  Implement a [stack](http://en.wikipedia.org/wiki/Stack_(abstract_data_type)) with the following methods:
    -  `push(string)` - Add a string to the top of the stack
    -  `pop()` - Remove and return the string on the top of the stack
    -  `size()` - Return the number of items on the stack

- [ ]  Implement a [queue](http://en.wikipedia.org/wiki/Queue_(abstract_data_type)) with the following methods:
    -  `enqueue(string)` - Add a string to the back of the queue
    -  `dequeue()` - Remove and return the string at the front of the queue
    -  `size()` - Return the number of items in the queue

### Instantiation Styles

1.  **Functional instantiation**: a simple "maker" pattern
    - *Do:*
        - Work within the `src/functional/` folder
        - Define all functions and properties within the maker function
        - Capitalize the maker function name
    - *Don't:*
        - Use the keyword `new`, the keyword `this`, or any `prototype` chains
    - *Example*: The provided classes `Stack` and `Queue` already follow this pattern

2.  **Functional instantiation with shared methods**: same as step 1, but with shared methods
    - *Do:*
        - Work within the `src/functional-shared/` folder
        - Create an object that holds the methods that will be shared by all instances of the class
        - Use the keyword `this` in your methods
        - Use [`_.extend`](http://underscorejs.org/#extend) to copy the methods onto the instance
    - *Don't:*
        - Use the keyword `new` or `prototype` chains
    - *Example*: [functional instantiation example](https://github.com/hackreactor/giraffeMaker/blob/master/src/giraffeExtend.js)

3.  **Prototypal instantiation**: using `Object.create`
    - *Do:*
        - Work within the `src/protoypal/` folder.
        - Use [`Object.create`](http://mdn.io/Object.create) with the object from step 2 to create instances of your class
    - *Don't:*
        - Use the keyword `new`
    - *Example:* [prototypal instantiation example](https://github.com/hackreactor/giraffeMaker/blob/master/src/giraffePrototype.js)

4.  **Pseudoclassical instantiation**: create instances with the keyword `new`
    - *Do:*
        - Work within the `src/pseudoclassical/` folder
        - Capitalize your function name to indicate to others that it is intended to be run with the keyword `new`
        - Use the keyword `new` when instantiating your class
        - Use the keyword `this` in your constructor
    - *Don't:*
        - Declare the instance explicitly
        - Return the instance explicitly
    - *Example:* [pseudoclassical instantiation example](https://github.com/hackreactor/giraffeMaker/blob/master/src/giraffePseudoClassical.js)

5.  **ES6 instantiation**: declare classes with the keyword `class`
    - *Do:*
        - Work within the `src/es6/` folder
        - Capitalize your function name to indicate to others that it is intended to be run with the keyword `new`
        - Use the keyword `new` when instantiating your class
        - Use the keyword `this` in your constructor
        - Explicitly declare a class method named `constructor`
        - Declare all other class methods within the class declaration
    - *Don't:*
        - Declare the instance explicitly
        - Return the instance explicitly
        - Add class methods to the class prototype directly
    - *Example:* [es6 instantiation example](https://github.com/hackreactor/giraffeMaker/blob/master/src/giraffeES6.js)

# Sprint Two: Data Structures
---

This repo holds a mostly-empty [Mocha](https://mochajs.org/) test suite. To run all the tests, first run `npm start` in your terminal from the sprint's root directory. You'll know if this step completed successfully when you see the following output in your terminal:

```
Serving "/Users/.../your-sprint-folder" at http://127.0.0.1:xxxx
```

Now, navigate to the `http://127.0.0.1:xxxx` link in your browser (don't forget to include the colon and extra numbers at the end), and open the `SpecRunner.html` file.

Some failing specs are included. You're welcome! You should make them pass, then write more specs and more code.

## Bare Minimum Requirements

### Implement and test the following classes:

### 1. [Linked List](https://en.wikipedia.org/wiki/Linked_list)

A linked list is a dynamic data structure that allows for constant time insertion and removal at any point in the linked list (compare this to an array which on average has linear time insertion and removal operations). In exchange for this insertion and removal speed, linked lists are not indexed and any find operations on a link list require the linear time operation of traversing the entire linked-list from the beginning.

<!-- ![Linked List image](../images/43154574-2615-11e3-8e29-43cf74e25b10.png) -->

#### A linked list would be great for....

An itinerary you expect to add and remove destinations to and from.

* A `linkedList` class, in functional style, with the following properties:
  - [ ] `.head` property, a `linkedListNode` instance
  - [ ] `.tail` property, a `linkedListNode` instance
  - [ ] `.addToTail()` method, takes a value and adds it to the end of the list
  - [ ] `.removeHead()` method, removes the first node from the list and returns its value
  - [ ] `.contains()` method, returns boolean reflecting whether or not the passed-in value is in the linked list
  - [ ] What is the time complexity of the above functions?

### 2. [Tree](https://en.wikipedia.org/wiki/Tree_(data_structure))

A tree is a hierarchical data structure consisting of a node (potentially) with children. The children are trees unto themselves, that is, nodes with (potential) children. For this reason the tree is referred to as a recursive data structure.

<!-- ![Tree image](../images/ternary-and-quaternary-tree.gif) -->

#### A tree would be great for....

Making a family tree.

* A `tree` class, in functional with shared methods style, with the following
  properties:
  - [ ] `.children` property, an array containing a number of subtrees
  - [ ] `.addChild()` method, takes any value, sets that as the target of a node, and adds that node as a child of the tree
  - [ ] A `.contains()` method, takes any input and returns a boolean reflecting whether it can be found as the value of the target node or any descendant node
  - [ ] What is the time complexity of the above functions?

### 3. [Graph](http://en.wikipedia.org/wiki/Graph_(mathematics))

Graphs consist of nodes (often referred to as vertices) and edges (often referred to as arcs) that connect the nodes. Unlike trees, graphs are not necessarily
hierarchical. Graphs can be undirected, which means that the relationship of any 2 nodes connected by an edge is a symmetrical relationship, or they can be directed,
which means there is an asymmetrical relationship between nodes that are connected by an edge. You will be implementing an undirected graph.

<!-- ![Graph image](../images/PlN2VGG.png) -->

#### A graph would be great for....

Representing how a collection of websites (or the entire world wide web) link to each other, and [many other things](https://www.cs.princeton.edu/courses/archive/spring13/cos226/lectures/42DirectedGraphs.pdf)

* Implement a `graph` class, in pseudoclassical style, with the following properties:
  - [ ] It is an undirected graph.  It does not have to be 'connected'.
  - [ ] An `.addNode()` method that takes a new node and adds it to the graph
  - [ ] A `.contains()` method that takes any node and returns a boolean reflecting whether it can be found in the graph
  - [ ] A `.removeNode()` method that takes any node and removes it from the graph, if present. All edges connected to that Node are removed as well.
  - [ ] An `.addEdge()` method that creates a edge (connection) between two nodes if they both are present within the graph
  - [ ] A `.hasEdge()` method that returns a boolean reflecting whether or not two nodes are connected
  - [ ] A `.removeEdge()` method that removes the connection between two nodes
  - [ ] A `.forEachNode()` method that traverses through the graph, calling a passed in function once on each node
  - [ ] What is the time complexity of the above functions?

### 4. [Set](https://en.wikipedia.org/wiki/Set_(abstract_data_type))

Sets contain unique values in no particular order.

![Set image](../images/Sets02.png)

#### A set would be great for....

A raffle, where all the tickets are unique and you just want to randomly pick one (or several) out of them all.

* A `set` class, in prototypal style, with the following properties:
  - [ ] An `.add()` method, takes any string and adds it to the set
  - [ ] A `.contains()` method, takes any string and returns a boolean reflecting whether it can be found in the set
  - [ ] A `.remove()` method, takes any string and removes it from the set, if present
  - [ ] What is the time complexity of the above functions?
  * **Note:** Sets should not use up any more space than necessary. Once a value is added to a set, adding it a second time should not increase the size of the set.
  * **Note:** Until the advanced section, your sets should handle only string values.
  * **Note:** This is a rather simple data structure. Take a look at the [Wikipedia](https://en.wikipedia.org/wiki/Set_(abstract_data_type)) entry. Which native Javascript type fits the requirements best?

### 5. [Hash Table](https://en.wikipedia.org/wiki/Hash_tables)

Hash tables (sometimes called hash maps) store key value pairs. They do so in a memory efficient way by using a 'hashing function' that translates keys into
numerical indices located within a fixed block of memory (think about the contiguous blocks of memory used in arrays). Hash tables only increase their size
in memory when necessary, and reduce their size in memory when possible.

<!-- ![Hash Table image](https://user-images.githubusercontent.com/13425777/77678866-0d08c700-6f4f-11ea-8cb7-daf83e78d937.png) -->

#### A hash table would be great for....

A contact list you might add to or remove from over time.

- [ ] A `hashTable` class, in pseudoclassical style:
  * [ ] **First:** Play with each of the helper functions provided to get a sense of what they do.
    * You will use the provided hash function to convert any key into an array index. Try interacting with it from the console first.
    * A `limitedArray` helper has been provided for you, check out the source code for it in `src/hashTableHelpers.js`. Use it to store all inserted values rather than using a plain JavaScript array. The `limitedArray`, as you will see in the source code, provides `get`, `set`, and `each` methods which you should use in order to interact with it. Do not use the typical bracket notation for arrays when interacting with a `limitedArray` instance. Try interacting with it from the console first.
  * Make the following properties appear on all instances:
    * [ ] An `.insert()` method
    * [ ] A `.retrieve()` method
    * [ ] A `.remove()` method
  - [ ] What is the time complexity of the above functions?
- [ ] Using your understanding of hash tables, refactor your set implementation from above to run in constant time

**On Objects and Hash Tables:** An astute hacker might find themself wondering "Is it not so that a JavaScript object is a hash table?" or even further, "Why would I ever need to create a hash table in JavaScript?" While it is true that objects and hash tables are functionally similar, knowing how a hash table works is hugely important as they are an incredibly useful and fundamental data structure. To have detailed knowledge of how a hash table is constructed will give you valuable insight on your path to code mastery. Additionally, other languages might not provide the convenience of JavaScript's object class, meaning you may someday have to put your hash table construction abilities to good use.

**Interesting Aside: JavaScript objects aren't necessarily backed by hash tables. Despite the similarities, the [ECMA-262](http://www.ecma-international.org/publications/files/ECMA-ST/Ecma-262.pdf) standard makes no restrictions on how JavaScript objects are implmented. The [V8 JavaScript engine](https://developers.google.com/v8/design?hl=sv&csw=1#prop_access), which is used in Chrome, implements objects in a way that is significantly faster than using a hash table.


### 6. [Binary Search Tree](http://en.wikipedia.org/wiki/Binary_search_tree)

Binary trees are trees that can only have 0, 1, or 2 children. Remember that trees are recursive data structures and therefore a tree's children are themselves trees and
can each have 0, 1, or 2 children. In a binary *search* tree, one child (out of potentially two) will always be less than the node's value (based on whatever sorting
condition you wish) and the other child will always be greater than the node's value. Whether it is the 'left' or the 'right' child which is greater or lesser is consistent
throughout the binary search tree. This structure results in particularly fast find operations. You'll be asked to answer just how fast yourself.

<!-- ![Binary Search Tree image](../images/eDw57vR.png) -->

#### A binary search tree would be great for....

A dictionary of all English words.

* Implement a `binarySearchTree` class with the following properties:
  - [ ] A `.left` property, a binary search tree (BST) where all values are lower than the current value.
  - [ ] A `.right` property, a BST where all values are higher than the current value.
  - [ ] A `.insert()` method, which accepts a value and places it in the tree in the correct position.
  - [ ] A `.contains()` method, which accepts a value and returns a boolean reflecting whether or not the value is contained in the tree.
  - [ ] A `.depthFirstLog()` method, which accepts a callback and executes it on every value contained in the tree.
  - [ ] What is the time complexity of the above functions?
  * Use case: Given a list of a million numbers, write a function that takes a new number and returns the closest number in the list using your BST. Profile this against the same operation using an array.

### Tests

- [ ] For each of the data structures you have implemented, go back and add at least one additional unit test. If possible, try to add a test that will require you improve your implementation in order to make the test pass.

## APIs and Implementation: A Note on Communicating Your Intentions as a Developer

**tl;dr**: _prefix private properties and methods with an underscore_

APIs are more than just URLs that return data; **API** is a general term that refers to the visible surface of any system, object, or library with which your code interacts. E.g., an airplane has an API that consists of knobs, dials, pedals, and a yoke which allow the pilot to make use of the airplane's underlying **implementation**--an engine, wings, and rudders. Importantly, the next model of airplane will probably have improvements to the engine, but the pilot need not know about this, as the controls will remain basically unchanged.

This relationship between APIs and implementations--that they remain independent--is what keeps the towering stacks of software we use everyday from falling over.

In JavaScript, because there is no concept of private variables (except through closure), sometimes API and implementation are both visible. If it's impossible to distinguish between API and implementation, you might depend upon a piece of implementation that later changes and breaks your code.

To prevent this from happening to your collaborators and consumers, indicate private properties and methods by prefixing them with an underscore. This is how we do.

## Advanced Content

Our advanced content is intended to throw you in over your head, requiring you to solve problems with very little support or oversight, much like you would as a mid or senior level engineer.

-  **Use the [Chrome profiling tools] to compare the performance of each instantiation pattern.**
    -  Create a new HTML page with your data structures and an additional profiling script.  It should instantiate and use a large number of stacks and queues
    -  Reload the page with the CPU profiler running to investigate the runtime of your functions
    -  Take a heap snapshot to investigate object allocations and memory use
    -  Optionally, reload the page with the heap profiler running to investigate garbage collection behavior
    -  Do this for each of the instantiation styles, record, and compare the results. Write a brief analysis you could share with a supervisor who needs the information you have in order to make wise decisions about the design of an upcoming project.

**Note**: _The following prompts have varying levels of difficulty and you may not wish to complete all of them in entirety. In order to decide how to allocate your time, please read the descriptions of all of them before starting._

Implement the following data structures and improvements. Use any instantiataion style you like.

**Optional, but highly recommended**: Use TDD.

* Create a [`doubly-linked-list`](http://en.wikipedia.org/wiki/Doubly_linked_list), with all the methods of your linked list, and add the following properties:
  - [ ] An `.addToHead()` method which takes a value and adds it to the front of the list.
  - [ ] A `.removeTail()` method which removes the last node from the list and returns its value.
  * Note: each `node` object will need to have a new `.previous` property pointing to the node behind it (or to `null` when appropriate); this is what makes it a doubly-linked list.
* Add parent links to your `tree`
  * [ ] A `.parent` property, which refers to the parent node or null when there is no node
  * [ ] A `.removeFromParent()` method, which disassociates the tree with its parent (in both directions)

- [ ] To prevent excessive collisions, make your `hashTable` double in size as soon as 75 percent of the spaces have been filled
- [ ] To save space, make sure the `hashTable` halves in size when space usage falls below 25 percent
- [ ] Implement a `.traverse()` method on your `tree`. Your `.traverse()` should accept a callback and execute it on every value contained in the tree
- [ ] `.breadthFirstLog()` method for `binarySearchTee`, logs the nodes contained in the tree using a breadth-first approach
- [ ] Make your `set` capable of handling numbers as well as strings
- [ ] Make your `set` capable of handling input objects of any type
- [ ] Make your `binarySearchTree` rebalance as soon as the max depth is more than twice the minimum depth

* Implement a `bloomFilter`:
  - [ ] Read the [Wikipedia article about Bloom Filters](http://en.wikipedia.org/wiki/Bloom_filter) and/or [BillMill.org](http://billmill.org)'s [Bloom Filters by Example](http://billmill.org/bloomfilter-tutorial/). tl;dr: It's a probabalistic data structure that efficiently determines whether or not an element is contained in a set. The downside is that is can report false positives. Use cases are often for checking against a giant list locally and only doing a full lookup when the local one comes back positive.
  - [ ] Create an "m=18, k=3" bloom filter. This means 18 slots, with 3 hash functions.
  - [ ] Run a small loop that runs 10,000 trials of trying to retreive a mix of items that are in the filter and not in the filter.
  - [ ] Record the empirical rate of false-positives by comparing your result with what you know to be true from the inputs you selected.
  - [ ] Compare that rate with the approximation given for Bloom filters, which is approximated as `(1- e^(-kn/m))^k`

## Nightmare Mode

**Note:** Please feel free to attempt the following in any order you would like.

- [ ] Write a [`prefixTree`](https://en.wikipedia.org/wiki/Trie) that can handle autocomplete for T9-style texting
- [ ] Write a [`bTree`](http://en.wikipedia.org/wiki/B-tree)
- [ ] Write a [`redBlackTree`](http://en.wikipedia.org/wiki/Red%E2%80%93black_tree)
- [ ] Design a data structure that finds every English word that can be made from a given bag of Scrabble letters
  * [ ] Optimize the algorithm and the data structure to return the set of words as quickly as possible
    * Your priority for this task is to optimize for time complexity, but do try to avoid wasted space in your solution
    * You can assume you have all the time required to do preprocessing on a dictionary of English words
- [ ] Advanced [`graph`](http://en.wikipedia.org/wiki/Graph_(mathematics)) work using [Node.js](https://nodejs.org/) (see section below)

### Advanced Graphs with Node.js

For this exercise you will work with adjacency list representations of graphs
using Node.js, which will allow you to interact with your file system. You'll
learn a ton about node later in the course, but this is advanced content so why
not get started early.

  * [ ] Create a basic JavaScript file that logs something to the console
  * [ ] In the terminal, in the directory of the file you just created (for this example let's say it's called `test.js`) run the command `node test.js`. You just ran JavaScript with the node interpreter and should see whatever you logged to the console in the terminal
  * [ ] Familiarize yourself with [Adajency Lists](https://en.wikipedia.org/wiki/Adjacency_list) and [Adjacency Matrices](https://en.wikipedia.org/wiki/Adjacency_matrix)
  * [ ] Whiteboard either a directed or an undirected graph and then translate it into an adjacency list text file
  * [ ] Write a function to return how many nodes your graph has. In order to accomplish this you will need to use node's `fs` module to read your adjacency list text file and split it into lines. You'll learn how to do this later in the course, but for now, feel free to use the following code:

    ``` javascript
    // this line lets you access the file system. You'll learn more about it later in the course
    var fs = require('fs');

    // read the `adjacency-list` file in this directory (you might have named the file differently) and split it on new lines into an array
    var fileLines = fs.readFileSync('./adjacency-list').toString().split('\n');

    // you may have to do this 0 or more times, to remove blank lines from fileLines
    fileLines.pop();

    fileLines.forEach(function(line) {
      // here you have access to each line of the adjacency list
      console.log(line);
    });
    ```

  * [ ] Write a function to peform a [depth first search](http://www.algolist.net/Algorithms/Graph/Undirected/Depth-first_search) (DFS) on your graph and output the node values in depth first order
    * [ ] Write Unit Tests for your DFS function
  * [ ] Try running your DFS function on a [larger adjacency list](https://snap.stanford.edu/data/#socnets)
    * [ ] Find, or create, a data set that will result in your exceeding the maximum call stack size, and then, refactor your DFS function to use [tail-call recursion](https://en.wikipedia.org/wiki/Tail_call) which is now possible in JavaScript on account of new language features introduced in the ES6 specification.
  * [ ] Implement [Karger's Algorithm](https://en.wikipedia.org/wiki/Karger%27s_algorithm) to identify the [Minimum Cut](https://en.wikipedia.org/wiki/Minimum_cut) for the minimum number of edges in an undirected graph
    * [ ] Write Unit Tests for your implementation
    * [ ] Start with a small undirected graph (in adjacency list format) of your own making, then give it a go with a [larger adjacency list](https://snap.stanford.edu/data/#socnets)
      * [ ] Try really hard to break your implementation so you are forced to improve it
  * [ ] Use [Kosaraju's Algorithm](https://en.wikipedia.org/wiki/Kosaraju%27s_algorithm) to identify the greatest [strongly connected component](https://en.wikipedia.org/wiki/Strongly_connected_component) (SCC) of a directed graph
    * [ ] Write Unit Tests for your implementation
    * [ ] Start with a small directed graph (in adjacency list format) of your own making, then give it a go with a [larger adjacency list](https://snap.stanford.edu/data/#socnets)
      * [ ] Try really hard to break your implementation so you are forced to improve it

  * [ ] Build a web crawler (see the Nightmare Mode content from the Recursion Review repo), to crawl the [webgraph](https://en.wikipedia.org/wiki/Webgraph), and utilize your implementation of Kosaraju's Algorithm to identify clusters of strongly connected web sites. Present your findings in a way that is easy for humans to understand.
    * [ ] Make your web crawler robust enough to run overnight, recovering from failures, so that you can return in the morning with massive amounts of meaningful data.
    * [ ] As your web crawler runs, store all the information it gathers in [redis](http://redis.io/). You will have to use [the Node.js redis client](https://github.com/NodeRedis/node_redis) in order to do this.

## Resources

- [Data structure coverage in Wikipedia](https://en.wikipedia.org/wiki/Data_structure) is no joke. Consider heading to Wikipedia when you have questions about data structures you are working with, or want to start learning about new ones.
- [VisuAlgo](http://visualgo.net/) is an incredible sight with clean visualizations of all kinds of data structures and algorithms.
- [functional instantiation example](https://github.com/hackreactor/giraffeMaker/blob/master/src/giraffeExtend.js)
- [prototypal instantiation example](https://github.com/hackreactor/giraffeMaker/blob/master/src/giraffePrototype.js)
- [pseudoclassical instantiation example](https://github.com/hackreactor/giraffeMaker/blob/master/src/giraffePseudoClassical.js)
- [es6 instantiation example](https://github.com/hackreactor/giraffeMaker/blob/master/src/giraffeES6.js)
- [Object.create](http://mdn.io/Object.create)
- [_.extend](http://underscorejs.org/#extend)
- [Mocha](http://visionmedia.github.io/mocha/)
- [Chrome profiling tools](https://developers.google.com/web/tools/chrome-devtools/profile/rendering-tools/js-execution)
- [Node.js](https://nodejs.org/)
- [Stack](http://en.wikipedia.org/wiki/Stack_(abstract_data_type))
- [Queue](http://en.wikipedia.org/wiki/Queue_(abstract_data_type))
- [Array](http://mdn.io/Array)
- [Array methods](http://mdn.io/Array#Methods_of_Array_instances)
- [Linked List](https://en.wikipedia.org/wiki/Linked_list)
- [Doubly Linked List](http://en.wikipedia.org/wiki/Doubly_linked_list)
- [Set](https://en.wikipedia.org/wiki/Set_(abstract_data_type))
- [Tree](https://en.wikipedia.org/wiki/Tree_(data_structure))
- [Binary Search Tree](http://en.wikipedia.org/wiki/Binary_search_tree)
- [Graph](http://en.wikipedia.org/wiki/Graph_(mathematics))
- [Graph Examples](http://algs4.cs.princeton.edu/lectures/42DirectedGraphs.pdf)
- [Hash Table](https://en.wikipedia.org/wiki/Hash_tables)
- [prefixTree](https://en.wikipedia.org/wiki/Trie)
- [bTree](http://en.wikipedia.org/wiki/B-tree)
- [redBlackTree](http://en.wikipedia.org/wiki/Red%E2%80%93black_tree)
- [adjacencyMatrix](https://en.wikipedia.org/wiki/Adjacency_matrix)
- [adjacencyList](https://en.wikipedia.org/wiki/Adjacency_list)
- [depthFirstSearch](http://www.algolist.net/Algorithms/Graph/Undirected/Depth-first_search)
- [largeDataSets](https://snap.stanford.edu/data/#socnets)
- [minimumCut](https://en.wikipedia.org/wiki/Minimum_cut)
- [kargersAlgorithm](https://en.wikipedia.org/wiki/Karger%27s_algorithm)
- [kosarajusAlgorithm](https://en.wikipedia.org/wiki/Kosaraju%27s_algorithm)
- [SCC](https://en.wikipedia.org/wiki/Strongly_connected_component)
