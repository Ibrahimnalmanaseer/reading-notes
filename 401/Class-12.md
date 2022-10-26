# Stack and Queue

## Stack :
Stack is a container of objects that are inserted and removed according to the last-in first-out (LIFO) principle.

![stackImg](https://user-images.githubusercontent.com/62019258/198150574-83b4b434-043b-480c-8278-e6471c54d9b0.jpg)



Push the item into the stack, and pop the item out of the stack. 

A stack is a limited access data structure - elements can be added and removed from the stack only at the top


## Queue :

Queue is a container of objects (a linear collection) that are inserted and removed according to the first-in first-out (FIFO) principle.

![queueImg](https://user-images.githubusercontent.com/62019258/198150803-0f604ab7-86c3-4b46-a254-0a2863f78409.jpg)


In the queue only two operations are allowed enqueue and dequeue. 
Enqueue means to insert an item into the back of the queue, dequeue means removing the front item.


## Stack and Queue Implementation :



### Basic Operations of Stack
There are some basic operations that allow us to perform different actions on a stack.

- **Push**: Add an element to the top of a stack
- **Pop**: Remove an element from the top of a stack
- **IsEmpty**: Check if the stack is empty
- **IsFull**: Check if the stack is full
- **Peek**: Get the value of the top element without removing it


### Working of Stack Data Structure

The operations work as follows:

- A pointer called TOP is used to keep track of the top element in the stack.
- When initializing the stack, we set its value to -1 so that we can check if the stack is empty by comparing TOP == -1.
- On pushing an element, we increase the value of TOP and place the new element in the position pointed to by TOP.
- On popping an element, we return the element pointed to by TOP and reduce its value.
- Before pushing, we check if the stack is already full
- Before popping, we check if the stack is already empty

```
# Stack implementation in python


# Creating a stack
def create_stack():
    stack = []
    return stack


# Creating an empty stack
def check_empty(stack):
    return len(stack) == 0


# Adding items into the stack
def push(stack, item):
    stack.append(item)
    print("pushed item: " + item)


# Removing an element from the stack
def pop(stack):
    if (check_empty(stack)):
        return "stack is empty"

    return stack.pop()


stack = create_stack()
push(stack, str(1))
push(stack, str(2))
push(stack, str(3))
push(stack, str(4))
print("popped item: " + pop(stack))
print("stack after popping an element: " + str(stack))
```
