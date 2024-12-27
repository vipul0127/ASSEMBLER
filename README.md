To change the file format for your assembler project, I suggest a new structure for the project files while maintaining the key features and instructions. Here's an updated version of the structure along with explanations for each file/folder:

---

### 🛠️ **Assembler for Custom Instruction Set**  
### 📜 **Overview**  
This assembler is designed to convert assembly language instructions into machine code for a custom instruction set architecture (ISA). It simplifies the process of program development by automating the translation of human-readable mnemonics into binary code that can be executed by the target system. The project incorporates various features such as opcode mapping, label resolution, error detection, and machine code generation.

### ✨ **Key Features**  
- **Instruction Parsing**: Efficiently reads and interprets assembly instructions line by line, ensuring adherence to the syntax of the custom ISA.
- **Opcode Mapping**: Translates mnemonics into their corresponding binary opcodes, based on the predefined mapping table.
- **Label Resolution**: Automatically resolves symbolic labels into memory addresses, enabling jump instructions to function correctly.
- **Machine Code Generation**: Produces optimized binary machine code ready for execution on the target hardware or emulator.
- **Error Detection**: Provides robust error handling, detecting syntax issues, undefined labels, and other common programming mistakes.
- **Scalable Design**: Modular code structure facilitates easy extension for additional instructions or new features.

### 🗂 **Project Structure**

```plaintext
/automatedTesting
    /tests
        /assembly
            /errorGen
                - test1
                - test2
                - test3
                - test4
                - test5
            /hardBin
                - test1
                - test2
                - test3
                - test4
                - test5
            /simpleBin
                - test1
                - test2
                - test3
                - test4
                - test5
            /bin_h
                - test1
                - test2
                - test3
                - test4
                - test5
            /bin_s
                - test1
                - test2
                - test3
                - test4
                - test5
    /run
    /src
        - SimGrader.py
        - AsmGrader.py
        - Grader.py
        - Results.py
        /utils
            /__pycache__
                - colors.cpython-310.pyc
                - colors.cpython-38.pyc
            - colors.py
        /__pycache__
            - AsmGrader.cpython-38.pyc
            - SimGrader.cpython-38.pyc
            - SimGrader.cpython-310.pyc
            - Grader.cpython-310.pyc
            - Grader.cpython-38.pyc
            - AsmGrader.cpython-310.pyc
            - Results.cpython-310.pyc
            - Results.cpython-38.pyc
        - main.py

/Simple-Assembler
    - Assembler.py
    /__pycache__
        - input.cpython-38.pyc
        - data.cpython-38.pyc
        - mem_addresses.cpython-38.pyc
        - binary.cpython-38.pyc
    /run

/SimpleSimulator
    /__pycache__
        - AssemblerF.cpython-38.pyc
        - AssemblerS.cpython-38.pyc
    - simulator.py
    /run

project.py

```

### 🔧 **Prerequisites**  
To run this assembler, ensure the following:
- **Python Version**: Python 3.6 or higher.
- **Dependencies**: Install the required libraries via `requirements.txt` (if applicable).

Install dependencies:
```bash
pip install -r requirements.txt
```

### 🚀 **How to Use**  
#### Step 1: Clone the Repository  
Begin by downloading the source code:
```bash
git clone https://github.com/your-repo/assembler
cd assembler
```

#### Step 2: Prepare Input File  
Write your assembly program in a text file with a `.asm` extension. Use mnemonics and labels as per the supported instruction set.

#### Step 3: Run the Assembler  
Execute the assembler using the following command:
```bash
python main.py input_file.asm output_file.bin
```
Replace `input_file.asm` with the path to your assembly file and `output_file.bin` with the desired output file name.

#### Step 4: Verify the Output  
The generated machine code will be saved in `output_file.bin`. This file can be loaded into the target system or emulator.

### 📜 **Supported Instructions**

The assembler supports the following instructions:

| Mnemonic | Binary Opcode | Description | Example |
|----------|---------------|-------------|---------|
| ADD      | 0001          | Adds values from two registers and stores the result in a register. | ADD R1, R2, R3 |
| SUB      | 0010          | Subtracts one register's value from another. | SUB R1, R2, R3 |
| LOAD     | 0100          | Loads data from memory into a register. | LOAD R1, 0x04 |
| STORE    | 0101          | Stores register data into a memory location. | STORE R1, 0x04 |
| JMP      | 0110          | Jumps to a specified label in the program. | JMP LOOP |

### 🧪 **Testing**  
The project includes test cases to validate its functionality. To run the tests:
1. Navigate to the project directory.
2. Use the following command:
```bash
python -m unittest discover tests
```
The test cases compare the assembler's output with expected binary files to ensure accuracy.

### 🔍 **Error Handling and Debugging**  
The assembler includes mechanisms to handle common errors:
- **Invalid Syntax**: Reports the line number and type of syntax error.
- **Undefined Labels**: Displays an error if a label is used but not defined in the program.
- **Invalid Instructions**: Warns if an instruction does not match the supported set.

### 🛠 **Extending the Assembler**  
You can extend the assembler to support new instructions or features:
- **Add New Opcodes**: Update the `opcode_mapping` dictionary in `utils/opcode_mapping.py`.
- **Enhance Error Handling**: Modify the error-checking logic in `assembler.py`.
- **Introduce New Features**: Add functionalities like macros, conditional assembly, or pseudo-instructions.

### 🤝 **Contribution Guidelines**  
Contributions to this project are highly encouraged! Follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes and push them to your branch.
4. Submit a pull request with a detailed explanation of your changes.

### 📧 **Contact Information**  
For questions, suggestions, or issues, feel free to reach out:
- **Email**: Vipul22576@iiitd.ac.in

---

### 📌 Additional Notes
Ensure that your input files strictly follow the defined syntax to avoid errors.
The assembler's modular design makes it adaptable to other custom instruction sets with minimal modifications.
Explore the provided sample programs for a quick start.
🌟 Happy Coding! 🌟

Let me know if you'd like to add more details or further elaborate any section!







