Sure, I'll add the instructions for manually adding the PostgreSQL server in pgAdmin to the README. Here's the updated README with the new section:

---

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

## Adding PostgreSQL Server in pgAdmin

To manually add the PostgreSQL server in pgAdmin, follow these steps:

1. Open pgAdmin in your web browser (`http://localhost:5050`) and log in.

2. Right-click on ‘Servers’ in the left-hand pane and select ‘Create’ -> ‘Server…’.

3. In the 'Create Server' window, give your server a name (e.g., `Local Postgres`).

4. Switch to the 'Connection' tab, enter `postgres` for 'Hostname/address', and fill in the username and password you set in the Docker configuration.

5. Click 'Save'. You should now be able to access your PostgreSQL databases in pgAdmin.

## Customization

- **Environment Variables**: Adjust PostgreSQL and pgAdmin settings in `docker-compose.yml`.

- **Data Persistence**: Modify the volume mapping for PostgreSQL data in `docker-compose.yml`.

## Stopping the Services

To stop the services, run:

```bash
docker-compose down
```

## Contributing

Contributions are welcome. Please fork the repository and submit pull requests with your changes.

## License

This project is licensed under the [MIT License](LICENSE.md).
