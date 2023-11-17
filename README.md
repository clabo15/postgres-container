# PostgreSQL with pgAdmin Docker Setup

This repository contains a Docker Compose setup for running a PostgreSQL database server along with pgAdmin, a popular web-based administration tool for PostgreSQL. The configuration ensures that both PostgreSQL and pgAdmin run using the latest available versions, allows connections from applications running on the host machine, and enables data persistence for the database.

## Prerequisites

Before you begin, ensure you have the following installed on your system:

- Docker
- Docker Compose

## Configuration

1. **PostgreSQL Configuration**: You can set your PostgreSQL user, password, and database name through environment variables in the `docker-compose.yml` file.

2. **pgAdmin Configuration**: Set your pgAdmin login email and password through environment variables in the `docker-compose.yml` file.

3. **Data Persistence**: The PostgreSQL data is persisted in a volume on the host machine. You can specify the path in the `docker-compose.yml` file.

## Usage

To use this setup, follow these steps:

1. Clone this repository to your local machine.

   ```bash
   git clone [Your Repository URL]
   ```

2. Navigate to the cloned repository's directory.

   ```bash
   cd [Your Repository Directory]
   ```

3. Edit the `docker-compose.yml` file to set your desired configuration for PostgreSQL and pgAdmin.

4. Run Docker Compose to start the services.

   ```bash
   docker-compose up -d
   ```

5. Access pgAdmin in your web browser at `http://localhost:5050`.

6. Connect to your PostgreSQL database using the credentials you configured. The database is accessible on the default PostgreSQL port `5432`.

## Customization

- **PostgreSQL Environment Variables**: Change `POSTGRES_PASSWORD`, `POSTGRES_USER`, and `POSTGRES_DB` in the `docker-compose.yml` file to your desired settings.

- **pgAdmin Environment Variables**: Change `PGADMIN_DEFAULT_EMAIL` and `PGADMIN_DEFAULT_PASSWORD` in the `docker-compose.yml` file for your pgAdmin access.

- **Data Persistence**: Modify the volume mapping under the `postgres` service in the `docker-compose.yml` file to your chosen local path for data persistence.

## Stopping the Services

To stop the running services, execute:

```bash
docker-compose down
```

## Contributing

Contributions to this project are welcome. Please fork the repository and submit a pull request with your changes or improvements.

## License

This project is licensed under the [MIT License](LICENSE.md).
