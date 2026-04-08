## Asynchronous Functions

Asynchronous functions allow you to perform non-blocking operations. They are integrated with Python's `asyncio` event loop.

- **`async func`**: Declares a function that returns a coroutine.
- **`await`**: Pauses execution of the current function until the awaited coroutine finishes.

```lunite
async func fetch_db() {
    out("Connecting...")
    return "Maybe some data from DB?"
}

async func main() {
    out("Starting lookup...")
    let data = await fetch_db()
    out("Received: " + data)
}

main()
```

---

<small>Docs Page 17 | [Previous](#docs/16-macros.md) | [Next](#docs/18-dict-set.md)</small>