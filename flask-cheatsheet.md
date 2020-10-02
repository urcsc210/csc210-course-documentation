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

### Git Repository used by the book

Follow along with the code samples from the book, **Flask Web Development**, *(Miguel Grinberg)* by using Git to clone the book's repository in GitHub

-  Initial setup: in any subdirectory where it makes sense to keep development files<br>at CLI: `git clone https://github.com/miguelgrinberg/flasky.git`
- Then follow the book's instructions; at CLI: `git checkout 1a` ...and then 1b, 1c, et cetera as indicated by the lemur icons throughout the book
- If needed, to a hard reset to baseline your files with Git; at CLI: `git reset --hard`

*Note: the sync'd files from GitHub are meant to be viewed and studied.  Don't edit them else you'll fall out of sync with the repository.*

## Setup a New Project

You need to do the following *each time* you start a new project OR you need to re-create a virtual environment

- Create a new project folder anywhere in your file system then...
  - at CLI: `cd` into the project folder
- Use a module (-m) in Python to install a virtual environment named *venv*<br>*(could be named anything but "venv" is standard)*
  - at CLI: `python3 -m venv venv`
- Activate the environment<br>at CLI (mac): `source venv/bin/activate`<br>
  at CLI (win): `venv\Scripts\activate`<br>
  ...notice your prompt change; indicates that you're working in a private python environment 
- Install Flask<br>
  at CLI: `pip install flask`
- IF you need to use an app file *different* than **app.py**, set the environment variable so Python can find the app (else skip this step)<br>
  at CLI (mac): `export FLASK_APP=hello.py`<br>
  at CLI (win): `set FLASK_APP=hello.py`

### Test the environment (Hello World!)

If you're creating a new project from scratch (i.e. there aren't any **.py** files there already), you need to make sure everything is setup correctly; write a simple Hello World! application.

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

### Freeze Requirements

When building an application it's common to add modules to extend Flask's capabilities.  After installation, you need to remember to "freeze" (take a snapshot) of the modules your app needs by creating a **requirements.txt** file

- At the CLI: `pip freeze > requirements.txt`

### New Project Command Summary

Mac zsh or bash...

```bash
python3 -m venv venv
source venv/bin/activate
pip install flask
export FLASK_ENV=development
export FLASK_APP=hello.py #...only if not using app.py
pip freeze > requirements.txt #...after installing new modules only
flask run #...then Ctrl-C to exit
```

Windows CMD...

```bash
python3 -m venv venv
venv/bin/activate
pip install flask
set FLASK_ENV=development
set FLASK_APP=hello.py #...only if not using app.py
pip freeze > requirements.txt #...after installing new modules only
flask run #...then Ctrl-C to exit
```

## Restart an Existing Project

After setting up a new project, you can leave (close the CLI) and come back later.  To pick-up where you left off:

- In a CLI: `cd` into the project folder
- Reactivate the environment<br>at CLI (mac): `source venv/bin/activate`<br>
  at CLI (win): `venv\Scripts\activate`<br>
  ...notice your prompt change; indicates that you're working in a private python environment
- Reset environment variable to indicate the app file (only if *not* using **app.py**)<br>
  at CLI (mac): `export FLASK_APP=hello.py`<br>
  at CLI (win): `set FLASK_APP=hello.py`
- Reset debug mode if you're planning to use it<br>
  at CLI (mac): `export FLASK_ENV=development`<br>
at CLI (win): `set FLASK_ENV=development` 
- Start the WSGI server (web server)<br>
  at CLI: `flask run`
- Open a web browser; try​ these URLs:
  - [http://127.0.0.1:5000/](http://127.0.0.1:5000/)
- Kill the web server<br>
  at CLI: Control-C

### Restart Command Summary

Mac zsh or bash...

```bash
source venv/bin/activate
export FLASK_ENV=development
export FLASK_APP=hello.py #...only if not using app.py
pip install -r requirements.txt #...if custom modules were used
flask run #...then Ctrl-C to exit
```

Windows CMD...

```bash
venv/bin/activate
pip install flask
set FLASK_ENV=development
set FLASK_APP=hello.py #...only if not using app.py
pip install -r requirements.txt #...if custom modules were used
flask run #...then Ctrl-C to exit
```