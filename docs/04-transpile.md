## Transpile Lunite Interpreter

As you know, the Lunite interpreter is made in Python. But due to societal norms, it is considered to be extremely slow for any good work. So, it is recommended that you transpile Lunite from Python to some other language. I chose C++.

You can transpile Lunite from Python to C++ using Cython. This creates a standalone executable that runs 2 to 3 times faster than the Python version.

### Prerequisites

These are the requirements for transpiling `lunite.py` into C++.

- **Python 3.x**
- **Cython:** Install with `pip install cython`
- **C++ Compiler:** (Recommended) GCC (`g++`) for Linux/MacOS, [w64devkit](https://github.com/skeeto/w64devkit) for Windows

### Transpile Python to C++

Run this command to output `lunite.cpp` C++ source code file using Cython.

```bash
python -m cython --embed --cplus -3 -o lunite.cpp lunite.py
```

### Compile Binary

**Linux/MacOS:** Run: ****`g++ -O3 -o lunite lunite.cpp $(python3-config --cflags) $(python3-config --ldflags --embed)` (untested)

**Windows:** First check the existence of the folder `C:\Program Files\Python313\Include` and the DLL file `C:\Program Files\Python313\libs\python313.lib` (highly depends on your Python version). If you have a different version of Python, please use the correct paths.

```bash
g++ -o lunite.exe -O3 -m64 -mconsole -municode -I "C:\Program Files\Python313\Include" lunite.cpp "C:\Program Files\Python313\libs\python313.lib"
```

**Note:** On Windows, if you get an error during compiling or execution about a missing DLL, you must copy the `python3xx.dll` (found in your Python installation folder and named according to your Python version) to the same directory as `lunite.py` or `lunite.exe` for it to compile or run.

---

<small>Docs Page 4 | [Previous](#docs/03-vscode-ext.md) | [Next](#docs/05-manual.md)</small>