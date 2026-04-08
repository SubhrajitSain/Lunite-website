## Enumerations

Enums allow you to define a set of named constants. Similar to C++ syntax.

```lunite
enum Color {
    Red,
    Green,
    Blue
}

let c = Color.Green
out(c) ~~ Prints the integer value (e.g., 1)

if (c == Color.Green) {
    out("Go!")
}
```

---

<small>Docs Page 19 | [Previous](#docs/18-dict-set.md) | [Next](#docs/20-string-interpolation.md)</small>