# Getting Started with MetaForge

This guide will help you set up MetaForge and write your first program.

---

## Prerequisites
- Python 3.x installed
- C/C++ toolchain (e.g., GCC or Clang)
- MetaForge Compiler (MFC)

---

## Installation
1. Clone the MetaForge Compiler repository:
   ```bash
   git clone https://github.com/seregonwar/metaforge-compiler.git
   cd metaforge-compiler
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Compile the compiler (if required):
   ```bash
   make
   ```

---

## Writing Your First Program
1. Create a new file called `hello_world.mf`:
   ```metaforge
   fn main() -> void {
       print("Hello, MetaForge!");
   }
   ```

2. Compile the program:
   ```bash
   python src/compile_metaforge.py examples/hello_world.mf -o build/hello_world.exe --platform windows --arch x64
   ```

3. Run the program:
   ```bash
   ./build/hello_world.exe
   ```

---

**You're ready to forge new programs!**







