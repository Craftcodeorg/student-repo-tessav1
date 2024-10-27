# Module Title: Algorithm Fundamentals 

## Exercise Requirements

### 1. Problem Statement:
Imagine you are working for a robotics company that develops intelligent robots capable of predicting the optimal paths for navigation. The Fibonacci sequence is often used in algorithms related to pathfinding and optimization. Your task is to write a recursive function that calculates the nth Fibonacci number, which will represent the number of unique paths a robot can take to reach its destination in a grid, based on the Fibonacci pattern.

### 2. Fill-in-the-Blank Starter Code:
Below is the starter code for implementing the Fibonacci sequence using recursion. Fill in the blanks to complete the function.

```python
# Starter code for implementing the Fibonacci sequence
def fibonacci(n):
    # Base case: if n is 0 or 1, return n
    if n <= 1:
        return _______  # Fill in the base case return value
    # Recursive case: return the sum of the two preceding numbers
    return fibonacci(n - 1) + fibonacci(n - 2)  # Recursive calls

# Test the function with an example value
n = _____  # Fill in the desired position in the Fibonacci sequence
print(f"The {n}th Fibonacci number is: {fibonacci(n)}")  # Expected output
```

### 3. Hints:
- **Hint 1**: Remember that the Fibonacci sequence starts with 0 and 1. Think about what values you should return when `n` is 0 or 1.
- **Hint 2**: Each Fibonacci number is the sum of the two preceding ones. Make sure your recursive function correctly reflects this relationship.
- **Hint 3**: Consider how you can test your function with different values of `n` to ensure it works correctly.

### 4. Expected Outcome:
The student should be able to fill in the blanks correctly, demonstrating an understanding of recursion and how it applies to solving problems related to pathfinding in robotics. The final solution should adhere to best practices, include error handling (e.g., checking if `n` is a non-negative integer), and be well-commented to explain the reasoning behind each step.

```python
# Completed code example after filling in the blanks
def fibonacci(n):
    # Base case: if n is 0 or 1, return n
    if n <= 1:
        return n  # Return n when it is 0 or 1
    # Recursive case: return the sum of the two preceding numbers
    return fibonacci(n - 1) + fibonacci(n - 2)  # Recursive calls

# Test the function with an example value
n = 5  # Example position in the Fibonacci sequence
print(f"The {n}th Fibonacci number is: {fibonacci(n)}")  # Expected output: The 5th Fibonacci number is: 5
```

### Integration
- Ensure that the exercise content is well-structured with clear headings and sections for easy parsing and integration into the learning platform.
- Use markdown for formatting and include any necessary files or resources as links.
- This exercise aligns with your career goals by promoting critical thinking and practical application of algorithmic concepts discussed in the lecture.