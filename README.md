# docker-todo-project
PROJECT OVERVIEW

Docker Todo App is a lightweight task management web application built with Python Flask and containerized using Docker. It allows users to add, complete, and delete tasks through a clean browser interface, with data persisted locally in a JSON file.
How it works
The user opens the app in their browser on localhost:5000. Requests are handled by a Flask backend (app.py) which reads and writes tasks to a todos.json file. The UI is rendered using a Jinja2 HTML template. The entire application runs inside a Docker container, making it easy to run on any machine without manual setup.

HOW IT WORKS

The user opens the app in their browser on localhost:5000. Requests are handled by a Flask backend (app.py) which reads and writes tasks to a todos.json file. The UI is rendered using a Jinja2 HTML template. The entire application runs inside a Docker container, making it easy to run on any machine without manual setup.

Tech Stack

LayerTechnologyBackendPython 3.11, FlaskFrontendHTML, CSS (Jinja2 templating)StorageJSON fileContainerDocker, Docker Compose

