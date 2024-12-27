# 🛠️ Assembler for Custom Instruction Set

## 📜 Overview
This assembler is designed to convert assembly language instructions into machine code for a custom instruction set architecture (ISA). It simplifies the process of program development by automating the translation of human-readable mnemonics into binary code that can be executed by the target system. The project incorporates various features such as opcode mapping, label resolution, error detection, and machine code generation.

---

## ✨ Key Features
1. **Instruction Parsing**: Efficiently reads and interprets assembly instructions line by line, ensuring adherence to the syntax of the custom ISA.
2. **Opcode Mapping**: Translates mnemonics into their corresponding binary opcodes, based on the predefined mapping table.
3. **Label Resolution**: Automatically resolves symbolic labels into memory addresses, enabling jump instructions to function correctly.
4. **Machine Code Generation**: Produces optimized binary machine code ready for execution on the target hardware or emulator.
5. **Error Detection**: Provides robust error handling, detecting syntax issues, undefined labels, and other common programming mistakes.
6. **Scalable Design**: Modular code structure facilitates easy extension for additional instructions or new features.

---


---

## 🔧 Prerequisites
To run this assembler, ensure the following:
- **Python Version**: Python 3.6 or higher.
- **Knowledge**: Familiarity with basic assembly language programming concepts.

---

## 🚀 How to Use
### Step 1: Clone the Repository
Begin by downloading the source code:
```bash
git clone https://github.com/VIPUL0127/assembler
cd assembler
```

### Step 2: Prepare Input File
Write your assembly program in a text file with a `.asm` extension. Use mnemonics and labels as per the supported instruction set.

### Step 3: Run the Assembler
Execute the assembler using the following command:
```bash
python main.py input_file.asm output_file.bin
```
Replace `input_file.asm` with the path to your assembly file and `output_file.bin` with the desired output file name.

### Step 4: Verify the Output
The generated machine code will be saved in `output_file.bin`. This file can be loaded into the target system or emulator.

---

## 📜 Supported Instructions
The assembler supports the following instructions:

| Mnemonic | Binary Opcode | Description               | Example           |
|----------|---------------|---------------------------|-------------------|
| ADD      | 0001          | Adds values from two registers and stores the result in a register. | `ADD R1, R2, R3` |
| SUB      | 0010          | Subtracts one register's value from another. | `SUB R1, R2, R3` |
| LOAD     | 0100          | Loads data from memory into a register. | `LOAD R1, 0x04`   |
| STORE    | 0101          | Stores register data into a memory location. | `STORE R1, 0x04`  |
| JMP      | 0110          | Jumps to a specified label in the program. | `JMP LOOP`        |

---

## 🧪 Testing
The project includes test cases to validate its functionality. To run the tests:
1. Navigate to the project directory.
2. Use the following command:
```bash
python -m unittest discover tests
```
The test cases compare the assembler's output with expected binary files to ensure accuracy.

---

## 🔍 Error Handling and Debugging
The assembler includes mechanisms to handle common errors:
- **Invalid Syntax**: Reports the line number and type of syntax error.
- **Undefined Labels**: Displays an error if a label is used but not defined in the program.
- **Invalid Instructions**: Warns if an instruction does not match the supported set.

---

## 🛠 Extending the Assembler
You can extend the assembler to support new instructions or features:
1. **Add New Opcodes**: Update the `opcode_mapping` dictionary in `utils.py`.
2. **Enhance Error Handling**: Modify the error-checking logic in `assembler.py`.
3. **Introduce New Features**: Add functionalities like macros, conditional assembly, or pseudo-instructions.

---

## 🤝 Contribution Guidelines
Contributions to this project are highly encouraged! Follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes and push them to your branch.
4. Submit a pull request with a detailed explanation of your changes.

---

## 📧 Contact Information
For questions, suggestions, or issues, feel free to reach out:
- **Email**: [Vipul22576@iiitd.ac.in](mailto:Vipul22576@iiitd.ac.in)

---

## 📌 Additional Notes
- Ensure that your input files strictly follow the defined syntax to avoid errors.
- The assembler's modular design makes it adaptable to other custom instruction sets with minimal modifications.
- Explore the provided sample programs for a quick start.

---

🌟 Happy Coding! 🌟

Let me know if you'd like to add more details or further elaborate any section!
