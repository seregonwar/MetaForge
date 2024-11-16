# MetaForge Build System

MetaForge includes a flexible build system for compiling and linking programs across various platforms.

---

## Compilation Flags

### Platform
Specify the target platform:
- `--platform windows`
- `--platform linux`
- `--platform macos`

### Architecture
Define the architecture:
- `--arch x64`
- `--arch arm`

### Optimization
Use `-O` to enable optimizations:
- `-O0`: No optimization
- `-O1`: Basic optimization
- `-O2`: Full optimization

---

## Example
Compiling a MetaForge program for a 64-bit Linux system with optimizations:
```bash
python src/compile_metaforge.py examples/program.mf -o build/program --platform linux --arch x64 -O2
```

**Control every aspect of your build process!**
