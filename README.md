# Cloud-Oriented Web Application Documentation

## Introduction
This documentation provides an overview of the cloud-oriented web application developed by Alikhon Hasankhonov (student Id: 48594), Khusan Khukumov (student Id: 48594) and Erali Choriyev (student Id: 48592) as part of their project to make the world a better place. The project utilizes PHP, MySQL, Redis, and Laravel framework to create a web application aimed at providing a useful platform for users.

## Installation
1. **Download Docker Desktop**: Install Docker Desktop from [here](https://www.docker.com/products/docker-desktop/).
2. **Install Ubuntu**: Follow the instructions [here](https://ubuntu.com/tutorials/install-ubuntu-desktop#7-ready-to-install) to install Ubuntu.
3. **Run Docker**: Run Docker on your system.
4. **Set Permissions**:
   - Before starting Docker containers, ensure that the project directory has the correct permissions. Run the following command in Ubuntu to set permissions recursively:
     ```bash
     chmod -R 755 .
     ```
   - This command will ensure that all files and directories in the project directory have the appropriate permissions for execution.
5. **Start Docker Containers**:
   - Navigate to the project directory.
   - Run the following command in Ubuntu to start Docker containers and install dependencies:
     ```bash
     ./vendor/bin/sail up
     ```
   - This command will install the project and its dependencies using Laravel Sail, which provides a Docker-powered local development environment.
   - Close the terminal window after the containers are up and running by pressing `Ctrl + C`.
6. **Run Docker Compose**:
   - After closing the terminal, run the following command to start the containers again using Docker Compose:
     ```bash
     docker-compose up
     ```
   - This command will ensure that your Docker containers continue to run in the background.
7. **Run Database Migrations and Seed Data**:
   - Once the containers are up and running, run the following command in a separate Ubuntu terminal to migrate the database schema and seed it with initial data:
     ```bash
     php artisan migrate --seed
     ```
   - This command will ensure that your database is properly configured and populated with the necessary data for the application to function.
9. **Open Localhost**:
   - Once everything is set up, open your web browser and go to `http://localhost` to access the running project.

## Project Structure
The project utilizes Docker containers to manage its components. The key components include:
- **PHP**: The PHP backend is powered by Laravel framework.
- **MySQL**: The database management system used for storing application data.
- **Redis**: Redis is used for caching purposes.
- **phpMyAdmin**: A web-based MySQL database administration tool.

## Usage
1. **Accessing phpMyAdmin**:
   - Access phpMyAdmin using the following URL: `http://localhost:8001`.
   - Use the following credentials to login:
     - Username: `sail`
     - Password: `password`
2. **Database Structure**:
   - The database includes tables for user registration and book management.
   - Additional tables can be created as needed.
3. **Seed Database**:
   - Populate the database with fake data using the following command: `php artisan db:seed`.
   - An admin user is created with the following credentials:
     - Email: `admin@domain.com`
     - Password: `password`
4. **Web Application Features**:
   - The web application provides functionality for viewing, creating, editing, and deleting books.
   - Admin users can manage books through the provided interface.

## Additional Functionalities
The project can be extended with additional functionalities as needed. Examples include user authentication, authorization, and more.

## Conclusion
The cloud-oriented web application developed by Alikhon Hasankhonov (student Id: 48594), Khusan Khukumov (student Id: 48594) and Erali Choriyev (student Id: 48592) aims to provide a useful platform for managing books. The application utilizes modern technologies such as PHP, MySQL, Redis, and Laravel framework, and is hosted on Docker containers for easy deployment and scalability.


