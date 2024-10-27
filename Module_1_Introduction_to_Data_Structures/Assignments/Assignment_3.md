# Assignment: Building a Binary Search Tree for Player Statistics Analysis

### Problem Statement
In the context of Premier League Soccer, you are tasked with creating a binary search tree (BST) to manage player statistics for Chelsea F.C. This BST will allow you to efficiently insert, delete, and traverse player statistics based on their performance metrics such as goals scored or assists made. Your goal is to implement methods for insertion, deletion, and traversal of the BST to analyze player performance data effectively.

### Starter Code
Below is a basic framework for your binary search tree. You will need to expand upon this code by implementing the necessary methods for insertion, deletion, and traversal.

```python
class Node:
    def __init__(self, key):
        self.left = None
        self.right = None
        self.val = key

class BinarySearchTree:
    def __init__(self):
        self.root = None

    def insert(self, root, key):
        # TODO: Implement the insertion logic
        pass

    def delete(self, root, key):
        # TODO: Implement the deletion logic
        pass

    def inorder_traversal(self, root):
        # TODO: Implement inorder traversal logic
        pass

    def preorder_traversal(self, root):
        # TODO: Implement preorder traversal logic
        pass

    def postorder_traversal(self, root):
        # TODO: Implement postorder traversal logic
        pass

# Sample usage
bst = BinarySearchTree()
# Add sample player statistics here
```

### Detailed Instructions
1. **Insertion Method**:
   - Implement the `insert` method to add a new node to the BST. Ensure that the left child contains values less than the parent node and the right child contains values greater.
   - Example of how to call this method after creating a new player statistic:
     ```python
     bst.root = bst.insert(bst.root, player_statistic)
     ```

2. **Deletion Method**:
   - Implement the `delete` method to remove a node from the BST. Ensure that when deleting a node with two children, you find the in-order predecessor or successor to maintain the BST properties.

3. **Traversal Methods**:
   - Implement three traversal methods: `inorder_traversal`, `preorder_traversal`, and `postorder_traversal`. Each method should return a list of values in the respective order.
   - Use these methods to print player statistics in different orders. For example:
     ```python
     print("Inorder Traversal:", bst.inorder_traversal(bst.root))
     ```

4. **Testing**:
   - After implementing your methods, create sample player statistics (e.g., goals scored) and test your BST implementation by inserting, deleting, and traversing these statistics.

### Criteria for Success and Evaluation
- **Correctness**: The BST must correctly implement insertion, deletion, and traversal methods.
- **Code Quality**: Code should be clean, well-documented, and follow best practices for readability and maintainability.
- **Functionality**: The output from traversal methods should accurately reflect the player statistics stored in the BST.
- **Efficiency**: The implementation should demonstrate an understanding of BST properties and operations.

### Submission Guidelines
- Submit your completed code as a single Python file.
- Include comments explaining your thought process and any challenges you faced during implementation.
- Ensure that your code runs without errors and produces expected results when tested with sample data.

This assignment will enhance your understanding of binary search trees and their practical applications in managing hierarchical data structures like player statistics in sports. Good luck!