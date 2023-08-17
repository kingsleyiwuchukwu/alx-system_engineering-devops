# Application Server

This repository contains the application deployment project for our AirBnB clone. The goal is to configure Nginx on the web servers provided by ALX to serve a WSGI Flask app running through Gunicorn. Additionally, we set up an Upstart script to ensure the application stays running even after server reboots.

## Tasks

### Task 0: Set up development with Python

In this task, we configure the file `web_flask/0-hello_route.py` from our AirBnB_clone_v2 to serve content on the route `/airbnb-onepage/`, running on port 5000.

### Task 1: Set up production with Gunicorn

This task involves setting up a production environment, installing Gunicorn, and configuring it to serve the file from Task 0.

### Task 2: Serve a page with Nginx

- **File**: `2-app_server-nginx_config`
- **Description**: Nginx configuration file that proxies requests on the route `/airbnb-onepage/` to the Gunicorn app running on port 5000.

### Task 3: Add a route with query parameters

- **File**: `3-app_server-nginx_config`
- **Description**: Nginx configuration file that proxies requests on the route `/airbnb-dynamic/number_odd_or_even/<int:num>` to the Gunicorn app running on port 5000.

### Task 4: Let's do this for your API

In this task, we configure the API from our AirBnB_clone_v3 to run on Gunicorn.

- **File**: `4-app_server-nginx_config`
- **Description**: Nginx configuration file that proxies requests on the AirBnB API to the corresponding Gunicorn app.

### Task 5: Serve your AirBnB clone

In this task, we configure the complete AirBnB app from AirBnB_clone_v4 to run on Gunicorn and be served through Nginx.

- **File**: `5-app_server-nginx_config`
- **Description**: Nginx configuration file configured to serve the static assets from `web_dynamic/static/` on the Gunicorn AirBnB app.

### Task 6: Deploy it

- **File**: `gunicorn.conf`
- **Description**: Configuration file for an Upstart script that starts a Gunicorn process bound to port 5003. It serves the content from Task 5. The Gunicorn process spawns three worker processes and logs errors to `/tmp/airbnb-error.log` and access to `/tmp/airbnb-access.log`.

### Task 7: No service interruption

- **File**: `4-reload_gunicorn_no_downtime`
- **Description**: Bash script that gracefully reloads Gunicorn, ensuring no service interruption during the process.

For detailed instructions and configurations, please refer to the respective task files.

---

This repository serves as a comprehensive guide for setting up the application server for our AirBnB clone project. For more detailed information on each task, please refer to the corresponding files.
