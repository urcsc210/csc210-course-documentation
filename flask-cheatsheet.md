# Flask Cheatsheet

There are three things you need to know when developing web applications in Flask:

- One-time initial install of Python3
- Setup a new project
  - ...and test the environment (Hello World!)
- Restart an existing project

## One-time Initial Install

You only need Python3 installed on your computer and have it properly set in your system environment's PATH

- Check: at CLI `python3 --version` or `where python3`<br>If response is good, you're good to go
- Else install or re-install Python from [www.python.org](https://www.python.org/)<br>Make sure your python3 installation is in your system's PATH

## Setup a New Project

You need to do the following *each time* you start a new project

- Create a new project folder anywhere in your file system then...
  - at CLI: `cd` into the project folder
- Use a module (-m) in Python to install a virtual environment named *venv*<br>*(could be named anything but "venv" is standard)*
  - at CLI: `python3 -m venv venv`
- Activate the environment<br>at CLI (mac): `source venv/bin/activate`<br>
  at CLI (win): `venv\Scripts\activate`<br>
  ...notice your prompt change; indicates that you're working in a private python environment 
- Install Flask<br>
  at CLI: `pip install flask`
- IF you need to use an app file *different* than **app.py**, set the environment variable (else skip this step)<br>
  at CLI (mac): `export FLASK_APP=hello.py`<br>
  at CLI (win): `set FLASK_APP=hello.py`

### Test the environment (Hello World!)

To make sure everything is setup correctly, write a simple Hello World! application.

- In the project folder, create a test file, e.g. **app.py**<br>*(.py is for Python)*

- In the **app.py** file, write a basic application<br>(Beware: Python syntax! Whitespace is important.)

```python
from flask import Flask
app = Flask(__name__)

@app.route('/')
def index():
	return "<h1>Hello World!</h1>"
```

...save the file.

- IF you are planning to use debug mode (and you are, usually) set the environment variable (else skip this step)<br>
  at CLI (mac): `export FLASK_ENV=development`<br>
at CLI (win): `set FLASK_ENV=development` 
- Start the WSGI server (web server)<br>
  at CLI: `flask run`
- Open a web browser; try​ these URLs:
  - [http://127.0.0.1:5000/](http://127.0.0.1:5000/)
- Kill the web server when you're done or need to change something in the environment<br>
  at CLI: Control-C

## Restart an Existing Project

After setting up a new project, you can leave (close the CLI) and come back later.  To pick-up where you left off:

- In a CLI: `cd` into the project folder
- Reactivate the environment<br>at CLI (mac): `source venv/bin/activate`<br>
  at CLI (win): `venv\Scripts\activate`<br>
  ...notice your prompt change; indicates that you're working in a private python environment
- Reset environment variable<br>
  at CLI (mac): `export FLASK_APP=hello.py`<br>
  at CLI (win): `set FLASK_APP=hello.py`

- Start the WSGI server (web server)<br>
  at CLI: `flask run`

- Open a web browser; try​ these URLs:
  - [http://127.0.0.1:5000/](http://127.0.0.1:5000/)
- Kill the web server<br>
  at CLI: Control-C