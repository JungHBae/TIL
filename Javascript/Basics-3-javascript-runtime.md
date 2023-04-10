# Javascript Runtime

## Compilation vs Interpretation:

 **Compilation** - Entire code in converted into machine code at once, and written to a binary file that can be executed by a computer.
 
 ```mermaid
flowchart LR
    A[Source code]-->|Step 1 :<br/>Compilation|B[Portable file:<br/>machine code]
    B[Portable file:<br/>machine code]-->|Step 2 :<br/>Execution|C[Program running]
 ```
 
 **Interpretation** - Interpreter runs through the source code and executes it in line by line.
 
  ```mermaid
flowchart LR
    A[Source code]-->|Step 1 :<br/>Execution line by line|B[Program running]
 ```
 
 **Just-in-time (JIT) compilation** - Entire code in converted into machine code at once, then executed immediately.
 
  ```mermaid
flowchart LR
    A[Source code]-->|Step 1 :<br/>Compilation|B[Machine code (not a portable file)]
    B[Machine code]-->|Step 2 :<br/>Execution(happens immediately)|C[Program running]
 ```
