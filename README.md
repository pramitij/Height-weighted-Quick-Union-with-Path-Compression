# Height-weighted-Quick-Union-with-Path-Compression

>This assignment aimed to implement an advanced union-find structure, specifically a height-weighted Quick Union with Path Compression (UF_HWQUPC). The primary focus was on enhancing the efficiency of dynamic connectivity among a set of elements through intelligent tree structuring and path compression during the union and find operations.

## Implementation Details
Height-weighted Quick Union with Path Compression (UF_HWQUPC): The core of this assignment involved enhancing the union-find data structure to optimize performance for large datasets. The key strategies employed were:

- **Height-weighting**: Ensures that, during a union operation, the shorter tree is always attached to the root of the taller tree. This approach minimizes the overall height of the union-find tree, ensuring that find operations are more efficient.
- **Path Compression**: During find operations, the path from each visited node to the root is compressed, directly linking each node to the root. This drastically reduces the path length for subsequent find operations, enhancing efficiency.

### I successfully implemented these strategies in the UF_HWQUPC class, ensuring that all unit tests passed, indicating the correctness and robustness of the implementation.

### UF_Client
A Union-Find client was developed to utilize the UF_HWQUPC implementation. The client's goal was to connect random pairs of integers between 0 and n-1, where n is the number of sites. For each pair, the client checks if they are connected and performs a union operation if they are not. This process repeats until all sites are connected, and the total number of connections made is recorded. The client is encapsulated in a static method count() that accepts an integer n and returns the total number of connections. A main method takes the command-line input for n, calls count(), and prints the returned value.

## Performance Analysis and Observations
The assignment also included an analysis of the relationship between the number of objects (n) and the number of pairs generated (m) to connect all sites. My findings, supported by extensive experimentation, indicated a linear relationship between the number of objects and the number of pairs required for complete connectivity. The empirical relationship determined from the experiments can be succinctly expressed as:

    ``` latex
        M = 1.2 \cdot N \log N

This formula was derived from plotting the experimental data and fitting a curve that best described the relationship between N and M. The coefficient 1.2 was obtained through this curve-fitting process, highlighting the efficiency of the height-weighted Quick Union with Path Compression in reducing the total number of operations required to achieve full connectivity.

## Conclusion
The implementation of the UF_HWQUPC class and the UF_Client demonstrated the effectiveness of height-weighting and path compression in optimizing the performance of union-find operations. The performance analysis provided a quantitative understanding of the algorithm's scalability, reaffirming its suitability for large-scale dynamic connectivity problems. This assignment not only strengthened my understanding of advanced data structures and algorithms but also provided a robust framework for efficiently managing connectivity queries within large datasets.






