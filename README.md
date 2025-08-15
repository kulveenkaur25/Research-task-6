# Research Task 05 – Descriptive Statistics & LLM Evaluation

## Overview
This project is part of the Research Task 05 assignment, which involves:
- Generating descriptive and advanced summary statistics from the **2023 NFL season** dataset.
- Providing these summary statistics (without the original dataset) to a Large Language Model (LLM) such as ChatGPT.
- Asking both **basic** and **advanced** natural language questions to evaluate the accuracy of the LLM’s responses.
- Comparing the LLM’s answers against the **ground truth** values derived from the dataset.

The goal is to explore the capabilities and limitations of LLMs in understanding structured data and producing accurate outputs.

---

## Dataset
The original play-by-play dataset is **not** included in this repository due to submission guidelines.  
Instead, we used a **combined_summary_stats.csv** file containing:
- Aggregated season statistics (total games, touchdowns, averages, etc.).
- Advanced metrics (yards per play by half, red-zone efficiency, etc.).

---

## Questions Asked
The questions were divided into two categories:

### **Original 6 (Basic Descriptive Statistics)**
1. How many games were played in the 2023 season?
2. Which team scored the most touchdowns?
3. What was the average yards gained per play?
4. Which team had the most passing touchdowns?
5. If a coach wanted to win two more games next season, should they focus on offense or defense? Why?
6. Who was the most impactful player in the season based on touchdowns and yards?

### **Advanced 10 (Derived/Complex Statistics)**
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

---

## Evaluation Table

| Q#  | Question                                                                                     | Ground Truth Answer                       | LLM Answer                                 | Correct? | Notes                                         |
| --- | -------------------------------------------------------------------------------------------- | ------------------------------------------ | ------------------------------------------- | -------- | --------------------------------------------- |
| 1   | How many games were played in the 2023 season?                                                | 272                                        | 272                                         | ✅        | Matches exactly                              |
| 2   | Which team scored the most touchdowns?                                                       | MIA – 66 touchdowns                        | MIA – 66 touchdowns                         | ✅        | Matches exactly                              |
| 3   | What was the average yards gained per play?                                                   | 3.752140085                                 | 3.75                                        | ✅        | Rounded to two decimals                      |
| 4   | Which team had the most passing touchdowns?                                                   | DAL – 37 touchdowns                        | DAL – 37 touchdowns                         | ✅        | Matches exactly                              |
| 5   | Should focus be on offense or defense to win 2 more games?                                    | Defense (allow fewer yards per pass)       | Defense (allow fewer yards per pass)        | ✅        | Matches reasoning                            |
| 6   | Most impactful player based on TDs and yards?                                                 | Jason Pinnock – 102-yard INT TD             | Jason Pinnock – 102-yard INT TD              | ✅        | Matches exactly                              |
| 7   | Highest avg yards/play in wins?                                                               | None / N/A (no valid data)                  | None                                        | ✅        | Both report no valid data                    |
| 8   | Defense allowed fewest passing TDs?                                                           | HOU – 18                                   | HOU – 18                                    | ✅        | Matches exactly                              |
| 9   | Quarter with highest scoring rate?                                                            | Q5 – 0.029412                              | Q5 – 0.029412                               | ✅        | Matches exactly                              |
| 10  | Most improved team (yards/play from H1 to H2)?                                                 | ARI                                        | ARI                                         | ✅        | Matches exactly                              |
| 11  | Player with largest % of team TDs?                                                             | Breece Hall – 4.17%                        | Breece Hall – 4.17%                         | ✅        | Matches exactly                              |
| 12  | Reduce scoring by 20% – focus on rush or pass?                                                 | Pass (7.23 yds/att vs 4.46 rush)           | Pass (7.23 yds/att vs 4.46 rush)            | ✅        | Matches reasoning                            |
| 13  | Most efficient red-zone offense?                                                               | DET – 0.074132                             | DET – 0.074132                              | ✅        | Matches exactly                              |
| 14  | DAL passing TDs with +10% rate?                                                                | 40.7 TDs                                   | 41 TDs                                      | ✅        | Slight rounding difference                   |
| 15  | Most competitive matchup (avg yds/play)?                                                       | IND vs WAS                                 | IND vs WAS                                  | ✅        | Matches exactly                              |
| 16  | Best balanced team (rush vs pass)?                                                             | NYJ                                        | NYJ                                         | ✅        | Matches exactly                              |

---

## Key Insights
- **Accuracy:** All 16 answers matched the dataset-derived ground truth, with only minor rounding differences.
- **LLM Strengths:** Works well with clean, structured summary data for both basic and advanced stats.
- **LLM Limitations:** Requires explicit metric definitions for subjective terms like "impactful" or "competitive."

---

## Repository Structure

Task_05_Descriptive_Stats/
│
├── scripts/ # Python scripts for data processing
├── prompts/ # Prompt engineering examples for LLM
├── combined_summary_stats.csv # Summary statistics file (no raw data)
├── README.md # This file



---

## How to Reproduce
1. Prepare **summary statistics** from your dataset.
2. Create a set of **basic and advanced** questions.
3. Feed the statistics and questions to an LLM.
4. Record the answers and compare them against ground truth.
5. Document results in a comparison table (as shown above).

---

## Author
Kulveen Kaur – Syracuse University – Applied Data Science MS

