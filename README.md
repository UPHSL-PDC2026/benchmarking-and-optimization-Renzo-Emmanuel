[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23197667&assignment_repo_type=AssignmentRepo)
	
<img width="764" height="161" alt="image" src="https://github.com/user-attachments/assets/dbe1069a-0586-4f8f-b848-e0f5fee1ae87" />


# Github Repository Link
[https://github.com/UPHSL-PDC2026/benchmarking-and-optimization-Renzo-Emmanuel](https://github.com/UPHSL-PDC2026/benchmarking-and-optimization-Renzo-Emmanuel)


# STEP 8: Short Analysis (Written Output)

### 1. Which version was fastest?
The original sequential version was the fastest, with an execution time of approximately **0.67 seconds**. Surprisingly, both the parallel and optimized versions performed slower in this case.

### 2. What was the speedup achieved?
The speedup was **less than 1** since the parallel version (**1.99 seconds**) was slower than the original sequential version (**0.67 seconds**). This means there was no actual performance gain from parallelization.

### 3. Was efficiency high or low? Why?
The efficiency was **low** because the overhead of creating multiple processes, splitting the data, and combining the results outweighed the benefits of parallel execution. This is common when the task is not heavy enough to justify multiprocessing overhead.

### 4. What bottleneck did profiling reveal?
Profiling revealed that the main bottleneck was the loop inside the `compute_sum` function, where each element is processed sequentially, leading to high computation time.

---

### 5. How did optimization affect performance?
The optimization slightly improved code readability but did not significantly improve performance. In fact, the optimized version (**0.84 seconds**) was still slower than the original sequential version, likely due to generator expression overhead.
