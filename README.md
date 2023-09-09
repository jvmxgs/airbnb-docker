# Airbnb Docker

This repository contains the Docker setup for the Airbnb project, including the frontend and backend components. Follow the steps below to set up and run the system locally.

## Prerequisites

Before you begin, ensure you have the following installed:

- [Git](https://git-scm.com/)
- [Docker](https://www.docker.com/get-started)

## Installation

1. Clone the repository and navigate to the project directory:

    ```bash
    git clone git@github.com:jvmxgs/airbnb-docker.git
    cd airbnb-docker/
    ```

2. Initialize and update the submodules:

    ```bash
    git submodule update --init --recursive
    ```

3. Navigate to the frontend submodule and switch to the main branch:

    ```bash
    cd airbnb-front
    git checkout main
    cd ../
    ```

4. Navigate to the backend submodule and switch to the main branch:

    ```bash
    cd airbnb-back
    git checkout main
    ```

5. Copy the example environment file and configure it with your SMTP credentials.

    ```bash
    cp .env.example .env
    ```

    Update the `.env` file with your SMTP credentials:

    ```env
    SMTP_HOST=smtp.ethereal.email
    SMTP_PORT=587
    SMTP_USERNAME=sincere32@ethereal.email
    SMTP_PASSWORD=WDuARawQgPV7gMg3hw
    ```
    You can create an account at [ethereal.email](https://ethereal.email) and use their SMTP service for testing:

6. Return to the main project directory:

    ```bash
    cd ../
    ```

## Running the System

7. Start the system using Docker Compose, which will build the necessary containers:

    ```bash
    docker-compose up --build
    ```

8. Once the containers are up and running, you can access the system by visiting [http://localhost:8080](http://localhost:8080) in your web browser.
