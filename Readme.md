
![lab](/resources/pclogo-2-2.png)

## <div align="center">Lab 09 – Introduction to CUDA (Google Colab Edition)</div>


## Objectives:

* Switch on a GPU runtime in Colab and confirm it is working with nvidia-smi
* Write, compile (nvcc) and run a CUDA program from notebook cells
* Explain the host/device pattern: copy in → launch kernel → copy out
* Map blocks and threads onto array elements, in one dimension and in two, with a bounds check

All programs were run in the Colab notebook `SE3082_Lab09_IT24103322.ipynb` on a Tesla T4 (compute capability 7.5, CUDA 13.0).

**Write:** `%%writefile name.cu` on the first line of a cell, then the code  
**Compile and run:** `!nvcc -arch=sm_75 name.cu -o name && ./name`

---

| Exercise | Topic | File |
|---|---|---|
| 1 | Set up the CUDA environment in Google Colab | `Exercise01/hello.cu` |
| 2 | First kernel: adding two numbers | `Exercise02/ex2_add.cu` |
| 3 | Vector addition with 512 blocks and one thread each | `Exercise03/ex3_blocks.cu` |
| 4 | Vector addition with one block and 512 threads | `Exercise04/ex4_threads.cu` |
| 5 | Multiplying two 10,000,000-element vectors (blocks and threads) | `Exercise05/ex5_vecmul.cu` |
| 6 | Multiplying two 10,000 × 10,000 matrices element by element (2D grid) | `Exercise06/ex6_matrix.cu` |

---

The answers and screenshots for all the exercises are in `PC Lab 9 IT24103322.pdf`. Each exercise folder also has its own PDF, and the Colab screenshots are in the `screenshots` folder.
