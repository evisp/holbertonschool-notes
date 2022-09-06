# AirBnB clone - Web framework

## What is a web framework

- A web framework is a software framework that is designed to support the development of web applications including web services, web resources and web API
- frameworks offer a set of features that you can use to create a custom application

### Types of Web frameworks

- **Server-side Frameworks**
  - The rules and architecture of the server-side frameworks permit you to create simple pages, landings and forms of different kinds.
  - Server-side frameworks handle HTTP requests, database control and management, URL mapping, etc
   - Example: `.NET, Django (Python), Express (JavaScript)`
- **Client-side Frameworks**
  - They function inside the browser. Therefore, you can enhance and implement new user interfaces
  - Examples: `Angular, React.js, Vue.js`

### Web application framework- Architecture

- Most of the web frameworks depend on the MVC (Model-View-Controller) architecture.
  - The Model comprises of all the data, business logic layers, its guidelines and functions
  - The View is for the graphical representation of the data like graph or charts etc. It is the apps’ front-end
  - The Controller translates the input data into the scope of commands of the previous ones

## A Minimal Application with Flask

[This](https://flask.palletsprojects.com/en/2.0.x/quickstart/#a-minimal-application) tutorial provides details.

### What is Flask?

- Flask is a lightweight WSGI web application framework. It is designed to make getting started quick and easy, with the ability to scale up to complex applications
- Flask offers suggestions, but doesn't enforce any dependencies or project layout.
- A minimal Flask application looks something like this:

```Python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def hello_world():
    return "<p>Hello, World!</p>"
```

### HTML Escaping

- When returning HTML, any user-provided values rendered in the output must be escaped to protect from injection attacks
- HTML templates rendered with Jinja, will do this automatically.

```Python
from markupsafe import escape

@app.route("/<name>")
def hello(name):
    return f"Hello, {escape(name)}!"
```

### Routing

- Modern web applications use meaningful URLs to help users.
- Use the `route()` decorator to bind a function to a URL.

```Python
@app.route('/')
def index():
    return 'Index Page'

@app.route('/hello')
def hello():
    return 'Hello, World'
```

### Rendering Templates

- Generating HTML from within Python is not fun, and actually pretty cumbersome because you have to do the HTML escaping on your own to keep the application secure.
- Because of that Flask configures the `Jinja2` template engine for you automatically.
- To render a template you can use the `render_template()` method

```Python
from flask import render_template

@app.route('/hello/')
@app.route('/hello/<name>')
def hello(name=None):
    return render_template('hello.html', name=name)
```

- Here is an example template:

```html
<!doctype html>
<title>Hello from Flask</title>
{% if name %}
  <h1>Hello {{ name }}!</h1>
{% else %}
  <h1>Hello, World!</h1>
{% endif %}
```

## Jinja

[This](https://jinja.palletsprojects.com/en/2.9.x/templates/) tutorial
provides fulld details.

### Synopsis

- A Jinja template is simply a text file. Jinja can generate any text-based format
- A template contains variables and/or expressions, which get replaced with values when a template is rendered; and tags, which control the logic of the template.
- An example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>My Webpage</title>
</head>
<body>
    <ul id="navigation">
    {% for item in navigation %}
        <li><a href="{{ item.href }}">{{ item.caption }}</a></li>
    {% endfor %}
    </ul>

    <h1>My Webpage</h1>
    {{ a_variable }}

    {# a comment #}
</body>
</html>
```

### Variables

- Template variables are defined by the context dictionary passed to the template.
- Example: `{{ foo.bar }}`

### Control structures

```html
<h1>Members</h1>
<ul>
{% for user in users %}
  <li>{{ user.username|e }}</li>
{% endfor %}
</ul>
```