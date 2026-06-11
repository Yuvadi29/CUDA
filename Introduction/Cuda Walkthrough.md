If you're building AI, LLMs , video processing tools, or high-performance applications, CUDA is one of the most important technologies to understand.

---
## What is CUDA ?
CUDA (Compute Unified Device Architecture) is a parallel computing platform and programming model created by NVIDIA.
It allows developers to use an NVIDIA GPU not just for graphics, but for general-purpose computation.

Without CUDA:
`CPU`
 `├─ Task 1`
 `├─ Task 2`
 `├─ Task 3`
 `└─ Task 4`
 Mostly we have sequential execution.

With CUDA:
`GPU`
 `├─ Task 1`
 `├─ Task 2`
 `├─ Task 3`
 `├─ Task 4`
 `├─ Task 5`
 `├─ Task 6`
 `└─ Thousands more`
 Massive parallel execution

---
## Why was CUDA Created ?
Traditional CPUs are optimized for:
- Complex logic
- Low latency
- Few powerful cores
GPUs are optimized for:
- Repetitive calculations
- Matrix Operations
- Parallel Workloads
This makes GPUs ideal for:
- Deep learning
- AI Training
- Video Processing
- Scientific Computing
- Image Rendering
- Simulations

---
## CUDA Toolkit
It is basically a collection of tools, libraries, and compilers that let developers write software that runs on NVIDIA GPUs.
Think of it as:
`CUDA Toolkit`
`├── Compiler (nvcc)`
`├── Runtime Libraries`
`├── CUDA Drivers`
`├── Debugging Tools`
`├── Profiling Tools`
`└── GPU Accelerated Libraries`

---
## Components of CUDA Toolkit
1. NVCC Compiler
	This is the CUDA Compiler. When we run normal C++ Code we create the object file with `.cpp` extention and use `g++` for compilation whereas for CUDA, we use `.cu` as CUDA source file extension and `nvcc` as compiler.
	
	Normal C++:
	`g++ main.cpp`
	 
	 CUDA:
	 `nvcc main.cu`

2. CUDA Runtime
	It provides APIs like `cudaMalloc()`, `cudaMemcpy()`, `cudaFree()` which are used for GPU memory management.
3. CUDA Libraries
	NVIDIA provides optimized libraries. Some of the famous ones are cuBLAS, cuDNN, NCCL, cuFFT, TensorRT
4. Profiling Tools
	These are used to identify GPU bottlenecks. For e.g. Nsight Systems, Nsight Compute

---
## CPU vs GPU Execution
Imagine adding 1 million numbers
**CPU:**
```c++
for(int i=0; i<1000000;i++){
result[i] = a[i] + b[i];
}
```
One core executes many operations.
**GPU:**
```c++
Thread 1 -> a[0] + b[0]
Thread 2 -> a[1] + b[1]
Thread 3 -> a[2] + b[2]
...
Thread 1000000 -> a[n] + b[n]
```
Thousands of threads work simultaneously.