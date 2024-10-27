# Module Title: Introduction to Data Structures

## Example 2: Creating a Linked List

### 1. Introduction
Creating a linked list is a fundamental concept in data structures that allows for dynamic memory allocation and efficient insertions and deletions. In the context of Robotics, semiconductors, and consumer electronics, linked lists can be used to manage data streams, sensor readings, and control signals that require real-time processing. This example builds upon the key concepts from the lecture on types of data structures, specifically focusing on linked lists' characteristics and applications.

### 2. Code Snippet
Here is a well-commented Python code snippet that demonstrates how to create a simple linked list. This code includes error handling and best practices suitable for an intermediate-level programmer.

```python
class Node:
    """Class to represent a single node in a linked list."""
    def __init__(self, data):
        self.data = data  # Store the data
        self.next = None  # Initialize the next pointer to None

class LinkedList:
    """Class to represent the linked list."""
    def __init__(self):
        self.head = None  # Initialize the head of the list

    def append(self, data):
        """Append a new node with the given data to the end of the list."""
        new_node = Node(data)  # Create a new node
        if not self.head:
            self.head = new_node  # If list is empty, set new node as head
            return
        last_node = self.head
        while last_node.next:  # Traverse to the last node
            last_node = last_node.next
        last_node.next = new_node  # Link the new node

    def display(self):
        """Display the contents of the linked list."""
        current_node = self.head
        while current_node:
            print(current_node.data, end=" -> ")
            current_node = current_node.next
        print("None")  # Indicate end of the list

# Example usage
if __name__ == "__main__":
    ll = LinkedList()
    ll.append(10)
    ll.append(20)
    ll.append(30)
    ll.display()  # Output: 10 -> 20 -> 30 -> None
```

### 3. Explanation
- **Node Class**: This class represents each element in the linked list. It contains two attributes: `data` (to store the value) and `next` (a pointer to the next node).
  
- **LinkedList Class**: This class manages the linked list. It has a `head` attribute that points to the first node in the list.

- **append Method**: This method adds a new node to the end of the linked list. It checks if the list is empty; if so, it sets the new node as the head. If not, it traverses to the last node and links it to the new node.

- **display Method**: This method prints all elements in the linked list, providing a visual representation of its contents.

The code effectively implements key concepts from the lecture by demonstrating how to create and manipulate a linked list. The use of classes encapsulates data and functionality, adhering to best practices in object-oriented programming.

### 4. Application
In Robotics, linked lists can be used to manage real-time data from various sensors. For example, consider a robotic arm that needs to process input from multiple sensors (temperature, pressure, position). Each sensor's reading can be stored in a linked list where each node represents a sensor's data point. 

This approach allows:
- **Dynamic Sizing**: New sensors can be added without needing to pre-allocate memory.
- **Efficient Insertions/Deletions**: If a sensor is removed or added, only pointers need to be updated, making it efficient compared to arrays.
- **Real-Time Processing**: The linked list can be traversed quickly to retrieve sensor readings for immediate processing, which is crucial in robotics where timely responses are necessary.

By mastering linked lists, you will enhance your problem-solving skills and prepare effectively for technical coding interviews in high-level tech positions within your industry.