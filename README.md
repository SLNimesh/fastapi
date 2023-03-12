# API Development with Python - FastAPI

## Setting up development env

- Visual Studio Code is used as the IDE.
- Install `Python` extension.

> Virtual Environment

- Install [virtualenv](https://virtualenv.pypa.io/en/latest/index.html) using pip.

```ps
    pip install virtualenv
```

- Creat a virtualenv.

```ps
    python -m virtualenv env
```

- Activate virtual env using the `activate.ps1` (*for powershell*) script.

```ps
    cd env
    Scripts/activate
```

- In order to make sure check the interpreter (*the one inside the scripts folder*) used at the bottom of the VS Code.

> Remove virtualenv

- To deactivate the envrinoment run command `deactivate` inside the virtual env.

```ps
    (env) PS ...\venv> deactivate
```

- Remove the created *env* folder.

---
&nbsp;

> requirements.txt file

❕ *Follow this once the vitual env is setup and activated. (.. used to create the requirements.txt file outside the env folder)*

- Used to keep track of all the dependecies installed in the project.

```sh
    pip install -r ../requirements.txt
```

- To generrate the `requirements.txt` file use `pip freeze` command.

```sh
    pip freeze > ../requirements.txt
```

---
&nbsp;

## Project Structure

- This project is organized under the file structure mentioned in the fast api [documentation](https://fastapi.tiangolo.com/tutorial/bigger-applications/).

````txt
.
├── app                  # "app" is a Python package
│   ├── __init__.py      # this file makes "app" a "Python package"
│   ├── main.py          # "main" module, e.g. import app.main
│   ├── dependencies.py  # "dependencies" module, e.g. import app.dependencies
│   └── routers          # "routers" is a "Python subpackage"
│   │   ├── __init__.py  # makes "routers" a "Python subpackage"
│   │   ├── items.py     # "items" submodule, e.g. import app.routers.items
│   │   └── users.py     # "users" submodule, e.g. import app.routers.users
│   └── internal         # "internal" is a "Python subpackage"
│       ├── __init__.py  # makes "internal" a "Python subpackage"
│       └── admin.py     # "admin" submodule, e.g. import app.internal.admin
````

---
&nbsp;

## Database (NoSQL)

- Using [NoSQl databases](https://fastapi.tiangolo.com/advanced/nosql-databases/) with fast api.

- According to MongoDb's official [documentation](https://www.mongodb.com/docs/drivers/pymongo/), `PyMongo` is used for synchronous python apps.
