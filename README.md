#Introduction:
This repository contains code and documentation for analyzing the performance of multi-threaded matrix multiplication using Python's NumPy library and threading module. The primary focus is on understanding how the number of threads utilized affects the time taken for matrix multiplication and CPU usage.

##Methodology:

#Matrix Generation:
100 random matrices of size 1000x1000 are generated using NumPy's np.random.rand() function.
A constant matrix of size 1000x1000 is also created.
Matrix Multiplication:
The matrices are multiplied with the constant matrix using multi-threading.
The number of threads used varies from 1 to 8, allowing for comparison of performance with different levels of parallelism.
Each thread is assigned a portion of the total matrices to multiply, ensuring efficient parallel processing.
Time Measurement:
The time taken for each multiplication operation is recorded using the time.time() function before and after the operation.
This allows for accurate measurement of the performance of each threading configuration.
CPU Usage Monitoring:
CPU usage during the experiments is monitored using the psutil library.
This provides insight into how the CPU resources are utilized by the multi-threaded matrix multiplication process.

#Graph:
The graph titled "Time Taken vs Number of Threads" illustrates the relationship between the number of threads used for matrix multiplication and the time taken to complete the operation.
X-axis (Number of Threads): Indicates the number of threads used for matrix multiplication.
Y-axis (Time Taken): Represents the time taken to complete the matrix multiplication operation in seconds.
Trend: Generally, as the number of threads increases, the time taken to complete the operation decreases. However, beyond a certain point, the overhead of thread creation and management may outweigh the benefits of parallelism, leading to diminishing returns.
Optimal Number of Threads: The graph helps identify the optimal number of threads that provide the best balance between parallelism and overhead, resulting in the fastest execution time. This can vary depending on the hardware and the specific characteristics of the workload.
By analyzing the graph and CPU usage data, users can gain insights into the performance characteristics of multi-threaded matrix multiplication on their system and optimize their threading configuration accordingly.
Conclusion:
This analysis provides valuable insights into the performance of multi-threaded matrix multiplication, helping users optimize their threading configuration for improved efficiency. Further experimentation and analysis can be conducted to explore additional factors affecting performance.
