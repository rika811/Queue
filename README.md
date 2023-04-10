# Queue

## What Is a Queue Data Structure?

A queue is also a non-primitive, linear data structure that stores elements in a sequential manner. However, the queue data structure follows a FIFO (First In First Out) order to store and retrieve elements from the memory. It can also only store similar kinds of elements in the queue.

An example of a queue can be a line or a queue in a bank in which the person who comes first will be served first. Therefore, it follows the FIFO order to process the elements.

### Basic Operations of Queue

A queue is an object (an abstract data structure - ADT) that allows the following operations:

+ Enqueue: Add an element to the end of the queue
+ Dequeue: Remove an element from the front of the queue
+ IsEmpty: Check if the queue is empty
+ IsFull: Check if the queue is full
+ Peek: Get the value of the front of the queue without removing it

### peek()
This function helps to see the data at the front of the queue. The algorithm of peek() function is as follows −

**Algorithm-**

```
begin procedure peek
   return queue[front]
end procedure
```

### isfull()
As we are using single dimension array to implement queue, we just check for the rear pointer to reach at MAXSIZE to determine that the queue is full. In case we maintain the queue in a circular linked-list, the algorithm will differ. Algorithm of isfull() function −

**Algorithm-**

```
begin procedure isfull

   if rear equals to MAXSIZE
      return true
   else
      return false
   endif
end procedure
```
### isempty()
Algorithm of isempty() function −

**Algorithm-**

```
begin procedure isempty

   if front is less than MIN  OR front is greater than rear
      return true
   else
      return false
   endif
   
end procedure
```
### Algorithm for enqueue operation

```
procedure enqueue(data)      

   if queue is full
      return overflow
   endif
   
   rear ← rear + 1
   queue[rear] ← data
   return true
   
end procedure
```

### Algorithm for dequeue operation
```
procedure dequeue
   
   if queue is empty
      return underflow
   end if

   data = queue[front]
   front ← front + 1
   return true

end procedure
```
