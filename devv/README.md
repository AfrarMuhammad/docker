# Flask Application

This project is a simple Flask web application that returns a greeting message.

## Project Structure

```
[project-name]
├── app
│   └── app.py
├── Dockerfile
└── README.md
```

## Requirements

- Docker

## Building the Docker Image

To build the Docker image for the Flask application, run the following command in the project directory:

```
docker build -t flask-app .
```

## Running the Docker Container

After building the image, you can run the Docker container using the following command:

```
docker run -p 5000:5000 flask-app
```

You can then access the application by navigating to `http://localhost:5000` in your web browser.

## Application Details

The application is a simple Flask app that responds with "Hello from Flask App!" when accessed at the root URL (`/`).