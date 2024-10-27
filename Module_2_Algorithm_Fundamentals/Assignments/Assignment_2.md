### Assignment: Implement a Search Function to Find Specific Players in a Database of Soccer Statistics

#### Problem Statement:
Create a function that searches for specific players in a database of soccer statistics. The function should take a list of player dictionaries and a player's name as input, returning the player's statistics if found, or an appropriate message if the player is not found. This task will help you apply the concepts of time complexity and Big O notation discussed in the lecture, particularly focusing on optimizing your search algorithm for efficiency.

#### Starter Code:
Below is a basic framework that you will build upon. The starter code includes a sample database of players and a placeholder function for your search implementation.

```python
# Sample database of players
players_database = [
    {"name": "Lionel Messi", "team": "Paris Saint-Germain", "goals": 672, "assists": 268},
    {"name": "Cristiano Ronaldo", "team": "Manchester United", "goals": 674, "assists": 229},
    {"name": "Neymar Jr", "team": "Paris Saint-Germain", "goals": 400, "assists": 200},
    {"name": "Kevin De Bruyne", "team": "Manchester City", "goals": 80, "assists": 130},
]

def search_player(players, player_name):
    # Step 1: Implement a search algorithm to find the player by name
    for player in players:  # O(n)
        if player["name"].lower() == player_name.lower():  # O(1)
            return player
    return None

# Test the function with a sample player name
result = search_player(players_database, "Lionel Messi")
if result:
    print(f"Player Found: {result}")
else:
    print("Player not found.")
```

#### Detailed Instructions:
1. **Implement the Search Logic**: 
   - Modify the `search_player` function to implement an efficient search algorithm. Consider using a binary search if the list is sorted by player names or stick with linear search for simplicity.
   - Ensure that your function can handle case insensitivity (e.g., "Lionel Messi" should match "lionel messi").

2. **Return Player Statistics**: 
   - If the player is found, return their statistics as a dictionary.
   - If not found, return a message indicating that the player does not exist in the database.

3. **Optimize Your Code**: 
   - After implementing the basic search, analyze its time complexity. If you used linear search (O(n)), consider how you could improve this if you had a larger dataset.
   - Discuss potential optimizations in comments within your code.

4. **Format Output**: 
   - Ensure that the output is user-friendly. If the player is found, format the statistics in a readable way.

#### Criteria for Success and Evaluation:
- **Functionality**: The function correctly finds and returns player statistics or an appropriate message.
- **Time Complexity**: You should comment on the time complexity of your search method (O(n) for linear search; O(log n) for binary search).
- **Code Quality**: The code should be clean, well-organized, and follow best practices (e.g., meaningful variable names, proper indentation).
- **User Experience**: The output should be formatted clearly and be easy to understand.

By completing this assignment, you will reinforce your understanding of time complexity and apply it to a practical scenario relevant to your interests in soccer and technology. Good luck!