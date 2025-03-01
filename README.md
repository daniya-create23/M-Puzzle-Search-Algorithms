Here is your **README.md** file for the **M-Puzzle Solver** with **BFS, DFS, and DFS with Revisit Check**:  

---

# **M-Puzzle Solver** 🧩🔍  

## **Overview**  
This project implements a **Sliding-Tile M-Puzzle Solver** using three search algorithms:  
✅ **Breadth-First Search (BFS)** – Guarantees the shortest path solution.  
✅ **Depth-First Search (DFS)** – Explores deeper nodes first.  
✅ **DFS with Revisit Check** – Avoids cycles by tracking visited states.  

The solver is designed for **3 ≤ n ≤ 6 puzzles** and supports **multiple random initial states**. The final state is the **standard sorted order**.  

---

## **Features**  
- 🔄 **Solves N-Puzzles (8-Puzzle, 15-Puzzle, 24-Puzzle, etc.)**  
- 📊 **Reports Initial & Final States**  
- 🔍 **Tracks Solution Depth & States Stored**  
- 🚀 **Optimized Search Strategies for Performance Comparison**  

---

## **Implementation Details**  

### **State Representation**  
Each puzzle state is stored as an **n×n 2D list**, where:  
- Tiles are represented by numbers `1` to `n²-1`.  
- `0` represents the **blank tile**.  
- Example **3×3 Initial State**:  
  ```python
  [1, 2, 3]
  [4, 5, 6]
  [7, 8, 0]  # '0' is the blank tile
  ```
- The goal state is the **sorted order** with `0` in the bottom-right corner.  

---

### **Operators & Actions**  
The blank tile (`0`) can move in four directions:  
- 🔼 **Up**  
- 🔽 **Down**  
- ◀️ **Left**  
- ▶️ **Right**  

Each move swaps `0` with an adjacent tile.  

---

## **Search Algorithms Implemented**  

### 🔵 **1. Breadth-First Search (BFS)**
- Uses a **queue (FIFO)** to explore the shallowest nodes first.  
- **Finds the optimal (shortest) solution** but requires high memory.  
- **Tracks**:  
  - **Solution Depth** (Minimum moves to reach goal).  
  - **Max States Stored** (Memory efficiency).  

#### **BFS Complexity**  
- **Time Complexity**: `O(b^d)` (Exponential).  
- **Space Complexity**: `O(b^d)`, where `b = 3` (branching factor), `d` = depth.  

---

### 🔴 **2. Depth-First Search (DFS)**
- Uses a **stack (LIFO)** to explore deeper paths first.  
- **May find non-optimal solutions** but is more memory-efficient.  
- **Avoids immediate reverses** (e.g., moving "Up" then "Down").  

#### **DFS Complexity**  
- **Time Complexity**: `O(b^d)`, but practical depth limit reduces expansion.  
- **Space Complexity**: `O(d)`, much lower than BFS.  

---

### 🟢 **3. DFS with Revisit Check**
- Same as **DFS** but **avoids revisiting states**.  
- Uses a **visited set** to prevent redundant explorations.  
- **Reduces cycles and improves efficiency.**  

#### **DFS-Revisit Complexity**  
- **Time Complexity**: `O(b^d)` but reduces duplicate paths.  
- **Space Complexity**: `O(d)` + `O(visited_states)`.  

---



## **Results & Performance Metrics**  

Each algorithm is run **10 times per puzzle size (`n = 3, 4, 5, 6`)**. The results include:  

📌 **Initial & Final States**  
📌 **Solution Sequence (Moves taken)**  
📌 **Solution Depth (Min, Max, Avg)**  
📌 **Max Memory Used (States stored concurrently)**  

✅ **BFS finds the shortest path but consumes high memory.**  
✅ **DFS is memory-efficient but may explore deep paths unnecessarily.**  
✅ **DFS-Revisit improves DFS by reducing unnecessary state revisits.**  

---

## **Future Improvements**  
🚀 Implement **A* Search Algorithm** for better performance.  
🚀 Add **Heuristic-Based Solvers** (Manhattan Distance, Linear Conflict).  
🚀 Optimize **state storage & memory usage**.  

---

## **Contributing**  
Want to improve this project? **Fork, submit pull requests, or suggest enhancements!**  

---

## **License**  
📜 This project is **open-source** and available for academic and research use.  

---

This README provides a **clear and structured overview** of your **M-Puzzle Solver** project. 🚀 Let me know if you need modifications!
