# Running Geo Application

This repository contains the code for the client and server components of the Geo Application. Below are the instructions to set up and run the application using Docker.

## Prerequisites

- [Docker](https://www.docker.com/get-started) installed on your system

## Steps to Run

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your/repository.git
   cd repository
   ```

2. **Set Up Docker Compose File**

   - Open the `docker-compose.yml` file.
   - Ensure that the `image` field for both `client` and `Server` services reflects the required Node.js versions or specific images needed.

3. **Run Docker Compose**

   - Open a terminal in the root directory of the cloned repository.
   - Run the following command to start the services:
     ```bash
     docker-compose up
     ```
   This command will build and start the containers based on the configurations specified in the `docker-compose.yml` file.

4. **Access the Application**

   - Once the containers are up and running, you can access the client application at `http://localhost:8080`.
   - The server will be available at `http://localhost:3000`.

## Notes

- The `docker-compose.yml` file defines the setup for both the client and server components of the application.
- Ports `8080` and `3000` are exposed for the client and server, respectively. Adjust these ports in the `docker-compose.yml` file if needed.
- The code for the client and server is expected to be located in the `geo_client` and `geo_server` directories, respectively. Adjust the `source` field in the `volumes` section if your code resides elsewhere.

If you encounter any issues, ensure that you have the necessary Node.js dependencies in your code directories and that the Docker images specified in the `docker-compose.yml` file are available.
