
# MetaForge Programming Language

MetaForge is a low-level meta-programming language that bridges the gap between assembly and C, while integrating support for Python, C, and C++ libraries. Designed for system-level programming and advanced memory manipulation, MetaForge offers a unique approach to multi-language interoperability and high-performance computing.

---

## Key Features

- **Low-Level Access:** Positioned between assembly and C, offering direct communication with system resources.
- **Cross-Language Integration:** Supports Python, C, and C++ libraries seamlessly.
- **Custom Syntax:** Combines simplicity with flexibility, tailored for developers seeking control over memory, cryptography, and pattern matching.
- **Extensibility:** MetaForge is designed to evolve, with planned support for web systems and additional language integrations.

---

## Language Overview

### Basic Types
MetaForge provides a wide range of basic types, including:
- Signed and unsigned integers: `i8`, `u8`, `i16`, `u16`, etc.
- Floating-point numbers: `f32`, `f64`
- Special types: `ptr`, `key`, `cipher`, `hash`, etc.

### Memory Operations
MetaForge includes powerful memory manipulation commands:
- `alloc` for memory allocation
- `free` for deallocation
- `deref` for dereferencing pointers
- `ref` for obtaining references

### Cryptographic Operations
Built-in cryptographic primitives:
- `encrypt` and `decrypt` for data security
- `hash` for generating hashes
- `genkey` for key generation
- `cipher` for advanced cryptographic operations

### Control Flow
Supports standard control flow constructs:
- `if`, `while`, `for`
- Pattern matching with `match`
- Error handling with `try` and `catch`

### Advanced Constructs
- **Generics:** Define reusable code with parameterized types.
- **Pattern Matching:** Match complex data structures with custom patterns.
- **List Comprehension:** Write concise and efficient iterations.
- **Lambda Functions:** Inline anonymous functions for functional programming.

---

## Installation

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

## Examples

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

## Roadmap

- Simplify syntax while maintaining low-level control.
- Expand compatibility with additional languages.
- Enable web-system integration.
- Develop a dedicated IDE with real-time syntax support.

---

## Contributing

We welcome contributions! Please check the [CONTRIBUTING.md](CONTRIBUTING.md) file for details on our coding standards and submission process.

---

## License

license free

---

**Developed with passion by SeregonWar**  
Explore, Extend, and Forge the Future!
