# 2. Getting Started

*Just a brief note: Only the concepts of the langauge are taught here, not how to install/run it. For that, check the documentation.*

## Hello, World!

The absolute, ginormous, ultimate question for a language is how to make a Hello World program in it. And, I would kid you not, it is...  

```lunite
out("Hello, World!")
```

Yes. Its that simple (unlike Java for instance). 

## Semicolons

Now, for the second most ginormous question, does it need semicolons? I think you already have the answer. No. But you can add semicolons at the end of statements and make one-liner programs.  

```lunite
out("Hi!"); out("How are you?")
```

The above snippet is completely valid.  

## Comments

Ah, the most important thing when it comes to annotations. **Comments**. So, how exactly **comments**? Well...  

For single line comments:  

```lunite
~~ yo this is cool
```

For multiline comments:

```lunite
~*
this is very nice
i am not kidding
*~
```

...or style it, like:  

```lunite
~*
 * this thing can host websites
 * i am being fr
 * halp me plis :3
 *~
```

## Some Global STDLIB Functions

These functions can be accessed globally throughout your programs. Totally not copied over from the docs.  
- `out(msg)`: Prints to console.
- `in(prompt, type_hint)`: Gets input. Type hint `type_hint` optional ("int", "float", "bool", "bit", "byte", "char"). Passwords can be input when `type_hint` is "pass".
- `len(obj)`: Returns length of string, list, or dict.
- `type(obj)`: Returns the type name of the object.
- `list(num, type_hint)`: Initializes a list with `n` elements and of type `type_hint` ("int", "float", etc.).
- `range(start, end)`: Returns a list of integers from `start` to `end` (inclusive).
- `raise(msg)`: Raises a runtime exception with the given message.
- **Casts:** `str(x)`, `int(x)`, `float(x)`, `bool(x)`, `bit(x)`, `byte(x)`, `char(x)`, `bytes(list)`.

<br>
<small>Lesson 2 | [Previous](#lessons/01-intro.md) - [Next](#lessons/03-values-and-datatypes.md)</small>