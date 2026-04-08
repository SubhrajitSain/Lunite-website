## Variables & Types

### Declaration

Variables are declared using the `let` keyword.

```lunite
let age = 21            ~~ Mutable variable
let mylist = [1, 2, 3]  ~~ List variable example
let const PI = 3.14159  ~~ Constant (cannot be changed)
let [a, b] = [9, 12]    ~~ Destructuring assignment

let x      ~~ Declared but not initialized
out(x)     ~~ null
x = 16 * 2
out(x)     ~~ 32
```

### Data Types

Lunite supports standard types and some specific low-level wrappers.

| **Type** | **Description** | **Example** |
| --- | --- | --- |
| `int` | Integer numbers | `10`,`-5` |
| `float` | Floating point | `10.5`,`.5` |
| `bool` | Boolean | `true`,`false` |
| `string` | Text string | `"Hello"`,`f"Age: {x}"` |
| `char` | Single character | `'a'`,`'1'` |
| `bit` | 0 or 1 | `bit(1)` |
| `byte` | 0 to 255 | `byte(255)` |
| `list` | Ordered collection | `[1, 2, 3]` |
| `dict` | Key-Value pairs | `{"key": "value"}` |
| `set` | Non-repeating list | `{'A', 'B', 'C'}` |
| `tuple` | Immutable fixed-size list | `(10, 20)` |
| `null` | Empty value | `null`  |

### Advanced List Features

- **Slicing:** Extract sub-lists using `[start:end]`.
    
    ```lunite
    let numbers = [10, 20, 30, 40, 50]
    let subset = numbers[1:4]  ~~ [20, 30, 40]
    let first_two = numbers[:2] ~~ [10, 20]
    ```
    
- **Pre-allocation:** Initialize lists with a size and type hint using `list(size, type)`.
    
    ```lunite
    let matrix = list(5, "list") ~~ Creates [[], [], [], [], []]
    let zeros = list(100, "int") ~~ Creates [0, 0, ... 0]
    ```


---

<small>Docs Page 8 | [Previous](#docs/07-tokens-keywords.md) | [Next](#docs/09-operators.md)</small>