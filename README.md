# stack-code-in-python
Stack  in python
class Stack:
    def __init__(self):
        self.stack = []

  def push(self, item):
        """Adds an item to the stack"""
        self.stack.append(item)

   def pop(self):
        """Removes the top item from the stack and returns it"""
        if not self.is_empty():
            return self.stack.pop()
        else:
            raise IndexError("pop from an empty stack")

   def peek(self):
        """Returns the top item of the stack without removing it"""
        if not self.is_empty():
            return self.stack[-1]
        else:
            raise IndexError("peek from an empty stack")

   def is_empty(self):
        """Checks whether the stack is empty"""
        return len(self.stack) == 0

  def size(self):
        """Returns the number of items in the stack"""
        return len(self.stack)

# Example usage:
stack = Stack()
stack.push(10)
stack.push(20)
stack.push(30)

print("Top of the stack:", stack.peek())  # Output: 30
print("Stack size:", stack.size())        # Output: 3

print("Popped item:", stack.pop())        # Output: 30
print("Stack size after pop:", stack.size())  # Output: 2

