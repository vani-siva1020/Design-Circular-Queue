# Design-Circular-Queue
🔄 Design Circular Queue (Java)
📌 Problem Statement

Design a Circular Queue data structure that supports the following operations:

enQueue(value) – Insert an element into the circular queue.

deQueue() – Delete an element from the circular queue.

Front() – Get the front item.

Rear() – Get the last item.

isEmpty() – Check whether the circular queue is empty.

isFull() – Check whether the circular queue is full.

The circular queue should be implemented using a fixed-size array.

💡 Approach

This implementation uses:

An integer array queue[] to store elements.

head pointer to track the front element.

count to track the number of elements currently in the queue.

capacity to store the maximum size of the queue.

🔁 Why Circular?

Instead of shifting elements after deletion, we use modulo (%) operation to wrap around the array.

Formula used:

Insert index → (head + count) % capacity

Rear index → (head + count - 1) % capacity

Move head → (head + 1) % capacity

This makes all operations O(1) time complexity.

🧠 Time & Space Complexity
Operation	Time Complexity
enQueue	O(1)
deQueue	O(1)
Front	O(1)
Rear	O(1)
isEmpty	O(1)
isFull	O(1)

Space Complexity: O(k)
(where k is the capacity of the queue)
