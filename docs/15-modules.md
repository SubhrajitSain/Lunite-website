## Modules

### Import Lunite Modules

You can split code into multiple files or modules. Note that importing a Lunite file loads it as an object (namespace). Only `public` members and methods are imported.

`utils.luna`:

```lunite
func help() {
    out("Helping...")
}
```

`mylib/hello.luna`:

```lunite
func hello() {
    out("Hello, Lunite!")
}
```

`main.luna`:

```lunite
import "utils"              ~~ Creates an object 'utils'
import "./mylib/hello.luna" ~~ Creates an object 'hello'

utils.help()                ~~ Access functions via object
hello.hello()
```

### Import Python Modules

You can also import Python modules using import_py. Example:

```lunite
import_py "math"         ~~ Creates a 'math' object
import_py sqrt from math ~~ Imports 'sqrt' directly

out("Value of Pi: " + str(math.pi))
out("Square root of 16: " + str(sqrt(16)))
```

### Import Lunite Modules/Files in Python

Lunite 1.9.8+ comes with `lunamod.py`, a Python module that you can use to import and use Lunite modules with.

```lunite
~~ Lunite module app.luna
import_py Flask from flask

let app = Flask("Lunite Flask real!")

@app.route("/", methods=["GET"])
func index() {
    return "Hello from Lunite Flask!"
}

@app.route("/ping", methods=["GET"])
func ping() {
    return "pong"
}
```

```python
# Python WSGI server
import lunamod
from gevent.pywsgi import WSGIServer

module = lunamod.import_module("app") # Lunite module is app.luna
app = module.app

http_server = WSGIServer(("0.0.0.0", 8000), app)
http_server.serve_forever()
```

### Python Flask Webserver

Lunite 1.9.7 added support for Python Flask webservers. The one given below is a sample Flask app made in Lunite. Templates are not provided for the sake of reading, they can be assumed to be normal Flask templates.

```lunite
import_py Flask from flask
import_py jsonify from flask
import_py abort from flask
import_py render_template from flask
import_py send_from_directory from flask

let app = Flask("__name__")

~~ note: you need a `index.html` (any html file) in `templates`
~~       you also need to have a `static` folder with some files

@app.route("/")
func index() {
    return render_template("index.html", title="Lunite Home")
}

@app.route("/api/status")
func status() {
    return jsonify({"status": "online", "version": "1.9.7"})
}

@app.route("/admin")
func admin() {
    return abort(401)
}

@app.route("/files/<path>")
func get_file(path) {
    return send_from_directory("static", path)
}

app.run(debug=true, host="0.0.0.0", port=8080)
```

---

<small>Docs Page 15 | [Previous](#docs/14-stdlib.md) | [Next](#docs/16-macros.md)</small>