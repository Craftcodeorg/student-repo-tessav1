# Module Title: Introduction to Data Structures

## Exercise Requirements

### 1. Problem Statement:
In this exercise, you will create a function that traverses a binary tree in pre-order. To contextualize this problem, imagine you are developing a system to analyze player formations and movements in a soccer match, specifically for Chelsea F.C. The tree structure will represent the hierarchy of players, where the root node represents the coach, and each subsequent level represents players in various positions. 

Your task is to write a function that visits each player (node) in the order of the hierarchy (pre-order traversal), which means you will first visit the coach, then the players in their respective positions. This exercise will help you understand how to manage hierarchical data structures, which is crucial in both coding interviews and real-world applications in robotics and semiconductors.

### 2. Fill-in-the-Blank Starter Code:
```python
class PlayerNode:
    def __init__(self, name):
        self.name = name
        self.left = None  # Represents one side player
        self.right = None  # Represents the other side player

def pre_order_traversal(node):
    # Base case: if the current node is None, return
    if node is None:
        return
    
    # Visit the current node (player)
    print(node.name)  # Fill in this blank with the correct action

    # Recursively traverse the left subtree
    pre_order_traversal(node.left)  # Fill in this blank with the correct recursive call

    # Recursively traverse the right subtree
    pre_order_traversal(node.right)  # Fill in this blank with the correct recursive call

# Example usage:
if __name__ == "__main__":
    # Creating a sample player hierarchy
    coach = PlayerNode("Coach")
    left_player = PlayerNode("Left Winger")
    right_player = PlayerNode("Right Winger")
    
    coach.left = left_player
    coach.right = right_player
    
    print("Pre-order traversal of player hierarchy:")
    pre_order_traversal(coach)  # Call your function here to test
```

### 3. Hints:
- **Hint 1**: Remember that in pre-order traversal, you first process the current node before moving to its children.
- **Hint 2**: Think about how you can represent each player's position as a node in the tree and how you would access them in the desired order.
- **Hint 3**: Use print statements to visualize which players are being visited during the traversal; this will help you debug your function.

### 4. Expected Outcome:
Upon completing this exercise, you should be able to:
- Fill in the blanks correctly to implement the pre-order traversal function.
- Demonstrate an understanding of how to traverse a binary tree and apply this concept to a real-world scenario related to your interests in soccer and technology.
- Produce well-commented code that explains your reasoning behind each step, showcasing best practices in coding.

This exercise will not only enhance your coding skills but also prepare you for technical interviews by solidifying your understanding of tree structures and their traversal methods.