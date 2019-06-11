# parrot-queue

An efficient queue in JavaScript. Note that using native arrays as a queue
leads to O(n) runtime complexity for dequeuing, because shift takes O(n) in
the worst case.

## Usage

```
const ParrotQueue = require("parrot-queue");

const cinemaQueue = ParrotQueue();
cinemaQueue.enqueue('Clara');
cinemaQueue.enqueue('Peter');
cinemaQueue.enqueue('Lisa');
cinemaQueue.enqueue('John');

console.log(cinemaQueue.size()) // "4"

console.log(cinemaQueue.peek()) // "Clara"
console.log(cinemaQueue.dequeue()) // "Clara"
console.log(cinemaQueue.dequeue()) // "Peter"
console.log(cinemaQueue.dequeue()) // "Lisa"
console.log(cinemaQueue.size()) // "1"
```

## Methods

- `enqueue(object: any): void` Adds an object to the queue
- `size(): number` Returns the size of the queue
- `peek(): any` Return most recently added element
- `dequeue(): any` Return most recently added element and delete it from the queue

## Runtime complexity

- `enqueue`: O(1)
- `size`: O(1)
- `dequeue`: O(1)
- `peek`: O(1)
