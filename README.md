# project_1 — Simple C++ Calculator

A small command-line calculator implemented in C++ (calculator.cpp). This README documents what the program does, how to build and run it, and notes about its behavior.

## Table of Contents

- [About](#about)
- [Status](#status)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Build & Installation](#build--installation)
- [Usage](#usage)
- [Behavior notes](#behavior-notes)
- [Development](#development)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## About

This repository contains a simple interactive calculator implemented in C++ (calculator.cpp). It prompts the user for two integers and an operator, then prints the result. It's intended as a small demo or starter project.

## Status

Prototype / learning example — suitable for demonstration and small experiments.

## Features

- Addition (+)
- Subtraction (-)
- Multiplication (*)
- Integer division (/) with divide-by-zero check
- Power (^) using pow from <cmath>
- Modulus (%) with zero-check

## Prerequisites

- A C++ compiler (g++, clang++)
- Basic command-line familiarity

## Build & Installation

Clone the repo and compile the program:

```bash
git clone https://github.com/Utkarsh636/project_1.git
cd project_1
g++ calculator.cpp -o calculator
```

Then run:

```bash
./calculator
```

## Usage

The program runs interactively. It prompts:

- "Enter the first number:" — enter an integer
- "Enter the second number:" — enter an integer
- It then shows the operator choices and waits for a single-character operator: + - * / ^ %

Example session:

```
welcome to the calculator
Enter the first number: 5
Enter the second number: 2
please select the operator to proceed
+ for addition
- for subtraction
* for multiplication
/ for division
^ for power
% for modulus
+
7
```

## Behavior notes

- The program uses int for inputs (num1, num2). Division (/) performs integer division; e.g., 5 / 2 yields 2.
- The power operator (^) is implemented with pow(num1, num2) from <cmath>. pow returns a floating-point value (double). When both inputs are integers, common results are integral, but the output may be printed as a floating-point representation depending on the value.
- Division and modulus protect against division by zero and will print an error message if the second number is zero.
- Input is simple and not validated beyond the checks described; non-integer input will cause std::cin to fail.

## Development

- The code is a single-file example (calculator.cpp). Suggested improvements:
  - Add input validation and support for floating-point numbers.
  - Improve prompt/UX and error handling.
  - Add unit tests for operations and edge cases.
  - Consider using long long or checking for overflow for large exponents.

## Contributing

Contributions are welcome. Suggested workflow:

1. Fork the repository.
2. Create a branch: `git checkout -b feature/my-feature`.
3. Commit changes: `git commit -m "Describe change"`.
4. Push: `git push origin feature/my-feature`.
5. Open a pull request describing your changes.

Please follow code style and include tests where appropriate.

## License

This project is available under the MIT License.

## Contact

Create an issue or reach out to the repository owner: https://github.com/Utkarsh636
