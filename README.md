```markdown
# TRON Compiler & The Mia Programming Language

### 📌 GitHub Repository Description
An academically rigorous multi-pass source-to-source compiler (transpiler) and IDE ecosystem that translates Roman Urdu syntax (Mia Language) into high-performance native binaries using Flex, Bison, and a GCC backend[cite: 1, 2].

The TRON Compiler is a complete, custom-engineered compiler development toolchain built to address the intersection of formal compiler theory and linguistic accessibility[cite: 2]. While traditional programming paradigms heavily rely on English-centric vocabularies, this project introduces Mia (Meta Intermediate Abstraction)—a statically typed, imperative programming language utilizing a Roman Urdu syntax structure[cite: 1, 2]. By allowing native South Asian students to express complex programming paradigms using local phonetics (such as `rakho` for variable initialization, `agar`/`warna` for conditional logic, and `jab_tak` for loops), TRON removes the syntax-vocabulary barrier without sacrificing formal technical rigor[cite: 1, 2].

Architected as a multi-pass source-to-source translator, the compiler pipeline features a Flex Lexical Analyzer to handle strategic tokenization, an LALR(1) Bison Parser implementing a Context-Free Grammar (CFG), and an integrated semantic evaluation component[cite: 1, 2]. As rules reduce, the engine simultaneously writes to a JSON-serialized symbol table and emits a machine-independent Three-Address Code (TAC) layer[cite: 1, 2]. These components are systematically stitched together into highly optimized C source code blocks and compiled into native machine applications (`.exe`) via the GNU Compiler Collection (GCC) backend[cite: 1, 2]. 

The toolchain is completely integrated with a custom-built, multi-threaded Python Tkinter desktop IDE[cite: 1, 2]. The workspace features live error routing, an automatic console engine, a live tree-view structural symbol memory inspector, and an intermediate TAC visualization panel to provide complete transparency for educational settings[cite: 1, 2]. 

---

## 🚀 Project Overview & Philosophy

While English remains dominant in global software engineering, the cognitive load of syntax translation often slows down foundational learning for students in South Asia[cite: 2]. 

Mia (Meta Intermediate Abstraction) is designed around the principle of "Logic over Lexicon"[cite: 2]. It allows developers to express complex computational structures (loops, variables, functions) using natural Roman Urdu phonetics, mapping them directly onto native machine logic[cite: 1, 2]. The compiler architecture functions as a multi-stage pipeline, translating `.mia` code into cross-platform Three-Address Code (TAC), converting it to high-performance C, and leveraging GCC (GNU Compiler Collection) to produce native executables (`.exe`)[cite: 1, 2].

### 🛠️ Key Technical Features
* **LALR(1) Parsing Engine:** Implements a robust context-free grammar state machine utilizing Bison[cite: 1, 2].
* **Intermediate Logic Abstraction:** Generates an intermediate Three-Address Code (TAC) representation layer to support machine-independent logic mapping[cite: 1, 2].
* **JSON Symbol Table Serialization:** Tracks identifiers, variable data-types, and line numbers, dynamically serializing state into JSON for developer tools[cite: 1, 2].
* **Integrated Development Environment (IDE):** Houses a native desktop application utilizing Python's Tkinter engine featuring live code streaming, an intermediate TAC terminal, and a visual memory symbol inspector[cite: 1, 2].

---

## 📑 Language Specification & Keyword Reference

Mia includes comprehensive language semantics designed with a fully mapping structural bridge to equivalent execution statements in native C[cite: 1, 2].

| Mia Keyword | English Meaning | Usage Example | Emitted Code Structure |
| :--- | :--- | :--- | :--- |
| `rakho` | Declare / Assign | `rakho x = 10;` | `double x = 10;` |
| `bol` | Print / Standard Out | `bol x;` | `printf("%g", x);` |
| `agar` | Conditional If | `agar (x > 0) { ... }` | `if (x > 0) { ... }` |
| `warna` | Else Block | `} warna { ... }` | `} else { ... }` |
| `jab_tak` / `jabtak` | While Loop | `jab_tak (x < 5) { ... }` | `while (x < 5) { ... }` |
| `har` | For Loop Block | `har (rakho i=0, i<5, rakho i=i+1)` | `for(double i=0; i<5; i=i+1)` |
| `kaam` | Function Definition | `kaam add(a, b) { ... }` | `double add(double a, double b)` |
| `wapas` | Return Statement | `wapas x;` | `return x;` |
| `shamil` | Include Library | `shamil "math.h";` | `#include "math.h"` |
| `aur` | Logical AND | `x > 0 aur x < 10` | `x > 0 && x < 10` |
| `ya` | Logical OR | `x < 0 ya x > 10` | `x < 0 \|\| x > 10` |

---

## 💻 Mia Syntax Guide

### 1. Variables & Arrays
Variables are dynamically inferred and managed via the symbol table[cite: 1, 2]. Arrays store flat sequential `double` blocks[cite: 1].
```pascal
rakho x = 10;                  // Numeric variable (double)
rakho name = "Ali";            // String variable (char*)
rakho result = x + 5;          // Assignment using expression results
rakho arr[5];                  // Native array allocation of 5 elements
arr[0] = 99;                   // Array element assignment

```

### 2. Standard Output

Output stream strings, raw variables, or comma-separated lists directly to the console.

```pascal
bol x;                          // Prints numeric values directly
bol "Hello World";              // Prints literal strings
bol "Result is: ", x;           // Sequentially prints chained parameters

```

### 3. Conditional Branching

Standard evaluation layout mimicking structured block execution.

```pascal
agar (x > 0) {
    bol "Positive";
} warna {
    bol "Not positive";
}

```

### 4. Loops (`while` & `for`)

Supports both standard conditional iteration blocks and structured declaration ranges.

```pascal
// While Loop execution block
rakho i = 0;
jab_tak (i < 5) {
    bol i;
    rakho i = i + 1;
}

// For Loop execution block
har (rakho j = 0, j < 5, rakho j = j + 1) {
    bol j;
}

```

### 5. Custom Functions

Define modular structures using `kaam` and pass calculations backward utilizing `wapas`.

```pascal
kaam jama(a, b) {
    wapas a + b;
}

rakho result = jama(10, 20);

```

### 6. Custom Math Library Built-ins

Integrate system mathematics tools by invoking the standard localized runtime wrapper.

```pascal
shamil "math.h";
rakho sq = jazar(16);           // Square root helper -> sqrt(16)
rakho pw = taqat(2, 10);        // Power calculation helper -> pow(2,10)
rakho ab = mutlaq(-7.5);        // Absolute value helper -> fabs(-7.5)

```

---

## 📋 Comprehensive Program Examples

### Example 1 — Basic Arithmetic Operations

```pascal
shamil "math.h";
rakho x = 10;
rakho y = 20;
rakho sum = x + y;
rakho diff = x - y;
rakho prod = x * y;
rakho quot = x / y;
bol "Sum: ", sum;
bol "Diff: ", diff;
bol "Product: ", prod;
bol "Quotient: ", quot;

```

### Example 2 — Nested If/Else Code Evaluations

```pascal
rakho marks = 75;
agar (marks >= 80) {
    bol "Grade A";
} warna {
    agar (marks >= 60) {
        bol "Grade B";
    } warna {
        bol "Grade C";
    }
}

```

### Example 3 — While Loop Countdown

```pascal
rakho n = 10;
jab_tak (n > 0) {
    bol n;
    rakho n = n - 1;
}
bol "Blast off!";

```

### Example 4 — For Loop Iterative Summation

```pascal
rakho total = 0;
har (rakho i = 1, i <= 10, rakho i = i + 1) {
    rakho total = total + i;
}
bol "Sum 1 to 10: ", total;

```

### Example 5 — Functional Subroutines & Math Wrappers

```pascal
shamil "math.h";

kaam hypotenuse(a, b) {
    rakho sq_sum = a*a + b*b;
    wapas jazar(sq_sum);
}

rakho result = hypotenuse(3, 4);
bol "Hypotenuse: ", result;

```

### Example 6 — Array Allocation and Traversal

```pascal
rakho marks[5];
marks[0] = 85;
marks[1] = 90;
marks[2] = 78;
marks[3] = 92;
marks[4] = 88;
rakho total = marks[0] + marks[1] + marks[2] + marks[3] + marks[4];
rakho avg = total / 5;
bol "Average: ", avg;

```

### Example 7 — Native String Concatenation

```pascal
rakho first = "Muhammad ";
rakho last = "Ali";
rakho full = first + last;
bol "Full Name: ", full;

```

---

## 🏗️ Architectural Pipeline

The system is split into a modular 6-stage compiler pipeline designed to process instructions incrementally:

1. **Lexical Analysis (`lexer.l` via Flex):** Streams source characters into tokens (e.g., `TOK_VAR`, `TOK_ID`, `TOK_NUM`). Discards whitespace and commentary components automatically.


2. **Syntax Analysis (`parser.y` via Bison):** Enforces language constraints through a deterministic shift-reduce stack mechanism using an LALR(1) framework.


3. **Semantic Analysis (`symtable.h`):** Verifies logical typing safety, visibility ranges, and ensures variable identifiers exist within active scope domains.


4. **Intermediate Representation (TAC):** Transforms grammar reduction steps into an explicit three-address machine-independent code format.


5. **C Synthesis & Stitching Engine:** Accumulates text streams (`.tmp`) and joins them systematically to compose the localized `generated_target.c` file.


6. **Machine Code Target Backend:** Invokes GCC to build intermediate targets into high-speed execution native binaries (`program.exe`).



---

## 🗂️ Repository Structure

```text
project/
├── ide/
│   └── app.py                  # Python Tkinter Multi-threaded IDE Frontend[cite: 1, 2]
├── inputs/
│   └── hello.mia               # Default testing script inputs[cite: 1]
├── libraries/
│   └── math.h                  # Core system mathematical Roman Urdu library wrapper[cite: 1]
├── downloads/
│   └── *.mia                   # User-saved persistent operational files[cite: 1]
└── system/
    ├── src/
    │   ├── lexer.l             # Flex Lexical Tokenizer Grammar Definition[cite: 1]
    │   ├── parser.y            # Bison Rule Architecture & Emission Configuration[cite: 1]
    │   └── symtable.h          # Global Symbol Table Structure & JSON Serializer[cite: 1]
    ├── temp/                   # Runtime target outputs (generated_target.c, mia_tac.tac)[cite: 1]
    ├── output/                 # Destination execution directories (program.exe)[cite: 1]
    └── Makefile                # Build orchestration configuration file[cite: 1]

```

---

## ⚙️ Build and Installation Requirements

### Prerequisites

Ensure the following development dependencies are added to your host platform environment variable system path:

* **MinGW Development Suite** (specifically providing `mingw32-make` and `gcc`)


* **Flex** (Fast Lexical Analyzer Generator Engine)


* **Bison** (GNU Parser Generator Engine)


* **Python 3.x** (with integrated standard `tkinter` UI libraries)



### Building the Toolchain via Terminal

Navigate directly into the compilation control directory (`system/`) to build the core compiler logic:

```bash
# Clean binary artifacts and build the primary transpiler executable (mia.exe)
mingw32-make clean
mingw32-make all

# Transpile, synthesize intermediate C assets, and evaluate tests in a single pass
mingw32-make run

```

### Accessing the Workspace IDE Dashboard

To compose programs with a live developer environment tracking Three-Address Code output logs and real-time active symbol allocations, execute the companion GUI desktop file:

```bash
cd ide
python app.py

```

---

## 📝 Intermediate Representation (TAC) Sample Output

When a `.mia` assignment or conditional statement is parsed, the parser emits a clean, sequential Three-Address Code trace directly to `temp/mia_tac.tac`:

```assembly
; ===== Mia Three-Address Code Intermediate Stream =====
BEGIN_MAIN
; INCLUDE math.h
x = 10
y = 20
t0 = x + y
sum = t0
PRINT "Addition Result: "
PRINT sum
END_MAIN

```

```

```
