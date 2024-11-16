# MetaForge Syntax Guide

This document provides an overview of the syntax used in the MetaForge programming language, highlighting its key features and constructs.

---

## Basics

### Hello World
A simple program in MetaForge looks like this:
```metaforge
fn main() -> void {
    print("Hello, MetaForge!");
}
```

### Variables
Variables are declared using the `let` keyword:
```metaforge
let x = 10;            // Integer
let name = "MetaForge"; // String
let is_active = true;  // Boolean
```

### Comments
Single-line and multi-line comments:
```metaforge
// This is a single-line comment

/*
This is a 
multi-line comment
*/
```

---

## Data Types

### Primitive Types
- Integers: `i8`, `u8`, `i16`, `u16`, `i32`, `u32`, `i64`, `u64`
- Floating-point numbers: `f32`, `f64`
- Boolean: `bool`
- Strings: `str`

### Special Types
- `ptr`: Pointer type for memory addresses.
- `key`, `cipher`, `hash`: Types for cryptographic operations.

---

## Functions

### Basic Function
Functions are defined using the `fn` keyword:
```metaforge
fn add(a: i32, b: i32) -> i32 {
    ret a + b;
}
```

### Returning Values
Use the `ret` keyword to return values:
```metaforge
fn square(x: i32) -> i32 {
    ret x * x;
}
```

### Void Functions
Void functions do not return a value:
```metaforge
fn greet() -> void {
    print("Hello, world!");
}
```

---

## Control Flow

### If-Else
```metaforge
if x > 10 {
    print("x is greater than 10");
} else {
    print("x is 10 or less");
}
```

### Loops
#### While Loop
```metaforge
while x < 10 {
    print(x);
    x += 1;
}
```

#### For Loop
```metaforge
for i in 0..10 {
    print(i);
}
```

---

## Advanced Features

### Pattern Matching
```metaforge
match value {
    1 => print("One"),
    2 => print("Two"),
    _ => print("Other"),
}
```

### Generics
```metaforge
fn swap<T>(a: T, b: T) -> (T, T) {
    ret (b, a);
}
```

### Lambda Functions
```metaforge
let add = (a: i32, b: i32) -> i32 {
    ret a + b;
};
```

### List Comprehension
```metaforge
let squares = [x * x for x in 0..10];
```

---

**Explore, experiment, and forge your path with MetaForge!**
```

---

### **`memory_model.md`**  
```markdown
# MetaForge Memory Model

MetaForge provides fine-grained control over memory allocation and deallocation, making it suitable for system-level programming and performance-critical applications.

---

## Memory Operations

### Allocation
Allocate memory using the `alloc` keyword:
```metaforge
let buffer = alloc 1024; // Allocates 1024 bytes
```

### Deallocation
Free memory explicitly using `free`:
```metaforge
free(buffer);
```

### Pointers
Use `ref` to obtain references and `deref` to access values:
```metaforge
let ptr = ref x;      // Reference to x
let value = deref ptr; // Access the value at ptr
```

---

## Pointer Arithmetic
Manipulate memory addresses directly:
```metaforge
let ptr = alloc 4;     // Allocate 4 bytes
let next = ptr + 4;    // Move 4 bytes ahead
```

---

## Safety Features
MetaForge includes basic safety checks to avoid common pitfalls like double-free errors and invalid dereferences. However, the programmer retains full control.

---

## Example
```metaforge
fn memory_example() -> void {
    let buffer = alloc 256;  // Allocate 256 bytes
    let data = deref buffer; // Access memory
    data = 42;               // Modify memory
    free(buffer);            // Free allocated memory
}
```

**Master memory with precision using MetaForge!**
```

---

### **`cryptography.md`**  
```markdown
# MetaForge Cryptography Guide

MetaForge integrates cryptographic primitives for secure and efficient data handling, making it ideal for applications requiring encryption, hashing, and key management.

---

## Built-In Functions

### Encryption and Decryption
Encrypt data using the `encrypt` function and decrypt using `decrypt`:
```metaforge
let encrypted = encrypt("sensitive data", key);
let decrypted = decrypt(encrypted, key);
```

### Hashing
Generate hashes with the `hash` function:
```metaforge
let hashed = hash("important data");
```

### Key Generation
Generate cryptographic keys with `genkey`:
```metaforge
let key = genkey();
```

### Cipher Operations
Perform advanced cipher manipulations:
```metaforge
let ciphered = cipher("message", algorithm);
```

---

## Supported Algorithms
MetaForge supports the following cryptographic algorithms:
- Symmetric: AES, ChaCha20
- Asymmetric: RSA, ECC
- Hashing: SHA-256, SHA-512, MD5 (for legacy systems)

---

## Example
### Encrypt and Decrypt
```metaforge
fn secure_data() -> void {
    let key = genkey();
    let data = "secret";
    let encrypted = encrypt(data, key);
    let decrypted = decrypt(encrypted, key);
    print(decrypted); // Outputs: "secret"
}
```

### Hash Data
```metaforge
fn generate_hash() -> void {
    let data = "password";
    let hashed = hash(data);
    print(hashed); // Outputs the hash of "password"
}
```

---

**Forge secure systems with built-in cryptography!**
