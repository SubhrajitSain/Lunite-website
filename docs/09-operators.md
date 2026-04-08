## Operators

### Operators List

**Arithmetic:** `+`, `-`, `\*`, `/`, `%`, postfix/prefix: `++`, `--`

**Compound:** `+=`, `-=`, `*=`, `/=`, `%=`

**Comparison:** `==`, `!=`, `<`, `>`, `<=`, `>=`

**Logical:**

- AND: `&` or `and`
- OR: `||` or `or`
- NOT: `!` or `not`

**Bitwise:** `&` (AND), `|` (OR), `^` (XOR), `~` (NOT), `<<` (left shift), `>>` (right shift)

**Ternary:** `condition ? true_val : false_val` (e.g., `(a > b) ? a : b`)

**Type Check:** `variable is type` (e.g., `x is int`) instead of using `if str(type(variable)) == "Type"` (e.g., `if str(type(x)) == "Int"`)

### The Hierarchy

In Lunite, expressions are evaluated according to a specific hierarchy of operators, with the acronym **PUMASBRLTA** or **PUMAS B**ring **R**eal **L**ove **T**o **A**ll.

The order is: **P**rimary → **U**nary → **M**ultiplicative → **A**dditive →  **S**hift → **B**itwise → **R**elational → **L**ogical → **T**ernary → **A**ssignment

| **Acronym** | **Priority** | **Category** | **Operators** |
| --- | --- | --- | --- |
| **P** | 1 **(High)** | Primary | `()`, `[]`, `.` |
| **U** | 2 | Unary | `++`, `--`, `!`, `~`, `-`, `+` |
| **M** | 3 | Multiplicative | `*`, `/`, `%` |
| **A** | 4 | Additive | `+`, `-` |
| **S** | 5 | Shift | `<<`, `>>` |
| **B** | 6 | Bitwise | `&`, `^`, `|` |
| **R** | 7 | Relational | `>`, `<`, `>=`, `<=`, `==`, `!=`, `is`, `in` |
| **L** | 8 | Logical | `&&`/`and`, `||`/`or`, `!`/`not` |
| **T** | 9 | Ternary | `(<cond>) ? <true_expr> : <false_expr>` |
| **A** | 10 **(Low)** | Assignment | `=`, `+=`, `-=`, `*=`, `/=`, `%=` |

### Hierarchy Example Code

```lunite
~~ Multiplication (M) happens before Addition (A)
let x = 2 + 3 * 4   ~~ 2 + 12 = 14

~~ Logic (L) happens after Relations (R)
if (x > 10 && x < 20) { out("Yes" } ~~ Yes

~~ Parentheses (P) override everything
let y = (2 + 3) * 4 ~~ 5 * 4 = 20
```

---

<small>Docs Page 9 | [Previous](#docs/08-variables-types.md) | [Next](#docs/10-control-flow.md)</small>