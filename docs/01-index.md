# Lunite Docs

# Metadata

Copyright Lunite by ANW (Subhrajit Sain), 2025-2026

Lunite is a hybrid OOP + POP programming language made in Python. Visit [https://github.com/SubhrajitSain/Lunite](https://github.com/SubhrajitSain/Lunite) for more information, source code and downloads.

This is the official documentation for Lunite version **1.9.8**. Docs updated: May 6th, 2026.

If you find any errors in this documentation, please let us know. Docs have been moved from Notion to here.

# Preface

Lunite is a modern-day hybrid programming language that is a blend of OOP and POP principles, which help you to write code in many use cases like scripting, web backend development, data models or similar. Lunite's syntax is very simple and has a wide variety of pre-installed functions in its standard library, mostly from Python.  

To get started with Lunite, one does not require to be a professional programming expert, even I (a 15 year old when I started this project) have made multiple things in Lunite, including a [PythonAnywhere](https://pythonanywhere.com) website at [dih.pythonanywhere.com](https://dih.pythonanywhere.com) that runs Lunite + Flask (site might not be up as it is running on the free tier) using simple `import_py` imports (you will learn about these later as you read the docs).  

So, I hope this helps to get you started with Lunite, and if you have any issues, questions or suggestions, please feel free to contact me through my website at [anw.is-a.dev]("https://anw.is-a.dev"). You can share your Lunite creations too, I would really appreciate it. Let's build something cool!  

ANW, Developer of Lunite.  

---

## Table of Contents

Click the link for each item to jump to that section.

- **[How to Build Lunite Executable](#docs/02-build-lunite.md)**
- **[VS Code Extension Installation](#docs/03-vscode-ext.md)**
- **[Transpile Lunite Interpreter](#docs/04-transpile.md)**
- **[Lunite User Manual](#docs/05-manual.md)**
    -  ▸ [Getting Started](#docs/06-getting-started.md): CLI Usage, Make `lunite` Command, File Extension, Line Terminator/Delimiter, Comments
    -  ▸ [Tokens & Keywords](#docs/07-tokens-keywords.md): Keywords, Literals
    -  ▸ [Variables & Types](#docs/08-variables-types.md): Declaration, Data Types, Advanced List Features
    -  ▸ [Operators](#docs/09-operators.md): Operators List, The Hierarchy
    -  ▸ [Control Flow](#docs/10-control-flow.md): If / Else If / Else, Loops, Match (Switch-Case), Leap (Goto), Assertions, Error Handling
    -  ▸ [Functions](#docs/11-functions.md): Definition, Lambdas (Anonymous Functions), Named Arguments, Decorators
    -  ▸ [Object-Oriented Programming (OOP)](#docs/12-oop.md)
    -  ▸ [Access Modifiers](#docs/13-access-modifiers.md)
    -  ▸ [Standard Library](#docs/14-stdlib.md): Global Functions, Math, Random, File System & I/O, Network & JSON, System, String Utils, Time, Regular Expressions, List Operations, Dictionary Operations, Set Operations, Base64, Hashing, Console Utilities, Lunite Interpreter Metadata
    -  ▸ [Modules](#docs/15-modules.md): Import Lunite Modules, Import Python Modules, Import Lunite Modules/Files in Python, Python Flask Webserver
    -  ▸ [Macros](#docs/16-macros.md): Syntax & Usage
    -  ▸ [Asynchronous Functions](#docs/17-async.md)
    -  ▸ [Dict Or Set?](#docs/18-dict-set.md)
    -  ▸ [Enumerations](#docs/19-enum.md)
    -  ▸ [String Interpolation (f-strings)](#docs/20-string-interpolation.md)
    -  ▸ [Error Diagnostics](#docs/21-error-diagnostics.md)
    -  ▸ [Escape Characters](#docs/22-escape-chars.md)
- **[Post Script](#docs/23-post-script.md)**

---

<small>Docs Page 1 | [Next](#docs/02-build-lunite.md)</small>
