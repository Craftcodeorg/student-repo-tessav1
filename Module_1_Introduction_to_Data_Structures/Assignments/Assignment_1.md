# Assignment: Simulating a Ticket Booking System Using Queues

## Problem Statement
In this assignment, you will develop a program that simulates a ticket booking system for a popular event, such as a concert or a sports match. The system will utilize a queue data structure to manage customer requests for tickets. This task will allow you to apply the concepts of queues and their significance in managing data efficiently, as discussed in the lecture on data structures.

### Key Requirements:
- Implement a queue to handle customer ticket requests.
- Each customer should be represented by a unique ID and the number of tickets they wish to purchase.
- The system should process requests in a first-come, first-served manner.

## Starter Code
Below is the starter code that sets up the basic structure for your ticket booking system. You will need to expand upon this code by implementing the queue operations and the logic for processing ticket requests.

```python
class Customer:
    def __init__(self, customer_id, tickets_requested):
        self.customer_id = customer_id
        self.tickets_requested = tickets_requested

class TicketBookingQueue:
    def __init__(self):
        self.queue = []

    def add_customer(self, customer):
        # Step 1: Add a customer to the queue
        self.queue.append(customer)

    def process_request(self):
        # Step 2: Process the next customer in the queue
        if self.queue:
            customer = self.queue.pop(0)  # Remove the first customer
            print(f"Processing request for Customer ID: {customer.customer_id}, Tickets Requested: {customer.tickets_requested}")
            # You can add logic here to check if tickets are available
        else:
            print("No customers in the queue.")

# Example usage
booking_queue = TicketBookingQueue()

# Adding customers to the queue
booking_queue.add_customer(Customer(1, 2))
booking_queue.add_customer(Customer(2, 4))

# Processing customer requests
booking_queue.process_request()
booking_queue.process_request()
booking_queue.process_request()  # This should indicate that there are no customers left.
```

## Detailed Instructions
1. **Implement Queue Functionality**:
   - Complete the `add_customer` method to ensure it adds customers to the end of the queue.
   - Complete the `process_request` method to remove and process the first customer in the queue. If there are no customers, print an appropriate message.

2. **Enhance Customer Processing**:
   - After processing a customer's request, implement logic to check if the requested number of tickets is available (you can simulate this with a fixed number of available tickets).
   - If tickets are available, reduce the available ticket count and confirm the booking. If not, inform the customer that their request cannot be fulfilled.

3. **Add Additional Features**:
   - Implement a method to display the current queue status (i.e., list all customers waiting in line).
   - Add error handling for invalid ticket requests (e.g., negative numbers or zero).

4. **Testing**:
   - Create multiple instances of `Customer` with varying ticket requests and test your queue system thoroughly.
   - Ensure that your system handles edge cases, such as when customers request more tickets than are available.

## Criteria for Success and Evaluation
- **Functionality**: The program should correctly manage customer requests using a queue and process them in order.
- **Code Quality**: The code should be clean, well-documented, and follow best practices for readability and maintainability.
- **User Experience**: The output should be clear and informative, guiding users through the ticket booking process.
- **Error Handling**: The program should handle invalid inputs gracefully without crashing.

### Success Criteria:
- The queue correctly adds and processes customers.
- The booking logic accurately reflects ticket availability.
- The code is well-organized and easy to follow.
- All edge cases are handled appropriately.

By completing this assignment, you will gain hands-on experience with queues, reinforcing your understanding of data structures and their applications in real-world scenarios. Good luck!