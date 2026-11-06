# Shneiderman's Eight Golden Rules

An interactive educational website exploring [Ben Shneiderman's](https://www.cs.umd.edu/~ben/index.html) [Eight Golden Rules of Interface Design](EIGHTRULES.md) through examples and quizzes.

## About the Project

This was originally developed as a group project for my Human-Computer Interaction class at Kent State University in Fall 2024.

This project demonstrates Shneiderman's Eight Golden Rules through interactive examples and a simple quiz system that allows users to test their understanding.

The original application has been restored and reorganized to make it easier to run, maintain, and potentially expand upon in the future.

## Project Status

The original website functionality has been preserved.

The project now includes a Docker-based MySQL environment, enivronment based configuration, and automatic database schema initialization.

Future improvements include redesigning portions of the website, modernizing the application architecture, and improving authentication and security.

I still might revisit some of the site design as well to improve my web development skills.

## Technologies

- HTML, CSS, JavaScript
- Node.js
- Express
- MySQL 8.4
- Docker Compose

## Getting Started

### Prerequisites

- Node.js (version 20.6 or newer)
- npm
- Docker Desktop with Docker Compose

### Installation

1. Clone the repository

```
git clone https://github.com/RixAt/8-golden-rules.git
cd 8-golden-rules
```

2. Install the dependencies

```
npm install
```

3. Create a local environment config from the example:

**macOS/Linux:**

```
cp .env.example .env
```

**PowerShell:**

```
Copy-Item .env.example .env
```

4. Open .env and configure the database connection, including a local development password. The database password must match the password configured for the MySQL container.

5. Start MySQL

```
docker compose up -d
```

On a fresh database volume, Docker automatically executes database/init.sql to create the required tables.

6. Start the application:

```
npm start
```

7. Open a browser and navigate to ```http://localhost:3000``` or the port configured in the application

### Stopping the Application

Stop the Node.js server with Ctrl+C.

To stop the MySQL container:

```
docker compose down
```

The database is stored in a persistent Docker volume, so users and quiz scores are retained between normal container restarts.

**Warning**: Running docker compose down -v also removes the database volume and deletes the locally stored data.

## Security Notice

This application preserves the authentication and quiz functionality of the original coursework project. It is **NOT** secure.

The legacy implementation has known security limitations, including plaintext password storage, client-controlled authentication cookies, and insufficient server-side validation.

**The application is intended for local development and educational use only. It should not be deployed publicly without significant security improvements.**

Do not use real or reused passwords when testing the application.

## Contributors

### Original development team:

- Brent Warring

- Gabe Colbrunn

- Ricky Atkinson

- Amari O'Bryant-Eppinger

- CJ Varga

The original coursework is preserved [here](https://github.com/bwarrin3/HCI-Final-Project).
