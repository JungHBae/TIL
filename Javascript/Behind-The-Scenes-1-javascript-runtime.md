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
 
 **Just-in-time (JIT) compilation** - Entire code in converted into machine code at once, then executed immediately. (Javascript)
 
  ```mermaid
flowchart LR
    A[Source code]-->|Step 1 :<br/>Compilation|B[Machine code, but NOT a portable file]
    B[Machine code]-->|Step 2 :<br/>Execution happens immediately|C[Program running]
 ```

## JS engine

 **First**, the javascript engine parses the code. During the parsing process the code is parsed into a data structure called Abstract Syntax Tree (AST).
 This step also checks if there are any syntax errors. 
 
 **Next**, the generated AST is compiled into machine code. 
 
 **Finally**, the compiled machine code gets immediately executed. Execution happens in the javascript engine's **call stack**.
 
 flowchart TB
    subgraph Parsing
        P1[Tokenize] --> P2[Parse]
    end
    subgraph Compilation
        C1[Abstract Syntax Tree] --> C2[Bytecode Generation] --> C3[Machine Code Generation]
    end
    subgraph Execution
        E1[Execution]
    end
        E1--> E2[Optimization]
    subgraph Compilation 2
        C4[Recompilation] --> C2
    end
    P2 --> C1
    C3 --> E1
    E2 --> C4
 
  ## Javascript Runtime in the Browser
  
 In the context of JavaScript, the runtime refers to the environment in which JavaScript code is executed. 
 This includes the **JavaScript engine**, which interprets and  executes the JavaScript code, as well as other 
 components such as the **Web APIs** and the **event loop**.

 The **JavaScript engine** is responsible for parsing, compiling, and executing JavaScript code. It provides a runtime 
 environment that includes features such as variables, functions, and object-oriented programming constructs. 
 Common JavaScript engines include Google's V8 engine, used in the Chrome browser, and Mozilla's SpiderMonkey engine, used in Firefox.

 In addition to the JavaScript engine, modern browsers also provide a set of **Web APIs** that allow JavaScript code 
 to interact with the browser and perform tasks such as manipulating the DOM, making HTTP requests, and accessing 
 device features like geolocation or the camera. These Web APIs are not part of the JavaScript language itself, 
 but are provided by the browser environment.

 The **callback queue** is another component of the JavaScript runtime that manages the order in which code is executed 
 in response to events such as user input or network requests. The **event loop** runs continuously and checks for 
 new events to process, then executes the corresponding code and updates the UI as necessary.
