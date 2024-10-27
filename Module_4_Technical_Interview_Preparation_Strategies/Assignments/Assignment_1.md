# Assignment: Analyzing Player Performance Data for Technical Interviews

## Problem Statement
Create a function that analyzes player performance data for a soccer team (inspired by Premier League Soccer, such as Chelsea F.C.). The function should calculate the average score of players over a series of matches and identify any matches where a player's score exceeded the average by more than 10%. This task will help you apply the concepts of coding challenges discussed in the lecture, particularly focusing on data structures and algorithm optimization.

## Starter Code
Below is the starter code that sets up the environment for analyzing player scores. You will need to expand upon this code by implementing the required functionality.

```python
# Starter code for analyzing player performance scores

def analyze_player_scores(scores):
    # Step 1: Calculate the average score
    avg_score = sum(scores) / len(scores) if scores else 0
    
    # Step 2: Identify matches where the score exceeds the average by more than 10%
    high_performance_matches = []
    for index, score in enumerate(scores):
        if score > avg_score * 1.1:
            high_performance_matches.append((index + 1, score))  # Store match number and score
    
    # Return results (students will need to format the output)
    return avg_score, high_performance_matches

# Test the function with sample data
player_scores = [1, 0, 2, 1, 3]
average_score, standout_matches = analyze_player_scores(player_scores)
print(f"Average Score: {average_score}")
print(f"Matches Exceeding 10% Over Average: {standout_matches}")
```

## Detailed Instructions
1. **Step 1**: Modify the function to ensure it handles cases where the `scores` list is empty. Ensure that it returns an appropriate message or value when there are no scores to analyze.

2. **Step 2**: Enhance the output to provide more detailed feedback. Instead of just returning the average score and standout matches, format the output to include:
   - The average score rounded to two decimal places.
   - A list of match numbers and scores where the performance exceeded the average by more than 10%.

3. **Step 3**: Add comments to your code explaining what each part does, especially where you perform calculations or checks.

4. **Step 4**: Write unit tests for your function to verify that it behaves as expected with different inputs (e.g., all scores below average, some scores above average, and edge cases like an empty list).

## Criteria for Success and Evaluation
- **Accuracy**: The function correctly calculates the average score and identifies matches where the score exceeds the average by more than 10%.
- **Code Quality**: The code is clean, well-documented, and follows best practices, including meaningful variable names and appropriate comments.
- **Output Formatting**: The output is user-friendly, providing clear information about both the average score and standout matches.
- **Testing**: Unit tests are included that cover various scenarios to ensure the function's reliability.

This assignment will help reinforce your understanding of technical interview formats while allowing you to practice essential coding skills relevant to your career goals in Robotics, semiconductors, and consumer electronics. Happy coding!