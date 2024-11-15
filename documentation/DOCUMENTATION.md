 

# **MetaForge - Official Documentation**
## **Index**
1. [Introduction](#introduction)
2. [Main features](#characteristics-principals)
3. [MetaForge syntax](#syntax-of-metaforge)
   - [Statements](#statements)
   - [Advanced types](#advanced-types)
   - [Pattern Matching](#pattern-matching)
   - [Error handling](#management-of-errors)
   - [Memory operations](#memory-operations)
   - [Cryptographic operations](#cryptographic-operations)
4. [Practical examples](#examples-practical)
5. [Future extensions](#extensions-futures)
---
## **Introduction**
MetaForge is a **meta-level** programming language, situated conceptually between low-level (like Assembly) and mid-level (like C). It provides total control of hardware, combined with modern syntax and advanced functionality, making it a versatile tool for developing critical and secure applications.
### **Objectives**
- Combine low-level control with modern simplicity and versatility.
- Support interoperability with libraries and languages such as **Python**, **C** and **C++**.
- Provide tools for cryptography, memory manipulations, and complex systems.
---
## **Main Features**
- **Compact and modern syntax**: Inspired by languages such as Rust and Python.
- **Advanced typing**: Support for generics, cryptographic types and pattern matching.
- **Multi-language compatibility**: Integrates external libraries in C, C++ and Python.
- **Low-level operations**: Direct memory manipulation.
- **Cryptographic extensions**: Built-in functions for encryption, hashing and key management.
---
## **Syntax of MetaForge**.
### **Declarations**.
MetaForge supports declarations of variables, functions, structures, enumerations and module imports.
#### **Example of structure declaration**
```metaforge
struct MemoryBlock {
    ptr address;
    u32 size;
    u32 protection;
}
```
#### **Example function declaration**
```metaforge
fn allocate_memory(HANDLE process, u32 size) -> MemoryBlock {
    let block = MemoryBlock {
        address: alloc size,
        size: size,
        protection: 0x40 // PAGE_EXECUTE_READWRITE
    };
    ret block;
}
```
---
### **Advanced types**
MetaForge introduces types for arrays, closures, and encryption.
- **Array**: `u32[10]` represents an array of 10 unsigned integers.
- **Closure**: `fn(i32) -> bool` represents an anonymous function that accepts an integer and returns a boolean.
- **Cryptographic types**: Specific to handle encryption operations.
  - `key`, `cipher`, `hash`, `bytes`, `stream`.
---
### **Pattern Matching**.
Pattern matching allows expressions to be compared against multiple instances in an elegant way.
#### **Example**
```metaforge
match value {
    0 => print(“Zero”),
    1 => print(“One”),
    _ => print(“Other”)
}
```
---
### **Error handling**
MetaForge supports constructs for error checking via `try` and `catch` blocks.
#### **Example**
```metaforge
try {
    let result = risky_function();
} catch err {
    print(“Error:”, err);
}
```
---
### **Memory operations**
MetaForge includes direct memory management features.
#### **Example allocation**
```metaforge
let ptr = alloc 64; // Allocates 64 bytes
free ptr; // Frees up memory
```
---
### **Cryptographic operations**
Built-in constructs for encryption, hashing and key management.
#### **Hashing example**
```metaforge
let digest = hash “message” with “SHA256”;
```
---
## **Practical Examples**
### **Hello World**
```metaforge
fn main() {
    print(“Hello, MetaForge!”);
}
```
### **Advanced Pattern Matching**
````metaforge
let result = match input {
    0 => “No results.”
    1 => “Found one”,
    _ => “Unknown error”
};
```
### **Cryptography**
````metaforge
let key = genkey 256;
let ciphertext = encrypt “message” using key;
let plaintext = decrypt ciphertext using key;
```
---
## **Future extensions**
- Support for **WebAssembly** for execution in the browser.
- Integration with modern languages such as **Rust** and **Go**.
- Dedicated IDE for a better development experience.

