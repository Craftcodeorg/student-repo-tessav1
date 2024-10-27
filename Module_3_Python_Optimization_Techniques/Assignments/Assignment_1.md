# Assignment: Optimize Python Script for Soccer Match Data Processing

## Problem Statement
As a member of a sports analytics team, you are tasked with optimizing a Python script that processes soccer match data to calculate the average goals scored by each player over a season. The current implementation is inefficient and takes too long to execute, especially when working with large datasets. Your goal is to apply the optimization techniques discussed in the lecture on performance bottlenecks to enhance the execution speed and efficiency of the script.

## Starter Code
Below is a basic framework for processing soccer match data. Your task is to optimize this code.

```python
import pandas as pd

# Sample data representing player statistics for each match
data = {
    'player': ['Player A', 'Player B', 'Player A', 'Player C', 'Player B', 'Player A', 'Player C'],
    'goals': [1, 0, 2, 1, 3, 0, 4]
}

# Function to calculate average goals per player
def calculate_average_goals(data):
    # Convert the data into a DataFrame
    df = pd.DataFrame(data)
    
    # Current inefficient method to calculate average goals
    average_goals = {}
    players = df['player'].unique()
    
    for player in players:
        total_goals = df[df['player'] == player]['goals'].sum()
        match_count = df[df['player'] == player]['goals'].count()
        average_goals[player] = total_goals / match_count if match_count > 0 else 0
    
    return average_goals

# Test the function with sample data
average_goals = calculate_average_goals(data)
print(average_goals)
```

## Detailed Instructions
1. **Step 1: Optimize Data Aggregation**
   - Modify the function to use `pandas` built-in group operations instead of looping through each player. This will significantly reduce the execution time.
   - Replace the loop that calculates total goals and match count with a single line that uses `groupby`.

2. **Step 2: Improve Code Readability**
   - Ensure that your code is clean and well-documented. Add comments explaining each part of your code, especially the new optimized sections.

3. **Step 3: Handle Edge Cases**
   - Ensure that your function handles cases where a player may not have any goals scored (e.g., if a player has no entries in the dataset).

4. **Step 4: Output Formatting**
   - Enhance the output to display not only the average goals but also the total goals scored by each player.

## Criteria for Success and Evaluation
- **Correctness**: The optimized function should correctly calculate the average goals per player.
- **Efficiency**: The execution time of your code should be significantly reduced compared to the original implementation.
- **Code Quality**: Your code should be clean, well-structured, and follow best practices. Proper variable naming and comments are essential.
- **Output Clarity**: The output should be user-friendly and clearly present both the average and total goals scored by each player.

### Success Criteria Example:
- The function correctly calculates the average goals per player using optimized methods.
- The code is clean, well-documented, and follows best practices.
- The output clearly shows both the average goals and total goals for each player.

By completing this assignment, you will practice applying performance optimization techniques in Python while working on a real-world problem relevant to sports analytics. This will enhance your skills in data structures and algorithms, aligning with your career goals in Robotics, semiconductors, and consumer electronics.