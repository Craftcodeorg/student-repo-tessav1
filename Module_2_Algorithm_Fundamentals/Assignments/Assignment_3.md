# Assignment: Optimizing Game Strategies in Valorant Using Backtracking Techniques

## Problem Statement:
In the competitive game Valorant, players often need to devise strategies that involve choosing the optimal sequence of actions to outmaneuver opponents. Your task is to design an algorithm that utilizes backtracking techniques to optimize a player's strategy based on a set of possible actions and their outcomes. The algorithm should evaluate all potential action sequences and select the one that maximizes the chances of winning the round.

## Starter Code:
Below is a basic framework for your algorithm. You will need to implement the backtracking logic to explore all possible action sequences.

```python
# Starter code for optimizing game strategies in Valorant

def maximize_strategy(actions, current_strategy=[], best_strategy=None, best_outcome=0):
    """
    Function to find the best strategy using backtracking.
    
    Parameters:
    actions (list): A list of possible actions.
    current_strategy (list): The current sequence of actions being evaluated.
    best_strategy (list): The best strategy found so far.
    best_outcome (int): The best outcome score for the best strategy found.
    
    Returns:
    tuple: The best strategy and its outcome score.
    """
    
    # Base case: Evaluate the current strategy's outcome
    current_outcome = evaluate_strategy(current_strategy)
    
    # Check if the current strategy is better than the best found so far
    if current_outcome > best_outcome:
        best_outcome = current_outcome
        best_strategy = current_strategy.copy()
    
    # Explore further actions
    for action in actions:
        # Include the action in the current strategy
        current_strategy.append(action)
        
        # Recur with the updated strategy
        best_strategy, best_outcome = maximize_strategy(actions, current_strategy, best_strategy, best_outcome)
        
        # Backtrack: remove the last action added
        current_strategy.pop()
    
    return best_strategy, best_outcome

def evaluate_strategy(strategy):
    """
    A mock function to evaluate the outcome of a given strategy.
    
    Parameters:
    strategy (list): The sequence of actions taken.
    
    Returns:
    int: A score representing the outcome of the strategy.
    """
    # This is a placeholder. Replace with your actual evaluation logic.
    return sum(action['score'] for action in strategy)

# Example usage
actions = [{'name': 'Action1', 'score': 10}, {'name': 'Action2', 'score': 20}, {'name': 'Action3', 'score': 15}]
best_strategy, best_outcome = maximize_strategy(actions)
print(f"Best Strategy: {best_strategy}, Outcome Score: {best_outcome}")
```

## Detailed Instructions:
1. **Implement the `evaluate_strategy` function**: This function should take a list of actions (the current strategy) and return a score based on how effective that strategy is. You can use any scoring mechanism relevant to Valorant gameplay.

2. **Modify the `maximize_strategy` function**:
   - Ensure it correctly implements backtracking by exploring all combinations of actions.
   - Keep track of the best strategy and its corresponding outcome score throughout the recursive calls.

3. **Enhance the output**: After finding the best strategy, print it in a user-friendly format that includes each action's name and score.

4. **Test with different action sets**: Create various scenarios with different action sets to validate your algorithm's effectiveness in finding optimal strategies.

## Criteria for Success and Evaluation:
- **Functionality**: The algorithm must correctly identify the optimal strategy based on the defined scoring system.
- **Code Quality**: Your code should be clean, well-structured, and include comments explaining key sections.
- **User Output**: The output must clearly present the best strategy and its score in an easy-to-read format.
- **Testing**: Include test cases with diverse action sets to demonstrate the robustness of your solution.

By completing this assignment, you will gain practical experience in applying backtracking techniques to solve complex problems, enhancing your skills in algorithm design and optimization within a gaming context.