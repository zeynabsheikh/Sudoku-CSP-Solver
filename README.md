# Sudoku Solver (CSP-Based)

![Python](https://img.shields.io/badge/Language-Python%203.x-blue.svg)
![AI-Heuristics](https://img.shields.io/badge/Algorithm-CSP%20%2B%20MRV-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

A high-performance Sudoku solver implemented as a **Constraint Satisfaction Problem (CSP)**. This project leverages logical inference and intelligent search heuristics to solve puzzles ranging from "Easy" to "Very Hard" difficulty levels with minimal backtracking.

---

## 🚀 Key Features

* **AC-3 Algorithm:** Pre-processes the grid to ensure initial arc consistency, often solving simple puzzles without any branching.
* **Backtracking Search:** A recursive DFS approach to explore potential solutions systematically.
* **Forward Checking:** A look-ahead strategy that prunes the search tree by removing inconsistent values from neighbor domains.
* **MRV Heuristic:** Uses the *Minimum Remaining Values* (fail-first) strategy to pick the most constrained cells first, drastically reducing backtrack calls.

---

## 📊 Performance Results

The solver tracks **Backtrack Calls** and **Failures** to measure efficiency. Below are the results from the benchmark files:

| Difficulty | Backtrack Calls | Failures | Status |
| :--- | :---: | :---: | :---: |
| **Easy** | 1 | 0 | ✅ Solved |
| **Medium** | 1 | 0 | ✅ Solved |
| **Hard** | 434 | 368 | ✅ Solved |
| **Very Hard** | 70 | 0 | ✅ Solved |

---

## 🛠️ Methodology

The solver treats Sudoku as a CSP where:
1.  **Variables:** 81 individual cells on the grid.
2.  **Domains:** Digits $\{1, 2, \dots, 9\}$ for empty cells.
3.  **Constraints:** Each row, column, and $3 \times 3$ subgrid must contain unique values.

Every time a value is assigned, **Forward Checking** is triggered to update the domains of all affected neighbors. If a domain becomes empty, the algorithm immediately backtracks, avoiding useless search paths.

---

## 📂 Project Structure

* `solver.py`: The core implementation containing the CSP logic and AC-3.
* `data/`: Directory containing input Sudoku boards in `.txt` format.
* `Report.ipynb`: A detailed analysis and walkthrough of the results.
* `README.md`: Project documentation.

---

## 💻 Installation & Usage

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/YourUsername/Sudoku-CSP-Solver.git](https://github.com/YourUsername/Sudoku-CSP-Solver.git)
    cd Sudoku-CSP-Solver
    ```

2.  **Run the solver:**
    ```bash
    python solver.py
    ```

---

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
*Developed as part of an Artificial Intelligence Lab project.*
