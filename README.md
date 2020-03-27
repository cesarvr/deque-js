# Deque

this is just a implementation of Python [deques](https://docs.python.org/2/library/collections.html#collections.deque) in JS. Deques are a generalization of stacks and queues (the name is pronounced “deck” and is short for “double-ended queue”).

Though list objects support similar operations, they are optimized for fast fixed-length operations and incur O(n) memory movement costs for pop(0) and insert(0, v) operations which change both the size and position of the underlying data representation.

## Install 

```sh
npm install dqs 
```

## Usage

```js
let dqueue = require('dqs')
```

## Methods 

#### insert(x)
Add x to the right side of the deque.

#### all 
Return all the objects in an Array.

#### clear() 
Remove all elements from the deque leaving it with length 0.

#### count(x)
Count the number of deque elements equal to x.

#### pop()
Remove and return an element from the right side of the deque. If no elements are present, raises an IndexError.

#### popleft()
Remove and return an element from the left side of the deque. If no elements are present, raises an IndexError.

```js
let dq = new DQueue([2,3,0,1])
let v1 = dq.popLeft()
let v2 = dq.popLeft()

console.log(v1, v2) // 2 3
console.log(dq.all()) // [0,1]

```

#### rotate(n=1)
Rotate the deque n steps to the right. If n is negative, rotate to the left.

```js
let dqueue = new DQS([2,3,0,1])
dqueue.rotate(-2)
//[0,1,2,3]
```




When the deque is not empty, rotating one step to the right is equivalent to d.appendleft(d.pop()), and rotating one step to the left is equivalent to d.append(d.popleft()).

