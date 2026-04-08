## Access Modifiers

Lunite 1.9.6 came with access specifiers for variables, functions and classes.

- `public`: (Default) Accessible by other scripts when imported.
- `private`: Accessible to current script only.
- `global`: Accessible anywhere within the script, in any block.

Example code:

```lunite
let a = 1                        ~~ public, can be used by other scripts
let public b = 2
let private id = "123"           ~~ private, available to this file only
let global filename = "temp.log" ~~ global, can be accessed in the script anywhere

~~ the same can be done to functions and classes
func public global print(x) { out(x) }
class private Cat {
    func meow() {
        print("Meow!")
    }
}

let gary = new Cat()
gary.meow()
```

---

<small>Docs Page 13 | [Previous](#docs/12-oop.md) | [Next](#docs/14-stdlib.md)</small>