## Control Flow

### If / Else If / Else

```lunite
if (length > 6) {
    out("Big")
} else if (length > 10) {
    out("Very Big")
} else {
    out("Small")
}
```

### Loops

**While Loop:**

```lunite
while (x < 10) {
    x += 1
}
```

**For Loop:**

```lunite
for item in list {
    out(item)
}
for i in range(1, 10) {
		out(i)
}
```

**Control:** `break` (exit loop), `advance` (continue to next iteration).

### Match (Switch-Case)

```lunite
match (x) {
    1: out("One")
    2: out("Two")
    other: out("Something else")   ~~ Default
}
```

You can also break out of match cases:

```lunite
let status = 200

func check_cache() {
    return true
}

match (status) {
    200:
        if (check_cache()) { break }
        out("Downloading...")
    other:
        out("Error")
}

out("Done!")
```

### Leap (Goto)

Jump to a specific label or line number.

```lunite
{MyLabel}         ~~ This is a label.
out("Looping...")
leap MyLabel      ~~ Jumps back to {MyLabel}
leap 30           ~~ Jumps to line 30
```

### Assertions

Useful for debugging and validating assumptions. If the condition is false, the program halts with an error.

```lunite
let x = 10
assert(x > 5, "X must be greater than 5")

x--
assert(x == 9) ~~ Message is optional
```

### Error Handling

```lunite
attempt {
    let x = 10 / 0             ~~ Try to divide by 0
} rescue (e) {
    out(f"Error caught: {e}")  ~~ Exception handling
} finally {
    out(f"Finished!")          ~~ Final stuff like cleanup, etc.
}
```

---

<small>Docs Page 10 | [Previous](#docs/09-operators.md) | [Next](#docs/11-functions.md)</small>