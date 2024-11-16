# MetaForge CLI Commands

The MetaForge Compiler (MFC) provides a rich set of commands and options for building and debugging MetaForge programs.

---

## Basic Commands

### Compile a Program
Compile a `.mf` file:
```bash
python src/compile_metaforge.py <input_file> -o <output_file>
```

### Specify Target Platform and Architecture
```bash
--platform <platform>  # e.g., windows, linux, macos
--arch <architecture>  # e.g., x64, arm
```

---

## Advanced Options

### Debugging
Include debugging information:
```bash
--debug
```

### Optimization
Control optimization levels:
```bash
-O0  # No optimization
-O1  # Basic optimization
-O2  # Full optimization
```

### Verbose Output
Enable verbose output for debugging:
```bash
-v
```

### Example
```bash
python src/compile_metaforge.py examples/hello_world.mf -o build/hello_world.exe --platform windows --arch x64 -v --debug -O2
```

**Master the CLI for full control over your builds!**



