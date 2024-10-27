### Assignment: Implementing a Linked List for Player Substitution Management in Soccer

#### Problem Statement:
In the context of managing player substitutions for a soccer team like Chelsea F.C., you are tasked with creating a linked list to represent the sequence of player substitutions during a match. Each node in the linked list will represent a substitution event, storing the player's name and the time of substitution. You will implement functions to insert new substitutions, delete substitutions, and search for specific substitutions by player name.

#### Starter Code:
```python
class Node:
    def __init__(self, player_name, substitution_time):
        self.player_name = player_name
        self.substitution_time = substitution_time
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None

    def insert(self, player_name, substitution_time):
        # Step 1: Implement the insertion logic
        new_node = Node(player_name, substitution_time)
        if not self.head:
            self.head = new_node
            return
        current = self.head
        while current.next:
            current = current.next
        current.next = new_node

    def delete(self, player_name):
        # Step 2: Implement the deletion logic
        if not self.head:
            return
        if self.head.player_name == player_name:
            self.head = self.head.next
            return
        current = self.head
        while current.next:
            if current.next.player_name == player_name:
                current.next = current.next.next
                return
            current = current.next

    def search(self, player_name):
        # Step 3: Implement the search logic
        current = self.head
        while current:
            if current.player_name == player_name:
                return f"Substitution found: {current.player_name} at {current.substitution_time}"
            current = current.next
        return "Player not found in substitutions"

# Test the linked list implementation
substitutions = LinkedList()
substitutions.insert("Player A", "45:00")
substitutions.insert("Player B", "60:00")
substitutions.insert("Player C", "75:00")

# Test searching for a substitution
print(substitutions.search("Player B"))  # Should find Player B

# Test deleting a substitution
substitutions.delete("Player A")
print(substitutions.search("Player A"))  # Should indicate Player A is not found
```

#### Detailed Instructions:
1. **Step 1: Implement the Insertion Logic**
   - Modify the `insert` method to allow for inserting substitutions at any point in the match. Consider allowing for insertion at the head or in sorted order based on time.

2. **Step 2: Implement the Deletion Logic**
   - Enhance the `delete` method to handle cases where a player may have multiple substitutions or to delete all instances of a player if needed.

3. **Step 3: Implement the Search Logic**
   - Modify the `search` method to not only find a player but also return all substitution times for that player in a formatted manner.

4. **Step 4: Testing and Validation**
   - Create test cases to validate your linked list implementation. Ensure that you test edge cases such as inserting at the head, deleting from an empty list, and searching for players who have not been substituted.

#### Criteria for Success and Evaluation:
- **Functionality**: The linked list should correctly handle insertions, deletions, and searches.
- **Code Quality**: The code should be clean, well-documented with comments explaining each part of the implementation.
- **User Feedback**: The output from search operations should be clear and informative, providing necessary details about substitutions.
- **Testing**: Include a set of test cases that cover various scenarios to ensure robustness.

This assignment will help you apply your knowledge of linked lists in a practical scenario relevant to soccer management while reinforcing your understanding of data structures and algorithms.