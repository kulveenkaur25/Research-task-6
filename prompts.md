# Prompts Used for Task 5 Analysis

This file contains the exact prompts used to generate the answers for Task 5, including both the original 6 questions and the advanced 10 questions.

---

## Prompt for Combined Summary Statistics Questions

**User Prompt:**
```
I have combined summary statistics from the 2023 NFL season. 
Here is the dataset:

[PASTE THE CONTENTS OF combined_summary_stats.csv HERE]

Using only this data, please answer the following 16 questions exactly and clearly:

Original 6:
1. How many games were played in the 2023 season?
2. Which team scored the most touchdowns?
3. What was the average yards gained per play?
4. Which team had the most passing touchdowns?
5. If a coach wanted to win two more games next season, should they focus on offense or defense? Why?
6. Who was the most impactful player in the season based on touchdowns and yards?

Advanced 10:
7. Which team had the highest average yards per play in games they won?
8. Which defense allowed the fewest passing touchdowns?
9. Which quarter had the highest scoring rate?
10. Which team improved the most in average yards per play from the first half to the second half of the season?
11. Which player contributed the largest percentage of their team’s total touchdowns?
12. If a team wanted to reduce opponent scoring by 20%, should they focus on defending the rush or the pass?
13. Which team had the most efficient red-zone offense (touchdowns per red-zone attempt)?
14. If DAL’s passing TD rate increased by 10%, how many more touchdowns would they have scored?
15. Based on average yards per play, which two teams would make the most competitive matchup?
16. Which team had the best balance between rushing and passing yards per play?

Return the answers in a table with these columns:
- Question Number
- LLM Answer
```

---

**Note:** All answers were generated strictly from the `combined_summary_stats.csv` file without using any external data.
