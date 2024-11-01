# 🔧 S-MIPS Processor Implementation

## 🎯 Overview

This project implements an S-MIPS architecture processor using Logisim, focusing on efficient instruction interpretation and execution while meeting specific price and performance constraints.

## 📦 Project Materials

* `README.md`: Project documentation and guidelines
* `smips.pdf`: Detailed architecture specifications
* `Python Testing Scripts`:
  * `assembler.py`: Assembly code processor
  * `test.py`: Automated testing framework
  * `price.py`: Component pricing calculator
* `Logisim Circuits`:
  * `s-mips-template.circ`: Base template
  * `s-mips.circ`: Implementation circuit
* `tests/`: Directory containing `.asm` test files

## 🏗️ Architecture Components

### Core Components:
* **CPU**: Main processing unit (requires implementation)
* **RAM**: Memory simulation component
* **RAM Dispatcher**: Test execution controller

### Implementation Guidelines:
* Modifications restricted to CPU component
* External component changes will be ignored during evaluation
* RAM interface specified in `s-mips.pdf`

## 🧪 Automated Testing

### System Requirements:
* Unix-based Operating System
* Python 3 (`python3` command accessible)
* Logisim (accessible via `logisim` command)

### Test Execution:
```bash
./test.py tests s-mips.circ -o ./tests-out -t s-mips-template.circ
```

### Test Case Format:
* Create `.asm` files in the `tests` directory
* Include `#prints <expected_output>` comment
* See existing test cases for reference

## 🔍 Manual Testing Process

1. Assemble test cases using `assembler.py`
2. Verify creation of `Bank0` through `Bank3` files
3. Open `s-mips.circ` in Logisim
4. Enable "Disable Dispatcher" input
5. Load `Bank` files into RAM components
6. Toggle clock for execution

## 📊 Evaluation Criteria

### Submission Details:
* **Deadline**: April 1-5, 2024
* **Format**: `<Student-Name>-C<Group>.zip`
* **Version Control**: Git repository with component-wise commits

### Requirements:

#### 1. Correctness
* Pass all provided test cases
* Match expected outputs defined by `#prints`

#### 2. Price Efficiency
* Less than 100 units (calculated by `price.py`)
* Based on component usage

#### 3. Performance
* Meet cycle count limits per test
* Limits defined by `#limit <iterations>`

## ⚠️ Important Notes

* RAM components from Logisim library cannot be used in custom implementations
* Follow component restrictions for test compatibility
* Maintain systematic version control throughout development

## 📝 License

This project is part of an academic assignment. All rights reserved.
