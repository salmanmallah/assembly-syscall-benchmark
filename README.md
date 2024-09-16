# Syscall vs Int 0x80 Benchmark Tool

This tool compares the execution times of two assembly programs, one using the `int 0x80` system call and the other using `syscall`. It automates the process of assembling, linking, and benchmarking both programs, then outputs the average execution time and the performance difference.

## Features
- Assembles and links user-provided assembly files.
- Runs both programs multiple times and calculates average execution times.
- Displays the percentage difference in performance between `int 0x80` and `syscall`.

## Prerequisites

- **NASM** (Netwide Assembler) installed.  
  You can install it using:
  ```bash
  sudo apt install nasm
  ```

- **figlet** (for terminal banner, optional).  
  You can install it using:
  ```bash
  sudo apt install figlet
  ```

## How to Use

1. Clone this repository:
   ```bash
   [git clone https://github.com/yourusername/syscall-vs-int80-benchmark.git](https://github.com/salmanmallah/assembly-syscall-benchmark.git)
   ```

2. Navigate into the directory:
   ```bash
   cd syscall-vs-int80-benchmark
   ```

3. Make the script executable:
   ```bash
   chmod +x benchmark.sh
   ```

4. Run the tool by providing your assembly files:
   ```bash
   ./benchmark.sh
   ```

5. Follow the prompts to enter the filenames of your two assembly programs:
   - The first file should use `int 0x80`.
   - The second file should use `syscall`.

   For example:
   ```bash
   Enter the filename for program1 (int 0x80, e.g., program1.asm): my_int80_program.asm
   Enter the filename for program2 (syscall, e.g., program2.asm): my_syscall_program.asm
   ```

## Example Commands

For testing two files, e.g., `int80_test.asm` and `syscall_test.asm`, you can do the following:

1. Place the files in the same directory as the script.
2. Run the script:
   ```bash
   ./benchmark.sh
   ```

## Output

The script will display the average execution times for both programs and show which method is faster, as well as by what percentage.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
