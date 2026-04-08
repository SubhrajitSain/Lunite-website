## Macros

Macros are preprocessed before the code is lexed or parsed. They allow for literal text replacement and code injection.

### Syntax & Usage

- **Constant Macros:** Simple value replacement.
- **Functional Macros:** Arguments are wrapped in parentheses for safety during replacement.
- **Multiline Macros:** Can inject entire blocks of code.

```lunite
macro PI = 3.14159
macro SQ(x) { ((x) * (x)) }

macro check_auth(user) {
    if (user == null) {
        out("Access Denied")
        return null
    }
}

func start(u) {
    check_auth(u)
    out("Welcome " + u + "!")
    out("Pi = " + PI)
    out("5 squared = " + SQ(5))
}
```

---

<small>Docs Page 16 | [Previous](#docs/15-modules.md) | [Next](#docs/17-async.md)</small>