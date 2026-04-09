## Standard Library

### Global Functions

Core functions available everywhere without a prefix.

- `out(msg)`: Prints to console.
- `in(prompt, type_hint)`: Gets input. Type hint `type_hint` optional ("int", "float", "bool", "bit", "byte", "char"). Passwords can be input when `type_hint` is "pass".
- `len(obj)`: Returns length of string, list, or dict.
- `type(obj)`: Returns the type name of the object.
- `list(num, type_hint)`: Initializes a list with `n` elements and of type `type_hint` ("int", "float", etc.).
- `range(start, end)`: Returns a list of integers from `start` to `end` (inclusive).
- `raise(msg)`: Raises a runtime exception with the given message.
- **Casts:** `str(x)`, `int(x)`, `float(x)`, `bool(x)`, `bit(x)`, `byte(x)`, `char(x)`, `bytes(list)`.

---

### Math

Accessed via the `Math` object.

- `Math.pi`: The constant π.
- `Math.abs(x)`: Absolute value.
- `Math.pow(x, y)`: `x` to the power of `y`.
- `Math.sqrt(x)`: Returns the square root of `x`.
- `Math.round(x)`, `Math.floor(x)`, `Math.ceil(x)`: Rounding functions.
- `Math.log(x)`: Returns the normal logarithm (with base `e`) of `x`.
- `Math.log10(x)`: Returns base 10 logarithm of `x`.
- `Math.rad(deg)`: Converts degrees to radians.
- `Math.deg(rad)`: Converts radians to degrees.
- `Math.clamp(n, min, max)`: Restricts `n` to be in the range `min` to `max`.
- `Math.max(a, b, c, ...)`: Returns the greatest value in the arguments.
- `Math.min(a, b, c, ...)`: Returns the smallest value in the arguments.
- `Math.factorial(x)`: Returns the factorial of `x`.
- `Math.gcd(a, b)`: Returns the GCD of `a` and `b`.
- `Math.lcm(a, b)`: Returns the LCM of `a` and `b`.
- `Math.hypot(x, y)`: Returns the 2D hypotenuse with coordinates `x` and `y`.
- **Trigonometry:** `Math.sin(x)`, `Math.cos(x)`, `Math.tan(x)`, `Math.asin(x)`, `Math.acos(x)`, `Math.atan(x)`.

---

### Random

Accessed via the `Random` object.

- `Random.random()`: Returns a pseudo-random floating-point number ≥0.0, and <1.0
- `Random.randint(a, b)`: Returns a random integer in integer range `a` to `b`.
- `Random.uniform(a, b)`: Returns a random float in float range `a` to `b`.
- `Random.randrange(start, stop, step)`: Returns a random integer number in the range `start` to `stop` (exclusive) and with `step` steps (optional).
- `Random.seed(a)`: Initialize the RNG seed with `a` if specified or else random.
- `Random.choice(l)`: Returns a random element from the list, tuple or string `l`.
- `Random.shuffle(l)`: Randomly shuffle and return elements in list `l`.
- `Random.sample(l, k)`: Returns a `k` length list of unique elements chosen from the list, tuple or set.

---

### File System & I/O

Accessed via the `File` object.

- `File.read(path)`: Returns file content as string.
- `File.write(path, content)`: Writes string to file.
- `File.read_bytes(path)`: Reads file as raw binary data.
- `File.write_bytes(path, data)`: Writes binary data to file.
- `File.exists(path)`: Returns true if file/directory exists.
- `File.mkdir(path)`: Creates a directory.
- `File.rmdir(path)`: Removes an empty directory.
- `File.remove(path)`: Deletes a file.
- `File.list(path)`: Returns list of files in directory.
- `File.cwd()`: Returns current working directory.
- `File.join(part1, part2)`: Joins path segments safely.
- `File.append(path, content)`: Append the string `content` to the end of the file at `path`.
- `File.is_file(path)`: Returns `true` if `path` is a file else `false`.
- `File.is_dir(path)`: Returns `true` is `path` is a directory else `false`.
- `File.abs(path)`: Returns the absolute path of `path`.
- `File.base(path)`: Returns the filename component of `path`.
- `File.ext(path)`: Returns the file extension of `path`.
- `File.size(path)`: Returns file size of `path` in bytes.

---

### Network & JSON

Accessed via `Net` and `Json` objects.

- `Net.get(url)`: Performs an HTTP GET request.
- `Net.post(url, data)`: Performs an HTTP POST request.
- `Net.download(url, path)`: Downloads a file at `url` and saves it to the disk at `path`.
- `Json.encode(obj)`: Converts an object (dict/list) to a JSON string.
- `Json.decode(str)`: Parses a JSON string into an object.

---

### System

Accessed via the `Sys` object.

- `Sys.cmd(command)`: Executes a shell command and returns output.
- `Sys.os()`: Returns operating system name (e.g., 'Windows', 'Linux').
- `Sys.arch()`: Returns system architecture.
- `Sys.args()`: Returns command line arguments.
- `Sys.set_env(key, val)`: Sets an environment variable `key` to `val`.
- `Sys.env(key)`: Gets an environment variable `key`.
- `Sys.exit(code)`: Terminates the program.

---

### String Utils

Accessed via the `String` object.

- `String.upper(s)`: Converts to uppercase.
- `String.lower(s)`: Converts to lowercase.
- `String.trim(s)`: Removes whitespace from ends.
- `String.replace(s, old, new)`: Replaces substrings.
- `String.split(s, delimiter)`: Splits string into a list.
- `String.join(list, delimiter)`: Joins a list into a string.
- `String.starts_with(s, prefix)`: Returns `true` if `s` begins with `prefix` else `false`.
- `String.ends_with(s, suffix)`: Returns `true` if `s` ends with `suffix` else `false`.
- `String.includes(s, sub)`: Returns `true` if `sub` is in `s` else `false`.
- `String.index(s, sub)`: Returns index of first occurrence of `sub` inside `s`, or `-1` if `sub` is not found in `s`.
- `String.char_at(s, index)`: Returns the character at `index` in `s`.
- `String.is_alpha(s)`: Returns `true` if all characters are letters else `false`.
- `String.is_digit(s)`: Returns `true` if all characters are digits else `false`.
- `String.pad_start(s, len, char)`: Returns the padded string `s` after padding the start of `s` by repeating the character `char` at the start until the length of `s` is `len`.
- `String.pad_end(s, len, char)`: Returns the padded string `s` after padding the end of `s` by repeating the character `char` at the end until the length of `s` is `len`.

---

### Time

Accessed via the `Time` object.

- `Time.now()`: Returns current Unix timestamp.
- `Time.sleep(seconds)`: Pauses execution.
- `Time.struct(timestamp)`: Returns a dictionary containing `{"year": y, "month": m, "day": d, "hour": h, "minute": min, "second": s, "weekday": w}`.
- `Time.format(fmt)`: Returns the time as per `fmt`, like: `"%Y-%m-%d"`.

---

### Regular Expressions

Accessed via the `Regex` object.

- `Regex.match(pattern, str)`: Checks if the beginning of string matches pattern.
- `Regex.search(pattern, str)`: Searches string for pattern.
- `Regex.find_all(pattern, str)`: Returns list of all matches.
- `Regex.replace(pattern, replacement, str)`: Returns modified string.

---

### List Operations

Accessed via the `List` object.

- `List.push(list, item)`: Appends `item` to the end of the list `list`.
- `List.pop(list, index)`: Removes and returns the item at `index` in the list `list` (default index is the last position).
- `List.sort(list)`: Returns the list `list` after sorting it in ascending order.
- `List.reverse(list)`: Returns the list `list` after reversing the positions of the elements.
- `List.copy(list)`: Returns a shallow copy of `list`.
- `List.clear(list)`: Removes everything from the list.
- `List.contains(list, item)`: Returns `true` if `item` is in `list` else `false`.
- `List.index(list, item)`: Returns the index of `item` in `list` or `-1` if not found.
- `List.count(list, item)`: Returns the number of times `item` is in `list`.
- `List.extend(l1, l2)`: Appends elements from list `l2` into list `l1`.

---

### Dictionary Operations

Accessed via the `Dict` object.

- `Dict.keys(d)`: Returns a list of keys in the dictionary `d`.
- `Dict.values(d)`: Returns a list of values in the dictionary `d`.
- `Dict.items(d)`: Returns a list of `[key, value]` pairs.
- `Dict.has(d, key)`: Returns `true` if `key` is in `d`, else `false`.
- `Dict.remove(d, key)`: Removes `key` from the dictionary `d`.
- `Dict.merge(d1, d2)`: Returns a dictionary after merging `d1` and `d2`.

---

### Set Operations

Accessed via the `Set` object.

- `Set.add(s, v)`: Add value `v` to the set `s`.
- `Set.remove(s, v)`: Remove value `v` from the set `s`.
- `Set.has(s, v)`: Returns `true` if set `s` has value `v`, else `false`.
- `Set.union(s1, s2)`: Returns the union of the sets `s1` and `s2`.
- `Set.intersect(s1, s2)`: Returns the intersect of the sets `s1` and `s2`.
- `Set.diff(s1, s2)`: Returns the difference between the sets `s1` and `s2`.
- `Set.list(s)`: Convert and return set `s` as a list.

---

### Base64

Accessed via the `Base64` object.

- `Base64.encode(s)`: Returns Base64 encoded value of `s`.
- `Base64.decode(s)`: Returns Base64 decoded value of `s`.

---

### Hashing

Accessed via the `Hash` object.

- `Hash.sha256(s)`: Returns SHA-256 hash of string `s`.
- `Hash.md5(s)`: Returns MD5 hash of string `s`.

---

### Console Utilities

Accessed via the `Console` object.

- `Console.clear()`: Clears the console/terminal.
- `Console.read_pass(p)`: Reads and returns a password from the console, with optional string prompt `p`.
- `Console.size()`: Returns the size of the terminal in the format `{"columns": <cols>, "lines": <lines>}`.
- `Console.title(t)`: Set the title of the console window to `t`.

---

### Lunite Interpreter Metadata

Accessed via the `LuniteMeta` object.

- `LuniteMeta.version()`: Returns value of `LUNITE_VERSION_STR` constant.
- `LuniteMeta.copyright()`: Returns value of `COPYRIGHT` constant.
- `LuniteMeta.user_agent()`: Returns value of `LUNITE_USER_AGENT` constant.
- `LuniteMeta.current_file()`: Returns current value of `CURRENT_FILE` global variable.
- `LuniteMeta.keywords()`: Returns the list of all keywords (`KEYWORDS` constant list).
- `LuniteMeta.regex_num()`: Returns the compiled regex object for numbers (`RE_NUM` constant).
- `LuniteMeta.regex_id()`: Returns the compiled regex object for identifiers (`RE_ID` constant).

---

<small>Docs Page 14 | [Previous](#docs/13-access-modifiers.md) | [Next](#docs/15-modules.md)</small>