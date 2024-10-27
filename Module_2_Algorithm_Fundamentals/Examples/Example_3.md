# Module Title: Algorithm Fundamentals

## Example 3: Recursive Function for Factorial Calculation

### 1. Introduction
The concept of a recursive function for factorial calculation is a fundamental example that illustrates the principles of recursion, a key concept in algorithms. In the context of the lecture on sorting and searching algorithms, understanding recursion enhances problem-solving skills, particularly when dealing with complex data structures and algorithmic challenges. 

In fields such as robotics, semiconductors, and consumer electronics, recursion can be applied to optimize various processes, such as navigating decision trees or processing nested data structures. For instance, calculating the factorial of a number can be a building block for more complex algorithms used in robotics for pathfinding or optimization problems.

### 2. Code Snippet
Here is a well-commented Python code snippet that demonstrates a recursive function to calculate the factorial of a number, incorporating error handling and best practices:

```python
def factorial(n):
    """
    Calculate the factorial of a non-negative integer n using recursion.

    Parameters:
    n (int): A non-negative integer whose factorial is to be calculated.

    Returns:
    int: The factorial of n.

    Raises:
    ValueError: If n is negative.
    """
    # Error handling for negative input
    if n < 0:
        raise ValueError("Factorial is not defined for negative numbers.")
    
    # Base case: factorial of 0 or 1 is 1
    if n == 0 or n == 1:
        return 1
    
    # Recursive case
    return n * factorial(n - 1)

# Example usage
try:
    number = 5
    result = factorial(number)
    print(f"The factorial of {number} is {result}.")  # Output: The factorial of 5 is 120.
except ValueError as e:
    print(e)
```

### 3. Explanation
This code implements the recursive approach to calculate the factorial of a non-negative integer `n`. Here’s a step-by-step breakdown:

- **Function Definition**: The function `factorial(n)` takes an integer `n` as input.
- **Error Handling**: It checks if `n` is negative and raises a `ValueError` if so, ensuring that the function only processes valid inputs.
- **Base Case**: The base case checks if `n` is either `0` or `1`, returning `1` since the factorial of both these numbers is `1`.
- **Recursive Case**: If `n` is greater than `1`, the function calls itself with the argument `n - 1`. This continues until it reaches the base case, effectively breaking down the problem into smaller subproblems.
- **Example Usage**: The function is called with a sample input (`5`), and the result is printed.

This implementation showcases recursion, which is significant in various applications within robotics and electronics. For instance, in robotics, recursive algorithms can be used to navigate through different states or configurations efficiently.

### 4. Application
A real-world application of the recursive factorial calculation can be found in robotics, particularly in algorithms that require combinatorial calculations. For example, when programming a robot to explore a maze, it might need to calculate the number of possible paths from one point to another. Using recursion allows the robot to explore each path systematically while backtracking upon reaching dead ends.

In semiconductor design, recursive algorithms can help optimize circuit layouts by evaluating multiple configurations to find the most efficient design. Similarly, in consumer electronics, recursive functions can enhance data processing tasks, such as parsing nested JSON data structures commonly found in APIs.

### Integration
This content is structured to facilitate easy integration into your learning platform. Each section is clearly defined with headings, and the use of markdown formatting enhances readability. By mastering recursive functions like the factorial calculation, you will build a strong foundation for tackling more complex algorithmic challenges relevant to your career goals in tech. 

Through hands-on coding challenges and mock interviews focused on these concepts, you will gain confidence in solving technical problems and excelling in coding interviews at top tech companies.