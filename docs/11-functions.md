## Functions

### Definition

Functions can have parameters with default values.

```lunite
func greet(name="World") {
    return f"Hello, {name}!"
}
```

### Lambdas (Anonymous Functions)

```lunite
let square = (x) => x * x
out(square(5)) ~~ Prints 25
```

### Named Arguments

You can call functions using specific argument names, regardless of order.

```lunite
func box_vol(w, h, l) {
    return w * h * l
}

~~ Order doesn't matter when you use named args
let v = box_vol(h=10, l=5, w=2)
```

### Decorators

Decorators allow you to wrap a function with another function to modify its behavior. In Lunite, decorators work for both internal Lunite functions and imported Python functions.

Function properties (can be used by decorators):

`f.name`: function name

`f.params`: list of parameters of the function

`f.is_lambda`: if function `f` is a lambda, it returns `true` else `false`

```lunite
func log(f) { ~~ f is the wrapped function
    func wrapper() {
        out("Calling function: " + f.name)
        return f()
    }
    return wrapper
}

@log ~~ using a decorator
func hi() {
    out("Hi!")
}

hi()
```

---

<small>Docs Page 11 | [Previous](#docs/10-control-flow.md) | [Next](#docs/12-oop.md)</small>