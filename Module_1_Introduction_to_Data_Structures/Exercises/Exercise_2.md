### Module Title: Introduction to Data Structures ###

### Exercise Requirements ###

1. **Problem Statement**: 
   In the context of managing a soccer team, such as Chelsea F.C., you are tasked with creating a queue to manage player substitutions during a match. Each player can be enqueued (added) to the substitution list when they are ready to enter the game and dequeued (removed) when they are called onto the field. Your goal is to implement a queue data structure that allows you to perform these operations efficiently. 

   **Task**: Create a queue and implement the following operations:
   - Enqueue a player into the substitution queue.
   - Dequeue a player from the substitution queue.
   - Display the current players waiting to be substituted.

   This exercise will help you understand the FIFO principle of queues and how they can be applied in real-world scenarios, particularly in sports management.

2. **Fill-in-the-Blank Starter Code**:
```python
# Starter code for implementing a queue for player substitutions
class PlayerQueue:
    def __init__(self):
        # Initialize an empty list to represent the queue
        self.queue = []

    def enqueue(self, player):
        # Add a player to the end of the queue
        self.queue.append(player)
        print(f"{player} has been added to the substitution queue.")

    def dequeue(self):
        # Remove and return the player at the front of the queue
        if not self.is_empty():
            player = self.queue.pop(0)
            print(f"{player} has entered the game.")
            return player
        else:
            print("The substitution queue is empty.")
            return None

    def is_empty(self):
        # Check if the queue is empty
        return len(self.queue) == 0

    def display_queue(self):
        # Display players currently in the queue
        if self.is_empty():
            print("No players in the substitution queue.")
        else:
            print("Current substitution queue:", self.queue)

# Example usage of PlayerQueue
substitution_queue = PlayerQueue()

# Enqueue players into the substitution queue
substitution_queue.enqueue("Player A")  # Fill in this blank
substitution_queue.enqueue("Player B")  # Fill in this blank

# Display current players in the queue
substitution_queue.display_queue()

# Dequeue a player from the substitution queue
substitution_queue.dequeue()  # Fill in this blank
```

3. **Hints**:
   - Remember that a queue follows the First In First Out (FIFO) principle; the first player added should be the first one to enter the game.
   - Use the `append` method to add players to the end of the list and `pop(0)` to remove players from the front.
   - Make sure to handle cases where you try to dequeue from an empty queue gracefully.

4. **Expected Outcome**:
   By completing this exercise, you should be able to implement a basic queue data structure that effectively manages player substitutions. The final solution should demonstrate an understanding of how queues operate, include error handling for empty states, and be well-commented to clarify each step's purpose. This exercise will enhance your problem-solving skills and prepare you for technical coding interviews focused on data structures.

### Integration ###
- Ensure that all code snippets are properly formatted using markdown for clarity.
- Encourage students to test their implementation with various scenarios (e.g., adding multiple players, attempting to dequeue from an empty queue) to solidify their understanding of queues in practical applications.