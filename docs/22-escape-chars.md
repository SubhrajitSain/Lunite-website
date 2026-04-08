## Escape Characters

| **Escape Character** | **Name** | **Description** |
| --- | --- | --- |
| `\n` | Newline | Moves the cursor to the next line. |
| `\r` | Carriage Return | Moves the cursor to the beginning of the current line. |
| `\t` | Tab | Inserts a standard horizontal tab. |
| `\h` | Horizontal Tab | Alias for`\t`, inserts a horizontal tab. |
| `\b` | Backspace | Moves the cursor back one position (deletes previous character in output). |
| `\0` | Null Character | Represents the null character (Unicode`\u0000`). |
| `\\` | Backslash | Inserts a literal backslash character. |
| `\'` | Single Quote | Inserts a single quote character (essential for`'`chars). |
| `\"` | Double Quote | Inserts a double quote character (essential for`"`strings). |
| `\uXXXX` | Unicode Character | Inserts a specific Unicode character defined by 4 hexadecimal digits (e.g.,`\u03A9`). |

---

<small>Docs Page 22 | [Previous](#docs/21-error-diagnostics.md) | [Next](#docs/23-post-script.md)</small>