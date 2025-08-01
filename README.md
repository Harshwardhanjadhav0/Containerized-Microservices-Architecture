# 🚀 Project 2: Containerized Microservices Architecture

This project showcases a simple containerized architecture using a Python Flask web application and MongoDB, orchestrated with Docker Compose. It simulates a microservices environment suitable for learning containerization, inter-service communication, and environment-based configuration. The Flask app includes RESTful endpoints for logs, metrics, and health status, making it useful for DevOps and monitoring practice. MongoDB serves as the backend database, storing user input or test data.

The project is ideal for those beginning with Docker, Flask, and service orchestration principles in a DevOps context.

---

## 📖 Table of Contents

- [🔍 Project Overview](#-project-overview)
- [🧰 Built With](#-built-with)
- [📦 Features](#-features)
- [🚀 Getting Started](#-getting-started)
  - [✅ Prerequisites](#-prerequisites)
  - [📂 Folder Structure](#-folder-structure)
  - [📁 Clone the Repository](#-clone-the-repository)
  - [⚙️ Run the App with Docker Compose](#️-run-the-app-with-docker-compose)
- [🧪 Running Tests](#-running-tests)
- [🛠 Troubleshooting & Tips](#-troubleshooting--tips)
- [📅 Project Status](#-project-status)
- [👨‍💻 Author](#-author)

---

## 🔍 Project Overview

This project implements a **microservices-based architecture** where each service runs independently in its own container. It includes:

- ✅ A **Flask-based API service** for routing and response logic  
- ✅ A **Dockerfile** to containerize the Flask application  
- ✅ A **Docker Compose** setup to orchestrate containers  
- ✅ Endpoints for **health checks** (`/health`), **performance metrics** (`/metrics`), and **logging** (`/logs`)  
- ✅ A **unit test suite** (`test_app.py`) using Pytest  
- ✅ A **MongoDB** container to persist data  

---

## 🧰 Built With

- [Python (Flask)](https://flask.palletsprojects.com/)
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
- [MongoDB](https://www.mongodb.com/)
- [Pytest](https://docs.pytest.org/) – For testing

---

## 📦 Features

- **🧱 Containerized Architecture** – Entire app runs in isolated Docker containers for easier deployment and scalability.
- **⚡ Lightweight Flask App** – A fast and minimal API server ideal for microservice-based setups.
- **📡 Health Checks** – `/health` and `/metrics` endpoints help with service uptime monitoring and performance tracking.
- **📄 Logging Endpoint** – `/logs` provides access to application logs for debugging and observability.
- **🧪 Unit Testing Support** – Comes with `test_app.py` for verifying routes and application logic.
- **🔌 Port Configurable** – Easily modify exposed ports through `docker-compose.yml`.
- **💾 Data Persistence** – MongoDB container ensures persistent backend storage.

---

## 🚀 Getting Started

### ✅ Prerequisites

Make sure you have the following installed:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/)
- [Python 3+](https://www.python.org/downloads/) (optional for local testing)
- [pip](https://pip.pypa.io/en/stable/) (optional for local testing)

---

### 📂 Folder Structure

```bash
project-root/
├── app/                   # Flask app source code
│   ├── __init__.py
│   └── routes.py
├── Dockerfile             # Flask app Dockerfile
├── docker-compose.yml     # Compose file with Flask and MongoDB services
├── requirements.txt       # Python dependencies
└── test_app.py            # Pytest test cases
```

### 📁 Clone the Repository

```bash
git clone https://github.com/Harshwardhanjadhav0/microservices-flask-docker.git
cd microservices-flask-docker
```

### ⚙️ Run the App with Docker Compose

```bash
docker-compose up --build
```

🔗 Access the app at: [http://localhost:80](http://localhost:80)

---

## 🧪 Running Tests

To run unit tests with Pytest (inside container):

```bash
docker exec -it <flask_container_name> pytest test_app.py
```

Or locally:

```bash
pip install -r requirements.txt
pytest test_app.py
```

---

## 🛠 Troubleshooting & Tips

- ❌ **Port Already in Use**: Change the exposed ports in `docker-compose.yml`.
- ❌ **MongoDB Connection Fails**: Make sure MongoDB service is up and reachable by Flask.
- ✅ **Auto-Restart Containers**: Add `restart: always` in `docker-compose.yml` for production.
- 💡 **Debug Logs**: Check Flask logs at `/logs` endpoint or with `docker logs <flask_container>`.
- ⚙️ **Clean Environment**: Run `docker-compose down -v` to remove containers and volumes.

---

## 📅 Project Status

- ✅ **Stable**
- 🛠️ **Actively maintained**
- 🔍 **Open to contributions**

---

## 👨‍💻 Author

**Harshwardhan Jadhav**  
- 💼 [LinkedIn](https://www.linkedin.com/in/jadhavharshwardhan/)
- 📁 [GitHub Profile](https://github.com/Harshwardhanjadhav0)
- ✉️ Feel free to connect and collaborate!

---

## 💡 Contributing

Contributions are welcome! Please fork this repo, create a new branch and submit a pull request.

---

## 🧾 License

This project is licensed under the MIT License.