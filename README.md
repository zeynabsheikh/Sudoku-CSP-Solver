# Sudoku Solver: A Constraint Satisfaction Problem Approach

## Project Overview
This project was developed as part of the **Artificial Intelligence Lab** to demonstrate the efficiency of **Constraint Satisfaction Problem (CSP)** techniques in solving combinatorial puzzles. The solver efficiently handles Sudoku boards of various difficulties using a Jupyter Notebook implementation.

---

## Core Algorithms & Heuristics

To optimize the search process and minimize computational overhead, the following strategies were implemented:

1. **AC-3 (Arc Consistency):** Acts as a powerful preprocessing step that ensures every cell's possible values (domain) are consistent with its neighbors.
2. **Backtracking Search:** A recursive depth-first algorithm used to explore potential digit assignments systematically.
3. **Forward Checking:** A look-ahead strategy that dynamically prunes the search space by removing inconsistent values from neighbors' domains.
4. **MRV (Minimum Remaining Values) Heuristic:** Prioritizes cells with the smallest remaining domain to reduce the branching factor of the search tree.

---

##  Experimental Results

The solver was tested against the provided benchmark boards (`easy.txt`, `medium.txt`, `hard.txt`, and `veryhard.txt`). Based on the performance metrics:

| Difficulty Level | Backtrack Calls | Failure Count | Solution Status |
| :--- | :---: | :---: | :---: |
| **Easy** | 1 | 0 | ✅ Solved |
| **Medium** | 1 | 0 | ✅ Solved |
| **Hard** | 412 | 346 | ✅ Solved |
| **Very Hard** | 97 | 27 | ✅ Solved |

---

##  Project Structure

* `F23-0545_AI_Ass_05.ipynb`: The main Jupyter Notebook containing the CSP implementation and logic.
* `easy.txt`, `medium.txt`, `hard.txt`, `veryhard.txt`: Input Sudoku puzzles used for testing.
* `README.md`: Project documentation and performance report.

---

##  How to Run

1. **Clone the project:**
   ```bash
   git clone [https://github.com/zeynabsheikh/Sudoku-Solver.git](https://github.com/zeynabsheikh/Sudoku-Solver.git)

2. **Open the Notebook:**
   * `Launch Jupyter Notebook or Google Colab and open F23-0545_AI_Ass_05.ipynb to execute the solver.
