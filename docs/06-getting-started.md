## Getting Started

### Hello, World!

I think this is the most important part of any programming language. So here it is, in all its glory, in Lunite.

```lunite
out("Hello, World!")
```

### CLI Usage

Lunite acts as both an interpreter and a compiler (using PyInstaller).

**Lunite REPL (Interactive Shell):** Run without arguments to enter live coding mode. Inspiration taken from Python’s REPL.

```bash
python lunite.py
```

**Run a Lunite Script:** Interprets and executes the file provided.

```bash
python lunite.py run program.luna
```

**Build and Compile to Executable:** Creates a standalone executable in the `dist` folder with PyInstaller.

```bash
python lunite.py build program.luna
```

**Clean Build Directories:** Delete the `build` and the `dist` folder created when compiling a Lunite program.

```bash
python lunite.py clean
```

**Display Version Information:** To check what version of Lunite you have, run:

```bash
python lunite.py version
```

### Make `lunite` Command

If you do not want to use the long `python` [`lunite.py`](http://lunite.py) prefix mentioned above to use Lunite, you can build the `lunite` or `lunite.exe` executable by following the steps mentioned above in **How to Build Lunite Executable**. If you do not prefer making an executable, you can just make the [lunite.py](http://lunite.py) script into an executable command by following these steps:

**On Linux:**

Rename `lunite.py` to your desired command name, e.g., `lunite`.

```bash
mv -v lunite.py lunite   # rename the script
```

Make the command executable.

```bash
sudo chmod +x lunite     # make it executable
```

Move the new command to a preferred directory, e.g., `/etc/lunite`

```bash
# make sure there is a directory, e.g., /etc/lunite
mkdir -pv /etc/lunite

# move the newly executable script to the directory
mv -v lunite /etc/lunite/lunite
```

Add the directory to the path.

```bash
# add the directory to PATH
export PATH="$PATH:/etc/lunite"
```

**On Windows:**

Put `lunite.py` in a permanent location according to your choice, e.g., `C:\Lunite\lunite.py`.

Create a file called `lunite.bat` in the same folder with:

```batch
@echo off
python "C:\lunite\lunite.py" %*
```

Add `C:\lunite` (or whatever you chose) to PATH:

- Press `Win + R` and enter: `sysdm.cpl`
- In the window, click `Advanced` and then `Environment Variables` button.
- Edit Path and add `C:\lunite`

Restart your terminal after doing the above.

**On MacOS:**

Rename the `lunite.py` to `lunite`.

```bash
mv -v lunite.py lunite
```

Make it executable:

```bash
sudo chmod +x lunite
```

Move it to a location already in PATH (CHOOSE ONE OF THESE):

```bash
sudo mv -v lunite /usr/local/bin/lunite
```

OR for Apple Silicon:

```bash
sudo mv -v lunite /opt/homebrew/bin/lunite
```

### File Extension

Lunite's file extension is `.luna`. Why `.luna` you may ask? Because “Lunite” in my terms means “moon rock” or “moon crystal”, and “luna” is a synonym for “moon”. So I chose `.luna` to be the file extension.

### Line Terminator/Delimiter

Lunite has an optional line terminator, `;` for using multiple statements on the same line.

```lunite
let a = 1; let b = 3; out(a + b); ~~ Outputs 4
```

### Comments

**Single Line:** `~~ This is a single line comment`

**Multi-Line:**

`~* This is single line block comment *~`, or you could do:

```lunite
~*
 * This is a multi-line comment
 * Another line!
 *~
```

… or this as well:

```lunite
~*
This works as well as the above one.
Because only the starting and ending characters matter.
*~
```

---

<small>Docs Page 6 | [Previous](#docs/05-manual.md) | [Next](#docs/07-tokens-keywords.md)</small>