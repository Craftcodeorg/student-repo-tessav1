# Assignment: Real-Time Player Statistics Tracker

### Problem Statement:
Develop a Python application that tracks player statistics for a soccer team (e.g., Chelsea F.C.) in real-time. The application should utilize optimized data structures to store player information and statistics efficiently. Key functionalities should include adding new player statistics, updating existing statistics, and calculating average performance metrics such as goals per match. This assignment will help you apply the concepts of built-in functions and libraries discussed in the lecture, particularly in data manipulation using Pandas.

### Starter Code:
Below is a basic framework for your application. You will need to expand upon this code to meet the assignment requirements.

```python
import pandas as pd

class PlayerStatistics:
    def __init__(self):
        # Initialize an empty DataFrame to hold player statistics
        self.stats = pd.DataFrame(columns=['Player', 'Goals', 'Matches'])

    def add_player(self, player_name, goals, matches):
        # Step 1: Add a new player with their statistics
        new_player = pd.DataFrame({'Player': [player_name], 'Goals': [goals], 'Matches': [matches]})
        self.stats = pd.concat([self.stats, new_player], ignore_index=True)

    def update_stats(self, player_name, goals, matches):
        # Step 2: Update the statistics for an existing player
        if player_name in self.stats['Player'].values:
            self.stats.loc[self.stats['Player'] == player_name, 'Goals'] += goals
            self.stats.loc[self.stats['Player'] == player_name, 'Matches'] += matches
        else:
            print(f"Player {player_name} not found!")

    def calculate_average_goals(self):
        # Step 3: Calculate and return the average goals per match for all players
        if not self.stats.empty:
            self.stats['Average Goals'] = self.stats['Goals'] / self.stats['Matches']
            return self.stats[['Player', 'Average Goals']]
        else:
            return "No player statistics available."

# Example usage
team_stats = PlayerStatistics()
team_stats.add_player('Player A', 10, 20)
team_stats.add_player('Player B', 15, 25)
team_stats.update_stats('Player A', 5, 5)

# Calculate and display average goals per match
average_goals = team_stats.calculate_average_goals()
print(average_goals)
```

### Detailed Instructions:
1. **Step 1: Add Player Functionality**
   - Implement the `add_player` method to allow adding players with their initial goals and matches. Ensure that the method checks for duplicate players and handles them appropriately.

2. **Step 2: Update Statistics**
   - Modify the `update_stats` method to allow updating a player's goals and matches. If a player does not exist in the DataFrame, inform the user.

3. **Step 3: Average Goals Calculation**
   - Enhance the `calculate_average_goals` method to calculate average goals per match accurately. Include error handling for cases where there are no players in the DataFrame.

4. **Step 4: User Interface**
   - Create a simple text-based interface that allows users to add players, update statistics, and display average goals per match interactively.

5. **Step 5: Testing**
   - Test your application with different scenarios, including adding multiple players, updating statistics for existing players, and checking average calculations.

### Criteria for Success and Evaluation:
- **Functionality**: The application must correctly add players, update their statistics, and calculate averages.
- **Code Quality**: The code should be clean, well-structured, and follow best practices for readability.
- **Documentation**: Include comments explaining each method's purpose and any complex logic.
- **User Experience**: The interface should be intuitive and provide clear feedback to the user.

**Success Criteria:**
- The application correctly handles player additions and updates.
- Average goals are calculated accurately.
- Code is well-documented and easy to understand.
- User interface is functional and user-friendly.

This assignment will reinforce your understanding of Python optimization techniques while providing practical experience relevant to your career goals in robotics and consumer electronics.