# Cross-Origin Resource Sharing (CORS)

- Cross-Origin Resource Sharing (CORS) is an HTTP-header based mechanism that allows a server to indicate any origins (domain, scheme, or port) other than its own from which a browser should permit loading resources
- The CORS mechanism supports secure cross-origin requests and data transfers between browsers and servers.
- In the simplest case, initialize the Flask-Cors extension with default arguments in order to allow CORS for all domains on all routes

```Python
from flask import Flask
from flask_cors import CORS

app = Flask(__name__)
CORS(app)

@app.route("/")
def helloWorld():
  return "Hello, cross-origin-world!"
```

### Resource specific CORS
- Alternatively, you can specify CORS options on a resource and origin level of granularity by passing a dictionary as the resources option, mapping paths to a set of options

```Python
app = Flask(__name__)
cors = CORS(app, resources={r"/api/*": {"origins": "*"}})

@app.route("/api/v1/users")
def list_users():
  return "user example"
```

### Route specific CORS via decorator

- Simply add `@cross_origin()` below a call to Flask’s `@app.route(..)`

```Python
@app.route("/")
@cross_origin()
def helloWorld():
  return "Hello, cross-origin-world!"
```