# MetaForge Examples and Templates

Explore these examples to get started with MetaForge.

---

## Basics

### Hello World
```metaforge
fn main() -> void {
    print("Hello, MetaForge!");
}
```

### Simple Addition
```metaforge
fn add_numbers(a: i32, b: i32) -> i32 {
    ret a + b;
}
```

---

## Advanced

### Memory Allocation
```metaforge
fn allocate_buffer(size: i32) -> ptr {
    let buffer = alloc size;
    ret buffer;
}
```

### File Encryption
```metaforge
fn encrypt_file(filepath: str, key: key) -> void {
    let data = read_file(filepath);
    let encrypted = encrypt(data, key);
    write_file(filepath + ".enc", encrypted);
}
```

---

## Templates

### Basic CLI Program
```metaforge
fn main(args: list[str]) -> void {
    if len(args) > 1 {
        print("Argument: ", args[1]);
    } else {
        print("No arguments provided.");
    }
}
```

