# Anythink Market Servers

This project contains both a FastAPI server implemented in Python and an Express server implemented in Node.js. Both servers provide the same API routes for managing a task list. The Node.js server was created by migrating the endpoints from the Python server.

## Project Structure

The project has the following files and directories:

- `python-server/src/main.py`: This file contains the implementation of the FastAPI server with API routes. It handles adding a task to a list and retrieving the list.

- `python-server/src/__init__.py`: This file is an empty file that marks the `src` directory as a Python package.

- `python-server/requirements.txt`: This file lists the dependencies required for the FastAPI server.

- `python-server/Dockerfile`: This file is used to build a Docker image for the FastAPI server. It specifies the base image, copies the source code into the image, installs the dependencies, and sets the command to run the server.

- `node-server/server.js`: This file contains the implementation of the Express server with the same API routes as the Python server.

- `node-server/package.json`: This file lists the dependencies required for the Express server.

- `node-server/Dockerfile`: This file is used to build a Docker image for the Express server. It specifies the base image, copies the source code into the image, installs the dependencies, and sets the command to run the server.

- `docker-compose.yml`: This file is used to define and run multi-container Docker applications. It specifies the services to run, their configurations, and any dependencies between them.

## Getting Started

To run both servers using Docker, follow these steps:

- Build and start the Docker containers by running the following command:

  ```shell
  docker compose up
  ```

  This command will build the Docker images for both servers and start the containers defined in the `docker-compose.yml` file.

- The FastAPI server should now be running on port `8000`.
- The Express server should now be running on port `8001`.

## API Routes

Both servers provide the same API routes:

- `GET /`: Returns "Hello World".

- `POST /tasks`: Adds a task to the task list. The request body should be JSON with a `text` field containing the task.

- `GET /tasks`: Retrieves the task list as JSON.

## Migration Details

The Node.js Express server was created by migrating the API endpoints from the Python FastAPI server. The endpoints were translated to use Express.js, maintaining the same functionality and response formats.
