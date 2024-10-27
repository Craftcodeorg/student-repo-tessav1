# Assignment: Sorting Soccer Players by Statistics

## Problem Statement
Create a program that sorts a list of soccer players based on their statistics, such as goals scored, assists, and minutes played. The program should implement various sorting algorithms discussed in the lecture, allowing you to analyze the performance of players effectively. This task is relevant to data analytics in sports, particularly in understanding player contributions and optimizing team strategies.

## Starter Code
Below is a basic framework for your program. You will need to expand upon this code to implement the sorting algorithms and complete the functionality.

```python
# Starter code for sorting soccer players by statistics

# Define a class to represent a soccer player
class SoccerPlayer:
    def __init__(self, name, goals, assists, minutes_played):
        self.name = name
        self.goals = goals
        self.assists = assists
        self.minutes_played = minutes_played

    def __repr__(self):
        return f"{self.name}: Goals={self.goals}, Assists={self.assists}, Minutes={self.minutes_played}"

# Sample data: list of soccer players
players = [
    SoccerPlayer("Player A", 10, 5, 900),
    SoccerPlayer("Player B", 15, 7, 1200),
    SoccerPlayer("Player C", 8, 10, 800),
]

# Step 1: Implement sorting algorithms here
def bubble_sort(players):
    n = len(players)
    for i in range(n):
        for j in range(0, n-i-1):
            if players[j].goals < players[j+1].goals:  # Sort by goals scored (descending)
                players[j], players[j+1] = players[j+1], players[j]
    return players

# Step 2: Test the sorting function
sorted_players = bubble_sort(players)
print("Sorted Players by Goals:")
for player in sorted_players:
    print(player)
```

## Detailed Instructions
1. **Implement Additional Sorting Algorithms**: 
   - In addition to the bubble sort provided, implement at least one more sorting algorithm (e.g., QuickSort or MergeSort) in the same format. Ensure that your new sorting function allows sorting by different player statistics (goals, assists, or minutes played).
   
2. **Modify the Output**: 
   - Enhance the output to display sorted players based on different statistics. Create a function that takes a statistic as an argument and sorts the players accordingly. 

3. **User Interaction**: 
   - Add a simple user interface (CLI) that allows users to choose which statistic to sort by (goals, assists, minutes played). Based on user input, call the appropriate sorting function and display the sorted list.

4. **Code Documentation**: 
   - Ensure that your code is well-documented with comments explaining the purpose of each function and key sections of your code. This will help others understand your logic and approach.

## Criteria for Success and Evaluation
- **Functionality**: The program must correctly sort players based on the chosen statistic and display them in descending order.
- **Code Quality**: The code should be clean, well-structured, and follow best practices for readability and maintainability.
- **User Interaction**: The user interface should be intuitive and allow for seamless interaction.
- **Documentation**: Code should be adequately commented to explain logic and functionality.

### Success Criteria:
- The program accurately sorts and displays players based on user-selected statistics.
- The implementation of multiple sorting algorithms is correct and efficient.
- The code is clean, with meaningful variable names and comprehensive documentation.

This assignment will help you apply the concepts learned in the lecture while engaging with a real-world scenario relevant to data analysis in sports. Good luck!