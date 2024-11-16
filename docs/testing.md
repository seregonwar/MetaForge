# MetaForge Testing Guide

This guide explains how to test your MetaForge programs to ensure correctness and reliability.

---

## Unit Testing

MetaForge includes a built-in testing framework.

### Writing Tests
Create a test file (e.g., `test_example.mf`):
```metaforge
fn test_addition() -> void {
    let result = add(2, 3);
    assert(result == 5, "Addition test failed");
}
```

### Running Tests
Run tests using the `--test` flag:
```bash
python src/compile_metaforge.py tests/test_example.mf --test
```

---

## Debugging
Use the `--debug` flag to include debug symbols:
```bash
python src/compile_metaforge.py examples/program.mf -o build/program --debug
```

---

**Test early, test often!**
```

---

### **`platform_support.md`**  
Elenca le piattaforme supportate e i dettagli di compatibilità.

```markdown
# MetaForge Platform Support

MetaForge is designed to run on multiple platforms and architectures.

---

## Supported Platforms
- **Windows**: Windows 10, 11
- **Linux**: Ubuntu, Fedora, Arch
- **macOS**: macOS Monterey and later

---

## Supported Architectures
- x86/x64
- ARM/ARM64

---

## Example Configurations
### Windows (x64)
```bash
python src/compile_metaforge.py examples/hello_world.mf -o build/hello_world.exe --platform windows --arch x64
```

### Linux (ARM)
```bash
python src/compile_metaforge.py examples/hello_world.mf -o build/hello_world --platform linux --arch arm
```

---

**Build anywhere, run everywhere!**
```

---

### **`error_handling.md`**  
Spiega come MetaForge gestisce gli errori.

```markdown
# MetaForge Error Handling

MetaForge includes robust error handling mechanisms to ensure program reliability.

---

## Try-Catch
Handle errors using `try` and `catch`:
```metaforge
try {
    let result = risky_operation();
} catch (err) {
    print("Error occurred: ", err);
}
```

---

## Assert
Validate conditions with `assert`:
```metaforge
assert(x > 0, "x must be positive");
```

---

## Error Propagation
Propagate errors using `throw`:
```metaforge
fn divide(a: i32, b: i32) -> i32 {
    if b == 0 {
        throw "Division by zero";
    }
    ret a / b;
}
```

---

**Handle errors gracefully!**
