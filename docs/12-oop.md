## Object-Oriented Programming (OOP)

Lunite supports classes, inheritance, and constructors.

```lunite
class Animal {
    let name = "Unknown"
    
    func init(n) {
        this.name = n
    }
    
    func message() {
        out("...")
    }
}

class Dog extends Animal {
    func message() {
        return f"{this.name} says Woof!"
    }
}

let d = new Dog("Spike")
out(d.message()) ~~ Spike says Woof!
```

---

<small>Docs Page 12 | [Previous](#docs/11-functions.md) | [Next](#docs/13-access-modifiers.md)</small>