# PlayEconomy

PlayEconomy is a simulation platform designed to mimic economic activities. The platform allows for the management of inventories, cataloging items, and facilitating various economic transactions. This project leverages a microservices architecture to ensure scalability and maintainability.

## Table of Contents

1. [Technologies](#technologies)
2. [Architecture](#architecture)
3. [Getting Started](#getting-started)
4. [Project Structure](#project-structure)
5. [Configuration](#configuration)
6. [Running the Application](#running-the-application)
7. [Contributing](#contributing)
8. [License](#license)

## Technologies

### Frontend

- React
- Bootstrap

### Backend

- .NET Core
- RabbitMQ (for messaging)
- MongoDB (NoSQL database)

### DevOps

- Docker (for containerization)
- Docker Compose

## Architecture

The project follows a microservices architecture consisting of the following services:

- **Catalog Service (Play.Catalog)**: Manages the cataloging of items.
- **Inventory Service (Play.Inventory)**: Handles inventory management.
- **Common Service (Play.Common)**: Provides shared utilities and components used across different services.
- **Frontend Service (Play.Frontend)**: React-based frontend application that interacts with the backend services.

## Getting Started

### Prerequisites

- Docker
- .NET Core SDK
- Node.js
- npm (Node Package Manager)

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/almoghindi/PlayEconomy.git
    cd PlayEconomy
    ```
2. Set up the environment variables:
    ```bash
    cp .env.example .env
    ```
3. Install frontend dependencies:
    ```bash
    cd Play.Frontend
    npm install
    cd ..
    ```
4. Build and run the services using Docker Compose:
    ```bash
    docker-compose up --build
    ```

## Project Structure

```plaintext
PlayEconomy/
├── .vs/
├── Play.Catalog/
│   └── src/
├── Play.Common/
│   └── src/
├── Play.Frontend/
│   ├── public/
│   ├── src/
│   ├── .env
│   ├── .gitignore
│   ├── package.json
│   ├── package-lock.json
│   └── README.md
├── Play.Infra/
├── Play.Inventory/
│   └── src/
└── docker-compose.yml

## Configuration

The configuration is managed through environment variables defined in the `.env` file. Here is an example of the configuration variables you might need to set:

```env
MONGO_URI=mongodb://mongo:27017/playeconomy
RABBITMQ_URI=amqp://rabbitmq
```
## Running the Application

To start the application:

1. Ensure Docker is running.
2. Run the following command to start all services:
    ```bash
    docker-compose up
    ```
3. The application should now be accessible from [http://localhost:3000](http://localhost:3000).
