# Drone Delivery Management System

SkyRoute is an advanced platform designed to streamline drone-based deliveries. Built with a microservices architecture, this project leverages multiple technologies to ensure scalability, efficiency, and robust performance.

## Table of Contents

- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Development](#development)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Features

- **Real-Time Drone Tracking:** Monitor drone locations and statuses in real-time.
- **Go API Backend:** The core API is developed in Go for high performance and concurrency.
- **React Frontend:** An interactive and responsive user interface built with React.
- **Microservices Architecture:**
  - Services implemented using both Python and Golang to handle business logic.
  - Asynchronous communication and integration via Kafka and RabbitMQ.
- **Containerized Deployment:** Fully containerized with Docker to simplify deployment and scaling.
- **Modular Design:** Clear separation of concerns between the API, frontend, and service layers.

## Project Structure

```plaintext
/skyroute   ../
├── .git/                   # Git repository metadata
├── docker/                 # Docker configurations and compose files
├── docs/                   # Project documentation and guides
├── release/                # Release assets, binaries, and changelogs
├── scripts/                # Utility scripts for deployment, testing, etc.
├── src/                    # Source code for the project
│   ├── api/                # API services written in Go
│   ├── frontend/           # Frontend application built with React
│   └── services/           # Microservices:
│         ├── python_service/   # Services implemented in Python
│         └── golang_service/   # Services implemented in Golang
├── .editorconfig           # Editor configuration settings
├── .gitattributes          # Git attributes definitions
├── .gitignore              # Git ignore rules
├── LICENSE                 # License file for the project
└── README.md               # This README file
```

## Installation

### Prerequisites

- [Docker](https://www.docker.com/get-started) (v20+ recommended)
- [Docker Compose](https://docs.docker.com/compose/install/)
- [Git](https://git-scm.com/)

### Setup

#### Clone the Repository

```bash
git clone https://github.com/raivokinne/skyroute.git
cd skyroute
```

#### Build and Run with Docker

The project includes Docker configurations for all components, including the Go API, React frontend, Python/Golang services, Kafka, and RabbitMQ:

```bash
docker-compose up --build
```

This command builds the Docker images and starts all the services.

#### Manual Setup

Alternatively, you can set up each component individually:

- **API (Go):**
  ```bash
  cd src/api
  go run main.go
  ```

- **Frontend (React):**
  ```bash
  cd src/frontend
  npm install
  npm start
  ```

- **Services:**
  - **Python Service:**
    ```bash
    cd src/services/python_service
    pip install -r requirements.txt
    python main.py
    ```
  - **Golang Service:**
    ```bash
    cd src/services/golang_service
    go run main.go
    ```

## Usage

Once the services are running, you can access the application components:

- **Frontend:** Open your web browser and navigate to `http://localhost:3000` (or the port specified in your Docker configuration).
- **API:** The API will be accessible at `http://localhost:8000` (or as defined in your configuration).
- **Messaging Services:** Kafka and RabbitMQ will be running as defined in the Docker setup for handling asynchronous communications between services.

### Common Commands

- **Start All Services:**
  ```bash
  docker-compose up
  ```

- **Stop All Services:**
  ```bash
  docker-compose down
  ```

- **View Logs:**
  ```bash
  docker-compose logs -f
  ```

## Development

### Code Overview

- **API (Go):** Implements RESTful endpoints and core business logic.
- **Frontend (React):** Provides the user interface for interacting with the system.
- **Services (Python & Golang):** Handle specialized tasks and background processing.
- **Messaging:** Kafka and RabbitMQ are used to facilitate communication between microservices.

### Running Locally

To develop or test specific components:

- **Go API:**
  ```bash
  cd src/api
  go run main.go
  ```

- **React Frontend:**
  ```bash
  cd src/frontend
  npm install
  npm start
  ```

- **Python Service:**
  ```bash
  cd src/services/python_service
  pip install -r requirements.txt
  python main.py
  ```

- **Golang Service:**
  ```bash
  cd src/services/golang_service
  go run main.go
  ```

### Testing

Test scripts are provided in the `scripts/` directory. To run tests:

```bash
./scripts/run_tests.sh
```

*Ensure all necessary dependencies are installed and environment variables are configured as needed.*

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Ensure your changes include relevant tests.
4. Submit a pull request with a detailed description of your changes.

For major changes, please open an issue first to discuss your ideas.

## License

This project is licensed under the terms outlined in the [LICENSE](./LICENSE) file.

## Contact

For questions, suggestions, or contributions, please reach out to:

- **Project Maintainer:** [Raivo](mailto:raivokinne236@gmail.com)
- **GitHub:** [raivokinne](https://github.com/raivokinne)


