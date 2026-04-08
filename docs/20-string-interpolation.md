## String Interpolation (f-strings)

Instead of concatenating strings with `+`, you can embed expressions directly inside strings starting with `f`. Syntax inspired from Python.

```lunite
let name = "Program"
let v = 2.3

~~ Old way
out("Welcome to " + name + " v" + str(v))

~~ F-String way
out(f"Welcome to {name} v{v}")

~~ You can do math inside too
out(f"5 squared is {5 * 5}")
```

---

<small>Docs Page 20 | [Previous](#docs/19-enum.md) | [Next](#docs/21-error-diagnostics.md)</small>