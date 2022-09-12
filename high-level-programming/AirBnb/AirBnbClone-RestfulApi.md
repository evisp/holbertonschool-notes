# REST API

- REST API is a software architectural style for Backend.
- REST = “REpresentational State Transfer”. API = Application Programming Interface
- REST API is Resource-based, a resource is an object and can be access by a URI. An object is “displayed”/transferred via a representation (typically JSON)
- There are 6 constraints
  1. **Uniform Interface** defined the interface between client and server
     - HTTP methods `GET, POST, PUT, DELETE`
     - Acess a resource through URI, as in `GET /users/12`
  2. **Stateless**
     - The server is independent of the client. The server doesn’t store user client information/state
  3. **Cacheable**
     - All server responses (resource representation) are cacheable:
  4. **Client-Server**
     - REST API is designed to separate Client from the Server. The server doesn’t know who is talking to it. Clients are not concerned with data storage
  5. **Layred System**
     - Client can’t assume direct connection to server. Intermediary servers may improve system scalability by enabling load-balancing and by providing shared caches
  6. **Code on demand (optional)**
     - Server can temporarily: transfer logi to client, allow client to execute logic

## Learn REST: A RESTful tutorial

### Designing a simple web service

- The task of designing a web service or API becomes an exercise in identifying the resources that will be exposed and how they will be affected by the different request methods
- Let's say we want to write a To Do List application and we want to design a web service for it as in `http://[hostname]/todo/api/v1.0/`
- The next step is to select the resources that will be exposed by this service.
  - `GET` to retreive tasks as in `http://[hostname]/todo/api/v1.0/tasks`
  - `POST` to create a new task as in `http://[hostname]/todo/api/v1.0/tasks`
  - `GET` or `PUT` to create/update a task as in `http://[hostname]/todo/api/v1.0/tasks/[task_id]`

### A brief introduction to the Flask microframework

- Using Flask, let's create a simple web application, which we will put in a file called `app.py`
```Python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def index():
    return "Hello, World!"

if __name__ == '__main__':
    app.run(debug=True)
```

### Implementing RESTful services in Python and Flask

[Here](https://blog.miguelgrinberg.com/post/designing-a-restful-api-with-python-and-flask) you can find the complete tutorial

- The clients of our web service will be asking the service to add, remove and modify tasks, so clearly we need to have a way to store tasks.
- Using the base Flask application we are now ready to implement the first entry point of our web service

```Python
from flask import Flask, jsonify

app = Flask(__name__)

tasks = [
    {
        'id': 1,
        'title': u'Buy groceries',
        'description': u'Milk, Cheese, Pizza, Fruit, Tylenol', 
        'done': False
    },
    {
        'id': 2,
        'title': u'Learn Python',
        'description': u'Need to find a good Python tutorial on the web', 
        'done': False
    }
]

@app.route('/todo/api/v1.0/tasks', methods=['GET'])
def get_tasks():
    return jsonify({'tasks': tasks})

if __name__ == '__main__':
    app.run(debug=True)
```

- Instead of the index entry point we now have a `get_tasks` function that is associated with the `/todo/api/v1.0/tasks` URI, and only for the `GET HTTP` method
- We can view using `curl -i http://localhost:5000/todo/api/v1.0/tasks`
- Now let's write the second version of the `GET` method for our tasks resource.

```Python
from flask import abort

@app.route('/todo/api/v1.0/tasks/<int:task_id>', methods=['GET'])
def get_task(task_id):
    task = [task for task in tasks if task['id'] == task_id]
    if len(task) == 0:
        abort(404)
    return jsonify({'task': task[0]})
```
- To generate own-defined error messages we can use

```Python
from flask import make_response

@app.errorhandler(404)
def not_found(error):
    return make_response(jsonify({'error': 'Not found'}), 404)
```