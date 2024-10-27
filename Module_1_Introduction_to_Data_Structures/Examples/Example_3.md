# Module Title: Introduction to Data Structures

## Example 3: Using Stacks for Expression Evaluation

### 1. Introduction
In this example, we will explore the concept of using stacks to evaluate expressions, a critical skill in both algorithmic problem-solving and practical applications within Robotics, semiconductors, and consumer electronics. Stacks are a fundamental data structure that follows the Last In First Out (LIFO) principle, making them ideal for tasks such as expression evaluation where operators and operands must be processed in a specific order.

The significance of this concept in fields like Robotics and semiconductors lies in its ability to manage complex calculations and operations efficiently. For instance, evaluating mathematical expressions is crucial in robotic control systems where real-time calculations are necessary for decision-making processes.

### 2. Code Snippet
Below is a Python code snippet demonstrating how to use a stack to evaluate a postfix expression (Reverse Polish Notation). The code includes error handling and follows best practices for readability and maintainability.

```python
class Stack:
    def __init__(self):
        self.items = []

    def push(self, item):
        self.items.append(item)

    def pop(self):
        if not self.is_empty():
            return self.items.pop()
        raise IndexError("Pop from empty stack")

    def peek(self):
        if not self.is_empty():
            return self.items[-1]
        raise IndexError("Peek from empty stack")

    def is_empty(self):
        return len(self.items) == 0

def evaluate_postfix(expression):
    stack = Stack()
    operators = set(['+', '-', '*', '/'])

    for token in expression.split():
        if token not in operators:
            try:
                stack.push(int(token))
            except ValueError:
                raise ValueError(f"Invalid token: {token}")
        else:
            try:
                right_operand = stack.pop()
                left_operand = stack.pop()
                if token == '+':
                    result = left_operand + right_operand
                elif token == '-':
                    result = left_operand - right_operand
                elif token == '*':
                    result = left_operand * right_operand
                elif token == '/':
                    if right_operand == 0:
                        raise ZeroDivisionError("Division by zero")
                    result = left_operand / right_operand
                stack.push(result)
            except IndexError:
                raise IndexError("Insufficient operands in expression")

    if stack.is_empty():
        raise ValueError("The expression is invalid")
    
    return stack.pop()

# Example usage
try:
    expression = "3 4 + 2 * 7 /"  # ((3 + 4) * 2) / 7
    print(f"Result of '{expression}' is: {evaluate_postfix(expression)}")
except Exception as e:
    print(f"Error: {e}")
```

### 3. Explanation
- **Stack Class**: We define a `Stack` class to manage our stack operations. It includes methods for pushing, popping, peeking, and checking if the stack is empty.
- **evaluate_postfix Function**: This function takes a postfix expression as input and evaluates it using the stack.
  - We iterate through each token in the expression.
  - If the token is an operand (not an operator), we convert it to an integer and push it onto the stack.
  - If the token is an operator, we pop the top two operands from the stack, perform the operation, and push the result back onto the stack.
  - Error handling ensures that we catch invalid tokens and handle division by zero appropriately.
- **Final Result**: At the end of evaluation, we check that there is exactly one item left on the stack, which represents the final result of the expression.

This implementation showcases how stacks can efficiently manage operations that require strict ordering, a common requirement in Robotics where control algorithms often rely on evaluating complex mathematical expressions quickly.

### 4. Application
In Robotics, stacks can be used to evaluate expressions in control algorithms that dictate how robots should respond to sensor inputs. For example, a robotic arm might use postfix expressions to compute angles and movements based on real-time data from its environment. 

In semiconductors, stacks can assist in parsing and evaluating configurations for circuit designs or signal processing algorithms. By efficiently managing these calculations, systems can operate faster and with higher accuracy.

In consumer electronics, stacks are crucial in applications like calculators or any device that requires mathematical computation. They enable efficient evaluation of user-inputted expressions, enhancing user experience through quick responses.

### Integration
This content is structured to facilitate easy integration into learning platforms. Each section is clearly defined with headings for straightforward navigation. The use of markdown ensures proper formatting for clarity and readability, supporting learners as they work through complex concepts related to data structures.