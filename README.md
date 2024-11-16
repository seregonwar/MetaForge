# MetaForge Programming Language

MetaForge is a low-level meta-programming language that bridges the gap between assembly and C, while integrating support for Python, C, and C++ libraries. Designed for system-level programming and advanced memory manipulation, MetaForge offers a unique approach to multi-language interoperability and high-performance computing.

---

## **Index**
1. [Introduction](#introduction)  
2. [Key Features](#key-features)  
3. [Language Overview](#language-overview)  
   - [Syntax](#syntax)  
   - [Memory Model](#memory-model)  
   - [Cryptography](#cryptography)  
   - [Control Flow](#control-flow)  
   - [Advanced Features](#advanced-features)  
4. [How to Compile](#how-to-compile)  
5. [Installation](#installation)  
6. [Examples](#examples)  
7. [Roadmap](#roadmap)  
8. [Contributing](#contributing)  
9. [FAQ](#faq)  
10. [License](#license)

---

## **Introduction**

MetaForge is a low-level meta-programming language that bridges the gap between assembly and C, while integrating support for Python, C, and C++ libraries. Designed for system-level programming and advanced memory manipulation, MetaForge offers a unique approach to multi-language interoperability and high-performance computing.

---

## **Key Features**

- **Low-Level Access:** Positioned between assembly and C, offering direct communication with system resources.
- **Cross-Language Integration:** Supports Python, C, and C++ libraries seamlessly.
- **Custom Syntax:** Combines simplicity with flexibility, tailored for developers seeking control over memory, cryptography, and pattern matching.
- **Extensibility:** MetaForge is designed to evolve, with planned support for web systems and additional language integrations.

---

## **Language Overview**

### **[Syntax](docs/syntax.md)**  
A detailed overview of MetaForge syntax, including statements, advanced types, pattern matching, and error handling.

### **[Memory Model](docs/memory_model.md)**  
Explore how MetaForge manages memory allocation, deallocation, and pointers.

### **[Cryptography](docs/cryptography.md)**  
Built-in cryptographic tools and their usage.

### **[Control Flow](docs/control_flow.md)**  
Understand control structures like loops, conditionals, and error handling.

### **[Advanced Features](docs/advanced_features.md)**  
Learn about generics, pattern matching, list comprehension, and lambda functions.

---

## **How to Compile**

MetaForge programs are compiled using the official **MetaForge Compiler (MFC)**. 

1. Visit the [MetaForge Compiler Repository](https://github.com/seregonwar/MetaForge-Compiler) to download or clone the compiler source code.
2. Follow the instructions in the `readme.md` of the compiler repository to set up the environment.
3. Compile your MetaForge programs using the following command structure:
   ```bash
   python src/compile_metaforge.py <source_file> -o <output_file> [options]
   ```
   Example:
   ```bash
   python src/compile_metaforge.py examples/hello_world.mf -o build/hello_world.exe --platform windows --arch x64 -v
   ```

For detailed options and configuration, refer to the [CLI Commands documentation](docs/cli_commands.md).

---

## **Installation**

MetaForge requires the following dependencies:
1. **Python (3.x)** for integration scripts.
2. **C/C++ Toolchain** for compilation and linking.
3. **Custom MetaForge CLI** (provided in the release package).

### Steps
1. Clone the repository:  
   ```bash
   git clone https://github.com/seregonwar/metaforge.git
   cd metaforge
   ```
2. Build the compiler:  
   ```bash
   make
   ```
3. Run your first MetaForge program:  
   ```bash
   ./metaforge my_program.mf
   ```

---

## **Examples**

Explore more in the [Examples and Templates](docs/examples_and_templates.md) documentation or visit the [examples folder](https://github.com/seregonwar/MetaForge/tree/main/examples).

### Hello World
```metaforge
fn main() -> void {
    print("Hello, MetaForge!");
}
```

### Memory Allocation
```metaforge
fn allocate_memory() -> ptr {
    let buffer = alloc 1024;
    ret buffer;
}
```

### Cryptographic Hashing
```metaforge
fn compute_hash() -> hash {
    let data = "important data";
    let hashed = hash(data);
    ret hashed;
}
```

---

## **Roadmap**

For planned features and future development, check the [Design Philosophy and Roadmap](docs/design_philosophy.md) document.

---

## **Contributing**

We welcome contributions! Please check the [Contributing Guidelines](docs/contributing_guidelines.md) for details on our coding standards and submission process.

---

## **FAQ**

For common questions and answers, refer to the [FAQ](docs/faq.md).

---

## **License**

License free.

---

**Developed with passion by SeregonWar**  
Explore, Extend, and Forge the Future!  

